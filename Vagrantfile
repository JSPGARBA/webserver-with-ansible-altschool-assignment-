Vagrant.configure("2") do |config|
  config.vm.define "ubuntu_node" do |ubuntu|
    ubuntu.vm.box = "ubuntu/bionic64"
    ubuntu.vm.network "private_network", type: "dhcp"
    ubuntu.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end

  config.vm.define "centos_node" do |centos|
    centos.vm.box = "centos/7"
    centos.vm.network "private_network", type: "dhcp"
    centos.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end

  config.vm.define "kali_node" do |kali|
    kali.vm.box = "kalilinux/rolling"
    kali.vm.network "private_network", type: "dhcp"
    kali.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
end
