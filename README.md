# Basic vim initialization

This is a basic vim initialization that I like, with some basic plugins.

## Requirements

Make sure `curl`and `git` is installed on the system!

## Optional

To get the statusbar to look nicer, you need to install a font that supports powerline. Powerline fonts can be found [here](https://github.com/powerline/fonts).

![statusbar](statusbar.png)

Make sure to use UTF-8 encoding in the terminal

## Install

Run the following to get the vimrc and install the plugins:

```sh
curl -fLo ~/.vimrc https://raw.githubusercontent.com/runih/basic-vimrc/main/vimrc
grep "plug.vim" ~/.vimrc | sed 's/^" //' | sh
vim -c "PlugInstall"
```
