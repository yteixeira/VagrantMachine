#required_plugins = %w( vagrant-hostsupdater )
#required_plugins.each do |plugin|
#  system "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin

#end

# Vagrant.configure("2") do |config|
#   config.vm.box = "ubuntu/xenial64"
#   config.vm.network "private_network", ip: "192.168.10.100"
#   config.hostsupdater.aliases = ["developer.local"]

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.100.10" #defines the ip address of the connection
  config.vm.synced_folder "app", "/home/vagrant/app" #makes a copy of the app folder inside the virtual machine
  config.vm.provision "shell", path: "environment/provision.sh" #runs the provision.sh file on start up

end
