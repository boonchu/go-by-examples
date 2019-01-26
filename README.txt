##### Go

##### VG
I use vg as a tool set to setup virtual env.
https://github.com/GetStream/vg

##### Download and install GO.

wget https://dl.google.com/go/go1.11.2.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.11.2.linux-amd64.tar.gz

##### VG Installation.
mkdir ~/go/{bin,src}
export GOPATH=~/go
export PATH=~/go/bin:$PATH
go get -u github.com/GetStream/vg
command -v vg >/dev/null 2>&1 && eval "$(vg eval --shell bash)"

##### Configure VG environment.
vg setup

##### Full isolation mode

$ vg init --full-isolation rest-api
(rest-api) $ vg destroy rest-api
Destroying workspace "rest-api"
Deactivating rest-api
$ vg activate rest-api --full-isolation 
