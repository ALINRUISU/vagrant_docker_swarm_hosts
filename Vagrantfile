Vagrant.configure("2") do |config|
  config.vm.define "docker01", primary: true do |docker01|
    docker01.vm.box = "centos/7"
    docker01.vm.hostname = 'docker01'

    docker01.vm.network :public_network, ip: "192.168.0.101"

    docker01.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "docker01"]
    end
    config.vm.provision :shell, path: "bootstrap.sh"

  end

  config.vm.define "docker02" do |docker02|
    docker02.vm.box = "centos/7"
    docker02.vm.hostname = 'docker02'

    docker02.vm.network :public_network, ip: "192.168.0.102"

    docker02.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "docker02"]
    end
    config.vm.provision :shell, path: "bootstrap.sh"

  end

  config.vm.define "docker03" do |docker03|
    docker03.vm.box = "centos/7"
    docker03.vm.hostname = 'docker03'

    docker03.vm.network :public_network, ip: "192.168.0.103"

    docker03.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 2048]
      v.customize ["modifyvm", :id, "--name", "docker03"]
    end
    config.vm.provision :shell, path: "bootstrap.sh"

  end

end