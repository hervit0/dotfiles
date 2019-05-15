# Dotfiles

Classic with fries, please!

Jeez, why is it encrypted?! Well, every secret needs to be hidden `¯\_(ツ)_/¯`.

## Encryption technologies

[Git-crypt](https://github.com/AGWA/git-crypt)

Cheat sheet:
```
git-crypt init
git-crypt status
git-crypt lock
git-crypt unlock
```

```
gpg --list-keys
gpg --list-secret-keys
```

## VSCode stuff

Copy local config to this repo:
```
./vscode/save_local_config
```

Install extensions from this repo (`vscode/extensions.json`) to local machine
```
./vscode/install_extensions
```

## Dotfiles stuff

Save local config to this repo:
```
./save/bash_profile
./save/gitconfig
./save/vimrc
```

## Install ZSH and Z terminal plugins

[Follow these steps.](https://jilles.me/badassify-your-terminal-and-shell/)

## Ubuntu Quick Start-Up

### Visual Studio Code:

Download Debian package: https://code.visualstudio.com/docs/setup/linux
```
sudo apt install ./code_1.29.1-1542309157_amd64.deb
```

### GPG

```
sudo apt-get install gnupg2
```

### Fsharp

```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
echo "deb https://download.mono-project.com/repo/ubuntu stable-bionic main" | sudo tee /etc/apt/sources.list.d/mono-official-stable.list
sudo apt update
sudo apt install mono-devel
sudo apt-get update
sudo apt-get install fsharp
```

### Dotnet Core

```
  131  sudo apt-key adv --keyserver packages.microsoft.com --recv-keys EB3E94ADBE1229CF\n\nsudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
  132  sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-bionic-prod bionic main" > /etc/apt/sources.list.d/dotnetdev.list'
  133  sudo apt-get update
  134  sudo apt-get install dotnet-sdk-2.1.105
```

### Java

```
sudo add-apt-repository ppa:linuxuprising/java
sudo apt-get update
sudo apt-get install oracle-java11-installer
sudo apt-get install oracle-java11-set-default
java --version
```

Set up intelliJ:
```bash
asdf where java
```
E.g. `/Users/h.ah-leung/.asdf/installs/java/openjdk-11.0.1`, then in IntelliJ > Project structure > Platform Settings > SDKs and fill with this path (no need to append any path).

### Scala

Download the binaries
Move the binaries
Add into `.zshrc` or `.bashrc`:
```
export SCALA_HOME="/usr/share/scala"
# And not that:
# export SCALA_HOME="/usr/share/scala/bin/scala"
export PATH="$PATH:$SCALA_HOME/bin"
```

### Spark

```
brew install hadoop
brew install zlib
asdf install python 3.7.3
asdf global python 3.7.3
```

Add to `.zshrc` (change py4j and spark veresion if needed):
```
# Using custom zlib - python 3 issue
# For compilers to find zlib you may need to set:
export LDFLAGS="-L/usr/local/opt/zlib/lib"
export CPPFLAGS="-I/usr/local/opt/zlib/include"
export LDFLAGS="${LDFLAGS} -L/usr/local/opt/zlib/lib"
export CPPFLAGS="${CPPFLAGS} -I/usr/local/opt/zlib/include"
# For pkg-config to find zlib you may need to set:
export PKG_CONFIG_PATH="${PKG_CONFIG_PATH} /usr/local/opt/zlib/lib/pkgconfig"

# Spark
export SPARK_HOME=/Users/h.ah-leung/.asdf/installs/spark/2.4.3
export PATH=$PATH:$SPARK_HOME/bin
export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/lib/py4j-0.10.7-src.zip:$PYTHONPATH
export PATH=$SPARK_HOME/python:$PATH
```

Hadoop issue (OS > High Sierra):
```
brew install hadoop
brew link hadoop
sudo mkdir /usr/local/sbin
sudo chown -R `whoami`:admin /usr/local/sbin
```

### Z plugin

- https://github.com/rupa/z

### zsh-syntax-highlighting

- https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md

### Misc linux

- https://askubuntu.com/questions/406204/how-can-i-add-the-current-cpu-usage-to-my-menu-bar-as-a-percentage
