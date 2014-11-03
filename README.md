This is my standard setup for Ubuntu 14.04 which includes YADR.

## Install zsh
```zsh
sudo apt-get update
sudo apt-get install zsh
```

## Set zsh as default shell
```zsh
chsh -s $(which zsh)
```

## Install vim
```zsh
sudo apt-get install vim
```
Reference: https://www.digitalocean.com/community/tutorials/installing-and-using-the-vim-text-editor-on-a-cloud-server

## Install git
```zsh
sudo apt-get update
sudo apt-get install git
```

## Setup git
```zsh
git config --global user.name “Eson Paguia”
git config --global user.email “etpaguia@gmail.com”
git config --list
```

## Install vim-*
To make neocomplete work in vim, you must have/install any of these packages:
  * vim-nox
  * vim-gtk
  * vim-gnome
  * vim-athena

To install vim-gtk:
```zsh
sudo apt-get install vim-gtk
```

Reference:
http://askubuntu.com/questions/281886/what-is-the-difference-between-the-different-vim-packages-available-in-ubuntu

## Install yadr
```zsh
sh -c "`curl -fsSL https://raw.github.com/skwp/dotfiles/master/install.sh`”
```

## Correct the colorscheme of vim
```zsh
vi .yadr/vim/settings.vim 
```

Add the following lines at the end of the settings.vim file: 
```zsh      
syntax enable
set background=dark 
let g:solarized_termcolors=256 
colorscheme solarized 

if has('gui_running') 
  set background=light 
else 
   set background=dark 
endif
```

eg.
![screenshot](https://raw.githubusercontent.com/etpaguia/setup-ubuntu-14.04/master/images/settings-vim.png)

Reference: https://github.com/altercation/vim-colors-solarized
