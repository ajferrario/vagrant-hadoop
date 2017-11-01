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

`mkdir vagrant_project
cd vagrant_project
vagrant init`
- install git

`sudo apt install git`
- clone the repo

`git clone https://github.com/ajferrario/vagrant-hadoop.git`
- replace Vagrantfile with repo

`cp -f vagrant-hadoop/Vagrantfile Vagrantfile`
- clean up repository

`rm -r -f vagrant-hadoop`

