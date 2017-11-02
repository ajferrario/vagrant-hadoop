# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.define "primary_name" do |primary_name|
    primary_name.vm.provider "virtualbox" do |vb|
      vb.name = "primary_name"
      vb.memory = "2048"
    end
    #primary_name.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #end
    primary_name.vm.box = "ubuntu/xenial64"
    primary_name.vm.network "private_network", ip: 192.168.33.10
  end
  
  config.vm.define "data_1" do |data_1|
    data_1.vm.provider "virtualbox" do |vb|
      vb.name = "data_1"
      vb.memory = "1024"
    end
    #data_1.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #end
    data_1.vm.box = "ubuntu/xenial64"
    data_1.vm.network "private_network", ip: 192.168.33.20
  end
  
  config.vm.define "data_2" do |data_2|
    data_2.vm.provider "virtualbox" do |vb|
      vb.name = "data_2"
      vb.memory = "1024"
    end
    #data_2.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "playbook.yml"
    #end
    data_2.vm.box = "ubuntu/xenial64"
    data_2.vm.network "private_network", ip: 192.168.33.30
  end
end
