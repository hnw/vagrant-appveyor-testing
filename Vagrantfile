# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |c|
  c.vm.box = "sensu/freebsd-11.0-i386"
  c.vm.box_version = "2.1.20161031055219"
  c.vm.synced_folder ".", "/vagrant", disabled: true
  c.vm.boot_timeout = 1800

  c.vm.provider :virtualbox do |p|
    p.customize ["modifyvm", :id, "--memory", "1024"]
    p.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
    p.customize ["modifyvm", :id, "--natdnshostresolver1", "off"]
    p.gui = true
  end
end
