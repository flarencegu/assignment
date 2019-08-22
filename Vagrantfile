# -*- mode: ruby -*- 
# vi: set ft=ruby : 
#Every Vagrant development environment requires a box. You can search for 
# boxes at https://atlas.hashicorp.com/search.
 
 Vagrant.configure(2) do |config|
	# Specifying the box we wish to use
	BOX_IMAGE = "centos/7"
	config.vm.box = BOX_IMAGE
	# Adding Bridged Network Adapter
	config.vm.network "public_network"
	# Iterating the loop for three times
	(1..3).each do |i|
		# Defining VM properties
		config.vm.define "vagrant_vm#{i}" do |node|
			# Specifying the provider as VirtualBox and naming the VM's
			config.vm.provider "virtualbox" do |node|
				# The VM will be named as edureka_vm{i}
				node.name = "vagrant_vm#{i}"  
				
				config.vm.box_check_update = true
				Vagrant.configure("2") do |config|
  config.vm.usable_port_range = 8000..8999
end
Vagrant.configure("2") do |config|
  config.vm.network "forwarded_port", guest: 80, host: 8080,
    auto_correct: true
end
   config.vm.network "private_network", ip: "192.168.33.#{i+10}"
      config.vm.provider "virtualbox" do |vb|
   vb.gui = true
   vb.memory = "2048"
			end
		end
	end
end
end

