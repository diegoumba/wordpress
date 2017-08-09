# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "vvv"
    ansible.sudo = "true"
    ansible.playbook = "provisioning/playbook.yml"
  end

  config.vm.define "vmwordpress" do |vmwordpress|
    config.vm.network "private_network", type: "dhcp"
    vmwordpress.vm.hostname = "vmwordpress"
  end
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

end
