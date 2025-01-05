Vagrant.configure("2") do |config|

    config.vm.define "gpt-server" do |cfg|
    cfg.vm.box = "bento/ubuntu-20.04"
	
	cfg.vm.provider "virtualbox" do |vb|
	  vb.name = "gpt-server"
 	  vb.gui = true
      vb.cpus = "1"
      vb.memory = "2048"
    end
	cfg.vm.host_name = "gpt-server"
    cfg.vm.network "private_network", ip: "192.168.1.20"
    cfg.vm.network "forwarded_port", guest: 22, host: 60020, auto_correct: true, id: "ssh"
    cfg.vm.provision "shell", inline: "apt-get update"
	
  end

end