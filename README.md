# vagrant-hadoop
- Set up Ubuntu VM (64 bit, 4 core, 8gb ram, 100gb storage)
- Install pip

`sudo apt-install pip`
- Install ansible

`pip install ansible`
- Install virtualbox

`sudo apt-get install virtualbox`
- Install vagrant

`sudo apt-get install vagrant`
- Install dkms to make sure virtualbox host kernels are ok if we upgrade linux

`sudo apt-get install virtualbox-dkms`
- Get ubuntu box

`vagrant box add ubuntu/xenial64`
- Create Vagrant folder and initialize project

```
mkdir vagrant_project
cd vagrant_project
vagrant init
```
- install git

`sudo apt install git`
- clone the repo

`git clone https://github.com/ajferrario/vagrant-hadoop.git`
- replace Vagrantfile with repo

`cp -f vagrant-hadoop/Vagrantfile Vagrantfile`
- clean up repository

`rm -r -f vagrant-hadoop`
- launch cluster

`vagrant up`

Full script
```
sudo apt-install pip
pip install ansible
sudo apt-get install virtualbox
sudo apt-get install vagrant
sudo apt-get install virtualbox-dkms
vagrant box add ubuntu/xenial64
mkdir vagrant_project
cd vagrant_project
vagrant init
sudo apt install git
git clone https://github.com/ajferrario/vagrant-hadoop.git
cp -f vagrant-hadoop/Vagrantfile Vagrantfile
rm -r -f vagrant-hadoop
vagrant up

```
