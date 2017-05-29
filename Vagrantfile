# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |c|
  #c.vm.box = "ubuntu/precise32"
  c.vm.box = "ubuntu/trusty32"
  #c.vm.box = "chef/ubuntu-14.04-i386"
  #c.vm.box_url = "https://atlas.hashicorp.com/ubuntu/boxes/precise32/versions/12.04.4/providers/virtualbox.box"
  c.vm.box_url = "https://atlas.hashicorp.com/ubuntu/boxes/trusty32/versions/14.04/providers/virtualbox.box"
  #c.vm.box_url = "https://atlas.hashicorp.com/chef/boxes/ubuntu-14.04-i386/versions/1.0.0/providers/virtualbox.box"
  c.vm.synced_folder ".", "/vagrant", disabled: true
  c.vm.boot_timeout = 1800

  c.vm.provider :virtualbox do |p|
    p.customize ["modifyvm", :id, "--nictype1", "Am79C973"]
    
    # Minimum memory - Observed working on 5/30/2017
    # => https://ci.appveyor.com/project/b-long/vagrant-appveyor-testing/build/22-master 
    # p.customize ["modifyvm", :id, "--memory", "128"]
    
    p.customize ["modifyvm", :id, "--memory", "512"]

    p.gui = true
  end
end
