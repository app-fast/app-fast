Concurrent package downloader written in bash/zsh, for macOS and Linux.

Inspired by [apt-fast](https://github.com/ilikenwf/apt-fast) and [powerpill](https://aur.archlinux.org/packages/powerpill).

The only dependency is aria2.

### Usage

on macOS:

```sh
app-fast install vim tmux git
app-fast upgrade
```

on Ubuntu/Debian:

```sh
app-fast install vim tmux git -y
app-fast upgrade -y
```

on Archlinux/Manjaro:

```sh
app-fast -S vim tmux git
app-fast -Syu
```

### Install

Just download (app-fast)[app-fast] and save it to somewhere like `/usr/bin/app-fast`.

on macOS, you should put it to `/usr/local/bin/app-fast`.

Make sure you have the permission to execute it `chmod +x app-fast`.

### What it does

* Download packages faster
* Upgrade packages faster
* Support macOS homebrew
* Support Ubuntu/Debian
* Support Archlinux

### What it doesn't

* Uninstall a package
* Search a package
* Support Android Termux
* Support Archlinux AUR
* Support macOS homebrew tap
* Support macOS homebrew bottles like `bottles-science` and `bottle :unneeded`
* Support Ubuntu mirror protocol like `mirror://mirrors.ubuntu.com/mirrors.txt`
* Support proxies

### Note

* I don't have any apple devices so macOS port is experimental.
* On Linux I use sed command, on macOS I use perl command.

### Why not apt-fast or powerpill

* I use it for docker containers and [KVMs](https://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine), only installing packages is needed.

### License

Public Domain
