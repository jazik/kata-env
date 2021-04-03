# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "fedora/33-cloud-base"

  memory = 4096
  cpus = 1
  config.vm.provider :libvirt do |v|
    v.memory = memory
    v.cpus = cpus
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision.yml"
    ansible.verbose = "v"
  end

end
