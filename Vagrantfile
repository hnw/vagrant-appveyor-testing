# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |c|
  c.vm.box = "freebsd-10.1-i386"
  c.vm.box_url = "http://iris.hosting.lv/freebsd-10.1-i386.box"
  c.vm.synced_folder ".", "/vagrant", disabled: true
  c.vm.boot_timeout = 1800

  c.vm.provider :virtualbox do |p|
    p.customize ["modifyvm", :id, "--nictype1", "Am79C973"]
    p.customize ["modifyvm", :id, "--memory", "512"]
    p.gui = true
  end
end
