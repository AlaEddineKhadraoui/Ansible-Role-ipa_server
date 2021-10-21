# -*- mode: ruby -*-
# vi: set ft=ruby :

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
     libvirt.storage :file, :device => :cdrom, :path => '/home/alaa/data-store/CentOS-7-x86_64-DVD-1708.iso'
  end

  
  #Ansible configuration
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "test_ipa_server.yml"

  end  




end
