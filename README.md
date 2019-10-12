# SXI LLC EXCHANGE SCRIPT

> Buy now $499 https://sxi.io/members/cart.php?gid=17

## Getting started
```
groupadd app
useradd -d /home/app -s `which bash` -g app -m app
apt update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu xenial stable"
sudo apt-get update
apt update
apt install docker-ce
usermod -aG docker app
curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```
```
vim /etc/sudoers
root ALL=(ALL:ALL)ALL
app ALL=(ALL:ALL)ALL
```
```
git clone https://github.com/sxiio/exchange.git
cd exchange
```
### Install ruby with rvm

```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
curl -sSL https://get.rvm.io | bash -s stable --ruby=2.6.0 --gems=rails

source /home/app/.rvm/scripts/rvm
rvm use 2.6.0
```

### Bundle install depedencies

```
bundle
rake -T
```

### Run everything

```
rake service:all
```

Insert in file `/etc/hosts`
```
0.0.0.0 www.app.local
0.0.0.0 monitor.app.local
```

You can login on `www.app.local` with the following default users from seeds.yaml
```
Seeded users:
Email: admin@barong.io, password: 0lDHd9ufs9t@
Email: john@barong.io, password: Am8icnzEI3d!
```

