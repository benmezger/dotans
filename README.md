# Ansible configuration for my dotfiles – [![Build Status](https://travis-ci.org/benmezger/dotans.svg?branch=master)](https://travis-ci.org/benmezger/dotans) (OSX)

This repository takes care of installing all the dependencies for my dotfiles,
For this to work, make sure you first clone my [dotfiles](https://github.com/benmezger/dotfiles.git) to your `$HOME`.

## Requirements
### Requirements (OSX)

Make sure you have [Homebrew](https://brew.sh/) installed:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Then install Ansible using Homebrew with `brew install ansible`

### Requirements (Archlinux)

You can easily adapt it to work on another Linux distribution.

Install Ansible using `pacman -Syy ansible`

## How to run

For Archlinux: `ansible-playbook -i inventory archlinux.yml -K`.

For OSX: `ansible-playbook -i inventory osx.yml -K`.

Further, you can take a look at my `dotfiles`
[here](https://github.com/benmezger/dotfiles)

