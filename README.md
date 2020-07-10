# Install gRPC CLI on Ubuntu

Here is the guideline to install [gRPC CLI](https://github.com/grpc/grpc) on _Ubuntu_

_PS_ : I am using WSL 2 on my machine, below guideline is working on WSL 2, as well

* Start a new shell with super user privilages

```bash
sudo -s
```

* Update _apt_ lists

```bash
apt update
```

* Install [LinuxBrew](https://docs.brew.sh/Homebrew-on-Linux)

```bash
apt install linuxbrew-wrapper
```

* Go back to previous shell

```bash
exit
```

* Check if _brew_ is installed and running successfully

```bash
brew
```

* Start a new shell with super user privilages

```bash
sudo -s
```

* Install required tools

```bash
apt-get install build-essential
```

* Set `PATH`, `MANPATH` and `INFOPATH` environment variables to include _linuxbrew_

```bash
echo 'export PATH="~/.linuxbrew/bin:$PATH"' >>~/.bash_profile
echo 'export MANPATH="~/.linuxbrew/share/man:$MANPATH"' >>~/.bash_profile
echo 'export INFOPATH="~/.linuxbrew/share/info:$INFOPATH"' >>~/.bash_profile

PATH="~/.linuxbrew/bin:$PATH"
```

* Go back to previous shell

```bash
exit
```

* Install _gcc_ and _gRPC_ from _brew_

```bash
brew install gcc

brew install grpc
```

* Go to _gRPC_ folder and check if _grpc_cli_ is working

```bash
cd ~/.linuxbrew/Cellar/grpc/1.28.1/bin

./grpc_cli
```

* Set `PATH` environment variable to include _grpc_cli_

```bash
PATH="~/.linuxbrew/Cellar/grpc/1.28.1/bin:$PATH"
```

* Check if you can run _grpc_cli_ from any folder

```bash
grpc_cli
```

👏 Congratulations, you installed _grpc_cli_ on your computer and it's ready to use now
