Vagrant.configure("2") do |config|
  config.vm.box = "bkenro/centos7dsm"
  config.vm.network "private_network", ip: "192.168.12.34"
  config.vm.hostname = "centos7dsm.local"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "vm-centos7dsm-0.2.0"
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.synced_folder "vagrant/", "/vagrant", type: "virtualbox", mount_options: ['dmode=777','fmode=777']
  config.vm.provision "shell", inline: <<-SHELL
    ln -s /vagrant/bin /home/vagrant/
    ln -s /var/www/html /home/vagrant/
    chown vagrant:vagrant /var/www
  SHELL
end