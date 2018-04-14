# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "CentOS7.1"
  config.vm.hostname = "vagrant"
  config.vm.network :private_network, ip: "192.168.33.11"
  config.ssh.insert_key = false
  config.ssh.forward_agent = true
  config.vm.synced_folder "src/", "/home/vagrant/src"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/playbook.yml"
  end  
end
