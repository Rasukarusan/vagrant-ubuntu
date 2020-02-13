Vagrant.configure("2") do |config|
    config.vm.define "32bit" do |ubuntu|
        ubuntu.vm.box = "bento/ubuntu-16.04-i386"
        ubuntu.vm.box_version = "202002.04.0"
        ubuntu.vm.network :private_network, ip: "192.168.56.101"
        config.vm.provider :virtualbox do |v|
            v.customize [ "modifyvm", :id, "--memory", 512]
        end
        ubuntu.vm.provision "ansible_local" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "64bit" do |ubuntu|
        ubuntu.vm.box = "bento/ubuntu-18.04"
        ubuntu.vm.box_version = "202002.04.0"
        ubuntu.vm.network :private_network, ip: "192.168.56.102"
        config.vm.provider :virtualbox do |v|
            v.customize [ "modifyvm", :id, "--memory", 512]
        end
        ubuntu.vm.provision "ansible_local" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end
end
