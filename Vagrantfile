# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.synced_folder "/Users/wagnerjgoncalves/projects", "/projects", nfs: true
  config.vm.hostname = "absolut"

  config.vm.network :forwarded_port, guest: 3000, host: 3000
  config.vm.network :private_network, ip: "192.168.0.133"

  config.vm.define "absolut" do |absolut|
  end

  config.vm.provider "virtualbox" do |vb|
    vb.name = "absolut"
    vb.memory = 2048
    vb.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "recepies/development.yml"
  end
end
