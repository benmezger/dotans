# Ansible configuration for my dotfiles

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

## Requirements (Gentoo)

To install Ansible using Emerge, run `emerge  --ask --verbose app-admin/ansible`

## How to run

For Archlinux: `ansible-playbook -i inventory archlinux.yml -K`.

For Gentoo: `ansible-playbook -i inventory gentoo.yml  -K`.

For OSX: `ansible-playbook -i inventory osx.yml -K`.

Further, you can take a look at my `dotfiles`
[here](https://github.com/benmezger/dotfiles)

## Packages
### Vim

`dotans` installs the following Vim packages (both for Linux and OSX)

- Vim-Plug

### ZSH

`dotans` installs a few ZSH packages (both for Linux and OSX)

- Zsh-Plug

### Tmux

`dotans` installs a few Tmux packages (both for Linux and OSX)

- Tmux-TPM

### Python

`dotans` installs a few Python packages using `pip2` (both for Linux and OSX)

- virtualenvwrapper
- ipython
- grasp
- neovim

### OSX
#### Homebrew

For OSX, `dotans` installs:
- python
- python3
- vim
- fasd
- ack
- gnupg2
- tmux
- tor
- reattach-to-user-namespace
- stow
- pinentry-mac
- git
- the_silver_searcher
- diff-so-fancy
- cmake
- mas

#### Homebrew cask
`dotans` installs a few casks.

- google-chrome
- transmission
- iterm2
- vlc
- skype
- spotify
- docker
- 1password
- hopper-disassembler
- java
- font-inconsolata-dz

#### App Store
`dotans` installs a few App Store apps using `mas`.

```
- 599327197  # Collective
- 1094298678 # RealDNS
- 443126292  # TrashMe
- 737047715  # Magic Number
- 1262957439 # Textual 7
- 639764244  # Xee
- 441258766  # Magnet
- 409789998  # Twitter
- 747648890  # Telegram
```

### Linux
For Archlinux, see [https://github.com/benmezger/dotans/blob/master/roles/archlinux/tasks/pacman.yml](this file).

For Gentoo, see [https://github.com/benmezger/dotans/blob/master/roles/gentoo/tasks/emerge.yml](this file).

### Linux services
`dotans` enables a few `systemd` services.

- pcscd.socket
- NetworkManager.service
- slim.service
