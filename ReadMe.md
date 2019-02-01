Concurrent package downloader written in bash/zsh, support macOS and Linux.

Inspired by [apt-fast](https://github.com/ilikenwf/apt-fast).

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

Just download `app-fast` and save it to somewhere like `/usr/bin/app-fast`.

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
* Support macOS homebrew tap
* Support macOS homebrew bottles like `bottles-science`
* Support Ubuntu mirror protocal like `mirror://mirrors.ubuntu.com/mirrors.txt`
* Support RPM-based Linux
* Support Alpine Linux

### Note

* I don't have any apple devices so macOS port is experimental.

### License

Public Domain
