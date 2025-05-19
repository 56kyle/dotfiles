# dotfiles
Various system configurations across many environments meant for use with GNU Stow


# Overview

This purpose of this repository is to store and organize various dotfiles used to configure Linux based systems.

The branching strategy of this repo is designed to organize both based on distro and the execution environment.

However, the goal is less to fill out all of the combinations and moreso just make sure that incompatible settings don't get mixed around.

## Branching Overview

```
- main
| - debian
| - | - debian-system
| - | - debian-wsl
| - | - debian-docker
| - | - ubuntu
| - | - | - ubuntu-system
| - | - | - ubuntu-wsl 
| - | - | - ubuntu-docker 
| - arch
| - | - arch-system
| - | - arch-wsl
| - | - arch-docker
| - red-hat
| - | - ...
```

The branches ideally should be used where each change is done at the most general level so that other braches can just rebase as needed.

However, that is much easier said than done, so many times it will be that more specific branches may receive changes, and then as other sibling branches get the same changes portions can be cherrypicked.

What this would look like in progress is changes may be committed to ubuntu-system, but then if a branch ubuntu-wsl is made then that warrants running a git diff and seeing what can be brought back into the ubuntu parent branch.

