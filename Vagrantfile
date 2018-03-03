Vagrant.configure("2") do |config|
  config.vm.box = "bkenro/centos7dsm"
  config.vm.box_version = "0.1.0"
  config.vm.network "private_network", ip: "192.168.12.34"
  config.vm.hostname = "centos7dsm.local"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "vm-centos7dsm-0.1.0"
    vb.customize ["modifyvm", :id, "--memory", "2048"]
  end
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.synced_folder "vagrant/", "/vagrant", type: "virtualbox", mount_options: ['dmode=777','fmode=777']
  config.vm.synced_folder "pj/", "/var/www/pj", type: "virtualbox", mount_options: ['dmode=777','fmode=777']
end
