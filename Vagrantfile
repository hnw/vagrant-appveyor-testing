# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |c|
  c.vm.box = "sensu/freebsd-10.3-i386"
  c.vm.box_version = "2.1.20161031004532"
  c.vm.synced_folder ".", "/vagrant", disabled: true
  c.vm.boot_timeout = 1800

  c.vm.provider :virtualbox do |p|
    p.customize ["modifyvm", :id, "--nictype1", "Am79C973"]
    p.customize ["modifyvm", :id, "--memory", "512"]
    p.gui = true
  end
end
