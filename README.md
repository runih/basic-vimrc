# Basic vim initialization

This is a basic vim initialization that I like, with some basic plugins.

## Requirements

### Windows

Make sure [git](https://git-scm.com/downloads) is installed

### *nix

Make sure `curl`and [git](https://git-scm.com/downloads) is installed on the system!

## Optional

To get the statusbar to look nicer, you need to install a font that supports powerline. Powerline fonts can be found [here](https://github.com/powerline/fonts).

![statusbar](statusbar.png)

Make sure to use UTF-8 encoding in the terminal

## Install

Run the following to get the vimrc and install the plugins:

### Windows

Run the following in PowerShell:

```PowerShell
New-Item -Path $HOME/vimfiles/autoload -ItemType 'directory' &&  Invoke-WebRequest https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim -OutFile $HOME/vimfiles/autoload/plug.vim && Invoke-WebRequest https://raw.githubusercontent.com/runih/basic-vimrc/main/vimrc -OutFile $HOME/_vimrc
```

Then start *vim* and run the following command `:PlugInstall`

### *nix

```sh
curl -fLo ~/.vimrc https://raw.githubusercontent.com/runih/basic-vimrc/main/vimrc
grep "plug.vim" ~/.vimrc | sed 's/^" //' | sh
vim -c "PlugInstall"
```

## Test with docker

Run the following:

```sh
docker run --rm --name ubuntu-test-vim -it ubuntu /bin/bash -c "apt update && apt upgrade -y && apt install -y curl git vim && curl -fLo ~/.vimrc https://raw.githubusercontent.com/runih/basic-vimrc/main/vimrc && grep \"plug.vim\" ~/.vimrc | sed 's/^\" //' | sh && vim -c \"PlugInstall\" && bash"
```
