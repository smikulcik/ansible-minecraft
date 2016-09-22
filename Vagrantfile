Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "ansible-minecraft"
  config.vm.network :private_network, ip: "192.168.0.5"
  config.vm.network "forwarded_port", guest: 25565, host: 25565
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "examples/site.yml"
  end
  config.vm.provider "virtualbox" do |vb|
    vb.memory=2048
	vb.cpus = 2
  end
end
