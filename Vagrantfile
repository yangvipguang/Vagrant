# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
(1..3).each  do |i|
	config.vm.define "node#{i}" do |node|
  	node.vm.box = "ubuntu/xenial64"
	node.vm.hostname="node#{i}"
 	node.vm.network "private_network", type: "dhcp" 
	node.vm.synced_folder "/opt", "/vagrant"
	node.vm.provider "virutalbox" do |v|
		v.name = "node#{i}"
		v.memory = 1024
		v.cpus=2
	end
	end
end
end
