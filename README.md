<h1 align="center">OS X Setup</h1>

<p align="center" >
	<img src="https://png.icons8.com/ios/1600/mac-os-filled.png" width="140px" />
</p>

<h3 align="center">
	OS X development environment setup
</h3>

<p align="center">
  <a href="https://github.com/srslafazan/osx-setup/blob/master/license">
		<img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat">
  </a>
</p>

## Setup

### Apple

- xcode-select --install
- softwareupdate --install

### Package Manager

- [Homebrew](https://brew.sh/)

### OS X Applications

- [iTerm](https://www.iterm2.com/)
- [Oh-My-Zsh](http://ohmyz.sh/)
- [Slack](https://itunes.apple.com/us/app/slack/id803453959?mt=12)
- [Spectacle](https://www.spectacleapp.com/)
- [Flux](https://justgetflux.com/)

### Languages

- [Node](https://nodejs.org/)
```bash
brew install nvm
nvm install node
```
- [Ruby](https://www.ruby-lang.org/)
```bash
brew install rbenv
rbenv init
rbenv install 2.5.1  # Latest stable version, 4-19-2018
```
- [Python](https://www.python.org/)
```bash
brew install openssl
brew install readline
brew install pyenv
pyenv install 2.7.14
pyenv install 3.6.2
```


### CLI Tools

- [YADR](https://github.com/skwp/dotfiles/) - Thanks @bkimbriel

### Path

Link cli tools
```
PATH="$PATH:/bin"
PATH="$PATH:/sbin"
PATH="$PATH:/usr/bin"
PATH="$PATH:/usr/sbin"
PATH="$PATH:/usr/local/bin"
PATH="$PATH:/usr/local/sbin"
PATH="$PATH:/usr/local/opt"
```