# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "fedora/38-cloud-base"

  config.vm.provider :libvirt do |domain|
    domain.cpus = 1
    domain.memory = 2048
  end

  config.vm.provision "ansible" do |ansible|
    ansible.galaxy_command = 'ansible-galaxy install -r requirements.yml'
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end

end
