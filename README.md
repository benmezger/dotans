# Ansible configuration for my dotfiles

This repository takes care of installing all the dependencies for my dotfiles,
including cloning my dotfiles and placing the files accordingly.

## How to run

For Linux:
    1. `ansible-playbook -i inventory linux.yml -K`
For OSX:
    1. `ansible-playbook -i inventory osx.yml -K`

Further, you can take a look at my `dotfiles`
[here](https://github.com/benmezger/dotfiles)
