
Vagrant.configure("2") do |c|
  c.vm.box = "chef/ubuntu-12.04-i386"
  c.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_ubuntu-12.04_chef-provisionerless.box"
  c.vm.hostname = "default-ubuntu-1204.vagrantup.com"
  c.vm.synced_folder ".", "/vagrant", disabled: true
  c.vm.provider :virtualbox do |p|
  end
end
