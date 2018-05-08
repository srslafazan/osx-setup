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
```bash
xcode-select --install
```

```bash
softwareupdate --install
```

### Package Manager

- [Homebrew](https://brew.sh/)

### OS X Applications

- [iTerm](https://www.iterm2.com/)
- [Oh-My-Zsh](http://ohmyz.sh/)
- [Slack](https://itunes.apple.com/us/app/slack/id803453959?mt=12)
- [Spectacle](https://www.spectacleapp.com/)
- [Flux](https://justgetflux.com/)

### Languages

[Ruby](https://www.ruby-lang.org/)
```bash
brew install rbenv
rbenv init
rbenv install 2.5.1  # Latest stable version, 4-19-2018
```

[Python](https://www.python.org/)
```bash
brew install openssl
brew install readline
brew install python@2  # Python2 is still a common legacy dependency
brew install python@3
# You may want to link /usr/local/bin/python3 to /usr/local/bin/python
```


### CLI Tools

- [YADR](https://github.com/skwp/dotfiles/) - Thanks @bkimbriel !
- [Electron](https://electronjs.org/)
- [Docker](https://store.docker.com/editions/community/docker-ce-desktop-mac)

### Path

Link CLI tools
```
PATH="$PATH:/bin"
PATH="$PATH:/sbin"
PATH="$PATH:/usr/bin"
PATH="$PATH:/usr/sbin"
PATH="$PATH:/usr/local/bin"
PATH="$PATH:/usr/local/sbin"
PATH="$PATH:/usr/local/opt"
```

### Applications

[Node](https://nodejs.org/)
```bash
brew install nvm  # Thanks @justinsisley !
nvm install node
```

[PostgreSQL](https://www.postgresql.org/)
```bash
brew install postgresql
```

[MongoDB](https://www.mongodb.com/)
```bash
brew install mongodb
```

[React Native](https://github.com/facebook/react-native)
```bash
npm install -g react-native-cli
# Extras
brew install watchman
npm install exp --global
```

## SDKs

- [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

## Credits

- Image (https://png.icons8.com)
