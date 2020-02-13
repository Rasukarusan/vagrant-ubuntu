Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04-i386"
  config.vm.box_version = "202002.04.0"
  config.vm.network :private_network, ip: "192.168.56.101"
  config.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "playbook.yml"
  end
end
