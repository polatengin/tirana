# Install gRPC CLI on Ubuntu

Here is the guideline to install [gRPC CLI](https://github.com/grpc/grpc) on _Ubuntu_

_PS_ : I am using WSL 2 on my machine, below guideline is working on WSL 2, as well

```bash
sudo -s
apt update
apt install linuxbrew-wrapper
exit
brew
sudo -s
apt-get install build-essential
echo 'export PATH="~/.linuxbrew/bin:$PATH"' >>~/.bash_profile
echo 'export MANPATH="~/.linuxbrew/share/man:$MANPATH"' >>~/.bash_profile
echo 'export INFOPATH="~/.linuxbrew/share/info:$INFOPATH"' >>~/.bash_profile

PATH="~/.linuxbrew/bin:$PATH"
exit
brew install gcc

brew install grpc
cd ~/.linuxbrew/Cellar/grpc/1.28.1/bin

./grpc_cli
PATH="~/.linuxbrew/Cellar/grpc/1.28.1/bin:$PATH"
grpc_cli
```
