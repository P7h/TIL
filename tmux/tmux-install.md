## tmux installation steps on Ubuntu

### tmux v2.x installation -- Ubuntu 14.04 (Trusty Tahr)
```shell
tmux -V
sudo apt-get update
sudo apt-get install -y python-software-properties software-properties-common
sudo add-apt-repository -y ppa:pi-rho/dev
sudo apt-get update
sudo apt-get install -y tmux
tmux -V
```

### tmux v1.9 installation -- Ubuntu 14.04 (Trusty Tahr)
```shell
tmux -V
sudo apt-get update
sudo apt-get install -y python-software-properties software-properties-common
sudo add-apt-repository -y ppa:pi-rho/dev
sudo apt-get update
sudo apt-get install -y tmux=1.9a-1~ppa1~t
tmux -V
```

> On Ubuntu 12.04 (Precise Pangolin), step 6 would be: `sudo apt-get install -y tmux=1.9a-1~ppa1~p`

> On Ubuntu 13.10 (Saucy Salamander), step 6 would be: `sudo apt-get install -y tmux=1.9a-1~ppa1~s`
