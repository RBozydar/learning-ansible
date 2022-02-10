# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"

  config.ssh.insert_key = false

  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.linked_clone = true
    v.cpus = 1
  end

  # App Server 1
  config.vm.define :alpha do |alpha|
    alpha.vm.hostname = "alpha.test"
    alpha.vm.network "private_network", ip: "192.168.60.4"
  end

  # # App Server 2
  # config.vm.define :beta do |beta|
  #   beta.vm.hostname = "orc-app2.test"
  #   beta.vm.network "private_network", ip: "192.168.60.5"
  # end

end
