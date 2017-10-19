Vagrant.configure(2) do |config|
	config.vm.synced_folder ".", "/vagrant", disabled: true

	config.vm.define "logserver" do |logserver|
		logserver.vm.box = "ubuntu/xenial64"
		logserver.vm.network "private_network", ip: "192.168.80.3"
		logserver.vm.provider "virtualbox" do |v|
  			v.memory = 3048
  			v.cpus = 3
		end
	end

	config.vm.define "loadbalancer" do |loadbalancer|
		loadbalancer.vm.box = "ubuntu/xenial64"
		loadbalancer.vm.network "private_network", ip: "192.168.80.4"
	end

end
