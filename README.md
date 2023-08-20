<h1 align="center">OS X Setup</h1>

<p align="center" >
	<img src="https://png.icons8.com/ios/1600/mac-os-filled.png" width="140px" />
</p>

<h3 align="center">
	OS X development environment setup
</h3>

<p align="center">
  A collection of tools, applications, and frameworks for developing tools, applications, and frameworks.
</p>

<p align="center">
  <a href="https://github.com/srslafazan/osx-setup/blob/master/license">
		<img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat">
  </a>
</p>


## Setup

### Apple


```bash
xcode-select --install
softwareupdate --install
```

### Dotfiles

[Oh My ZSH](https://ohmyz.sh/)
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```


### Package Managers

[Homebrew](https://brew.sh/)

Packages:
> - openssl
> - postgresql
> - mongodb
> - watchman
> - rbenv
> - jenv
> - go
> - readline
> - python@2
> - python@3
> - mas
> - --cask adoptopenjdk/openjdk/adoptopenjdk14


```bash
brew tap homebrew/cask-versions
brew update
brew tap homebrew/cask
brew tap mongodb/brew
brew tap adoptopenjdk/openjdk


brew install \
  openssl \
  nvm \
  postgresql \
  mongodb-community@4.4 \
  watchman \
  rbenv \
  jenv \
  go \
  readline \
  python \
  python@3

brew install --cask adoptopenjdk/openjdk/adoptopenjdk7
brew install --cask adoptopenjdk/openjdk/adoptopenjdk8
brew install --cask adoptopenjdk/openjdk/adoptopenjdk14

```

[npm](https://www.npmjs.com/)

Global Packages:
> - yarn
> - exp
> - react-native-cli
> - http-server
> - dotenv
> - truffle


### OS X Applications

- [iTerm](https://www.iterm2.com/)
- [Oh-My-Zsh](http://ohmyz.sh/)
- [Slack](https://itunes.apple.com/us/app/slack/id803453959?mt=12)
- [Spectacle](https://www.spectacleapp.com/)
- [Flux](https://justgetflux.com/)

### Languages

[Terraform](https://www.terraform.io/)
```bash
brew install tfenv
tfenv install
```

[Rust](https://www.rust-lang.org/tools/install)
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
echo """
export PATH="$PATH:~/.cargo/bin"
"""
source ~/.zshrc
source ~/$HOME/.cargo/env
```

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
brew install python  # Python2 is still a common legacy dependency, used in enterprise production apps, etc.
brew install python@3
# You may want to link /usr/local/bin/python3 to /usr/local/bin/python
```

[Java SE](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

- Also, via Homebrew

```bash
brew tap homebrew/cask-versions
brew update
brew tap homebrew/cask
brew install --cask adoptopenjdk/openjdk/adoptopenjdk14
```

- Consider [jenv](http://www.jenv.be/) for version management:

```bash
brew install jenv
# ... add versions, ex:
jenv add /Library/Java/JavaVirtualMachines/jdk1.8.0_172.jdk/Contents/Home/
```

[Go](https://golang.org/)
```bash
brew install go
```
## SDKs


### CLI Tools

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

### Editors

[VSCode](https://code.visualstudio.com/) / [Cursor](https://www.cursor.so/)

Extensions
- GitLens
- GitHub Pull Requests and Issues
- HashiCorp Terraform

[Android Studio](https://developer.android.com/studio/)

- Consider adding the CLI tools to your path:

```bash
PATH="$PATH:~/Library/Android/sdk/tools"
PATH="$PATH:~/Library/Android/sdk/tools/bin"
```

- Consider installing Android SDK Components and Platform Tools, Emulators (AVD Manager)

### Applications

[Node](https://nodejs.org/)
[nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
[asdf](https://asdf-vm.com)

```bash
brew install nvm
mkdir ~/.nvm
echo """
export NVM_DIR="$HOME/.nvm"
  . "/usr/local/opt/nvm/nvm.sh"
""" >> ~/.zshrc

source ~/.zshrc

nvm install node
nvm install 'lts/*' --reinstall-packages-from=current
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

### Orchestration

- Kubernetes

[kubectl](https://kubernetes.io/)
```bash
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/darwin/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```

[minikube](https://github.com/kubernetes/minikube/)
```bash
curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.25.2/minikube-darwin-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```

[helm](https://helm.sh/)
```bash
brew install kubernetes-helm
```

# Blockchain

[Ganache](https://truffleframework.com/ganache/)

[Truffle JS](https://truffleframework.com/)
```
npm i -g truffle
```
[web3.js](https://github.com/ethereum/web3.js/)

## Credits

- Image (https://png.icons8.com)
