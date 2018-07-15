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
brew install python@2  # Python2 is still a common legacy dependency, used in enterprise production apps, etc.
brew install python@3
# You may want to link /usr/local/bin/python3 to /usr/local/bin/python
```

[Java SE](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

- - Also, via Homebrew

```bash
brew tap caskroom/versions
brew cask install java8
```

- Consider [jenv](http://www.jenv.be/) for version management:

```bash
brew install jenv
# ... add versions, ex:
jenv add /Library/Java/JavaVirtualMachines/jdk1.8.0_172.jdk/Contents/Home/
```

## SDKs


### CLI Tools

- [YADR](https://github.com/skwp/dotfiles/) - Thanks @bkimbriel !
- [Electron](https://electronjs.org/)
- [Docker](https://store.docker.com/editions/community/docker-ce-desktop-mac)

### Path

Link CLI tools
```bash
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

[Android Studio](https://developer.android.com/studio/)

- Consider adding the CLI tools to your path:

```bash
PATH="$PATH:~/Library/Android/sdk/tools"
PATH="$PATH:~/Library/Android/sdk/tools/bin"
```

- Consider installing Android SDK Components and Platform Tools, Emulators (AVD Manager)

### Orchestration

- Kubernetes
[kubectl](https://kubernetes.io/)
```bash
# kubectl
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/darwin/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
# minikube
curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.25.2/minikube-darwin-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```
[heml](https://helm.sh/)
```bash
brew install kubernetes-helm
```

## Credits

- Image (https://png.icons8.com)
