# Ansible configuration for my dotfiles

This repository takes care of installing all the dependencies for my dotfiles,
including cloning my dotfiles and placing the files accordingly.

## Requirements

Make sure you have [Homebrew](https://brew.sh/) installed:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Then install Ansible using Homebrew with `brew install ansible`

## How to run

For Linux:
    1. `ansible-playbook -i inventory linux.yml -K`
For OSX:
    1. `ansible-playbook -i inventory osx.yml -K`

Further, you can take a look at my `dotfiles`
[here](https://github.com/benmezger/dotfiles)
