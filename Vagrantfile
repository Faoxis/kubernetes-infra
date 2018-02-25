Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  N = 3

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant-playbook.yml"
  end

  (1..N).each do |i|
	config.vm.define "ubuntu#{i}" do |node|
		node.vm.network "private_network", ip: "55.55.55.#{i}"
	end
  end

end


