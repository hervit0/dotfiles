# Ubuntu Installation Flight Sheet

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

### Java

```
sudo add-apt-repository ppa:linuxuprising/java
sudo apt-get update
sudo apt-get install oracle-java11-installer
sudo apt-get install oracle-java11-set-default
java --version
```

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

### Z plugin

- https://github.com/rupa/z

### zsh-syntax-highlighting

- https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md

### Misc linux

- https://askubuntu.com/questions/406204/how-can-i-add-the-current-cpu-usage-to-my-menu-bar-as-a-percentage
