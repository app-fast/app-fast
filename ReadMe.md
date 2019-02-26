Concurrent package downloader written in bash/zsh, for macOS, Linux, Android and Windows Msys2.

Inspired by [apt-fast](https://github.com/ilikenwf/apt-fast) and [powerpill](https://aur.archlinux.org/packages/powerpill).

The only dependency is [aria2](https://github.com/aria2/aria2).

### Usage

on macOS:

```sh
brew update
app-fast install vim tmux git
app-fast upgrade
```

on Ubuntu/Debian/Android Termux:

```sh
app-fast update
app-fast install vim tmux git -y
app-fast upgrade -y
```

on Archlinux/Manjaro/Windows Msys2:

```sh
app-fast -S vim tmux git
app-fast -Syu
```

### Install

Just download [app-fast](app-fast) and save it to somewhere like `/usr/bin/app-fast`.

On macOS, you should put it to `/usr/local/bin/app-fast`.

Make sure you have the permission to execute it `chmod +x app-fast`.

On Windows Msys2, you should put [aria2.exe](https://github.com/aria2/aria2/releases) to your system path first, because Msys2 does not provide aria2 package.


### Install for Linux

Wget

```sh
sudo wget https://raw.githubusercontent.com/joeky888/app-fast/master/app-fast -O /usr/bin/app-fast
sudo chmod +x /usr/bin/app-fast
```

Curl

```sh
sudo curl https://raw.githubusercontent.com/joeky888/app-fast/master/app-fast -o /usr/bin/app-fast
sudo chmod +x /usr/bin/app-fast
```

Aria2

```sh
sudo aria2c https://raw.githubusercontent.com/joeky888/app-fast/master/app-fast -d / -o /usr/bin/app-fast
sudo chmod +x /usr/bin/app-fast
```

### Install for macOS

```sh
curl https://raw.githubusercontent.com/joeky888/app-fast/master/app-fast -o /usr/local/bin/app-fast
sudo chmod +x /usr/local/bin/app-fast
```

### Install for Android Termux

```sh
pkg i curl -y
curl https://raw.githubusercontent.com/joeky888/app-fast/master/app-fast -o $PREFIX/bin/app-fast
chmod +x $PREFIX/bin/app-fast
```

### What it does

* Download packages faster
* Upgrade packages faster
* Support macOS homebrew
* Support Ubuntu/Debian
* Support Archlinux
* Support Android Termux
* Support Windows Msys2

### What it doesn't

* Uninstall a package
* Search a package
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
