# -*- mode: ruby -*-
# vi: set ft=ruby :
iso_path = "/home/alaa/iso/CentOS-7-x86_64-DVD-1708.iso" 
# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.hostname = "server.centos.com"

  config.vm.provider :libvirt  do |libvirt|
      
     libvirt.cpus = 2
     libvirt.memory = 2048
     libvirt.storage :file, :device => :cdrom, :path => iso_path
  end

  
  #Ansible configuration
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "test_ipa_server.yml"

  end  




end
