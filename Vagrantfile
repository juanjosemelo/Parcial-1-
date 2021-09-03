Vagrant.configure("2") do |config|
	config.vm.define :cliente do|cliente|
		cliente.vm.box = "bento/centos-7.9"
  		cliente.vm.box = "juanj/vm_test_cliente"
  		cliente.vm.box_version = "0.0.2"
		cliente.vm.network :private_network, ip: "192.168.50.6"
		cliente.vm.hostname ="cliente"
	end 
	config.vm.define :servidor do|servidor|
		servidor.vm.box = "bento/centos-7.9"
  		servidor.vm.box = "juanj/vm_test_servidor"
  		servidor.vm.box_version = "0.0.2"
		servidor.vm.network :private_network, ip: "192.168.50.7", virtualbox__intnet: "lan1"
		servidor.vm.hostname ="servidor"
		servidor.vm.network "forwarded_port", guest: 80, host: 8080
	end 
end