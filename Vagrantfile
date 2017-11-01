# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.define "primary_name" do |primary_name|
    primary_name.vm.provider "virtualbox" do |vb|
      vb.name = "primary_name"
      vb.gui = true
      vb.memory = "2048"
    end
    primary_name.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
    primary_name.vm.box = "ubuntu/xenial64"
    primary_name.vm.network "private_network", ip: "192.168.50.0"
  end
  
  config.vm.define "data_1" do |data_1|
    data_1.vm.provider "virtualbox" do |vb|
      vb.name = "data_1"
      vb.gui = true
      vb.memory = "1024"
    end
    data_1.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
    data_1.vm.box = "ubuntu/xenial64"
    data_1.vm.network "private_network", ip: "192.168.50.10"
  end
  
  config.vm.define "data_2" do |data_2|
    data_2.vm.provider "virtualbox" do |vb|
      vb.name = "data_2"
      vb.gui = true
      vb.memory = "1024"
    end
    data_2.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
    data_2.vm.box = "ubuntu/xenial64"
    data_2.vm.network "private_network", ip: "192.168.50.11"
  end


  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
