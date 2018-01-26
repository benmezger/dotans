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

### Requirements (Linux)

The Linux version is configured to install on a Archlinux distro. You can easily adapt it to work on another Linux distribution.

Install Ansible using `pacman -Syy ansible`

## How to run

For Linux: `ansible-playbook -i inventory linux.yml -K` .

For OSX: `ansible-playbook -i inventory osx.yml -K`.

Further, you can take a look at my `dotfiles`
[here](https://github.com/benmezger/dotfiles)

## Packages
### Vim

`dotans` installs a few Vim packages (both for Linux and OSX)

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
For Linux, `dotans` installs:

#### Pacman
- python2
- python2-pip
- vim
- fasd
- ack
- gnupg2
- tmux
- tor
- valgrind
- chromium
- zsh
- xorg-xset
- xorg-xrdb
- dunst
- pcsclite
- feh
- pcsc-tools
- stow
- scrot
- xautolock
- wget
- rofi
- openssh
- lxappearance
- ccid
- imagemagick
- cmake
- libu2f-host
- linux-zen
- linux-zen-headers
- linux-headers
- neovim
- gnome-keyring
- acpi
- gdb
- unrar
- zathura-pdf-mupdf
- redshift
- networkmanager
- network-manager-applet
- networkmanager-openvpn
- noto-fonts-emoji
- ttf-symbola
- ttf-font-awesome
- the_silver_searcher
- vagrant
- docker
- htop
- urxvt-perls
- rxvt-unicode
- xf86-input-evdev
- xf86-input-mouse
- xf86-input-keyboard
- xf86-video-intel
- slim
- qt5-base

#### AUR
It also installs a few package from AUR (using Aura).

- xss-lock
- spotify
- numix-icon-theme-git
- gitter
- dropbox
- git-crypt
- otf-inconsolata-dz
- pairing_tool

### Linux services
`dotans` enables a few `systemd` services.

- pcscd.socket
- NetworkManager.service
- slim.service
