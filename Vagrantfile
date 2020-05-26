Vagrant.configure(2) do |config|
	config.vm.box = "debian/buster64"
	config.vm.provider "virtualbox" do |v|
		v.memory = 4000
		v.cpus = 2
		v.gui = false
	end
	config.vm.provision :shell,
	inline: <<-END
		mkdir -p /home/vagrant/.ssh
		chown -R vagrant:vagrant /home/vagrant/.ssh
		cat /vagrant/ssh_key.pub >> /home/vagrant/.ssh/authorized_keys
  	END
end
