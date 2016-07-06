# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define :web do |web|
    web.vm.box = "https://github.com/CommanderK5/packer-centos-template/releases/download/0.6.7/vagrant-centos-6.7.box"
    web.vm.network :private_network, ip: "192.168.33.10"
    web.vm.synced_folder "app", "/home/vagrant/app"
  end

  config.vm.provision :shell, path: "provision/install-ansible.sh"

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "provision/playbook.yml"
    ansible.install = true
    ansible.verbose = "vvv"
    ansible.limit = "all"
  end
end
