# Basic vim initialization

This is a basic vim initialization that I like, with some basic plugins.

## Install

Run the following to get the vimrc and install the plugins:

```sh
curl -fLo ~/.vimrc https://raw.githubusercontent.com/runih/basic-vimrc/main/vimrc
grep "plug.vim" ~/.vimrc | sed 's/^" //' | sh
vim -c "PlugInstall"
```
