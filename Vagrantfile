# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|

  # Ensure we use our vagrant private key
  config.ssh.insert_key = false
  config.ssh.private_key_path = '~/.vagrant.d/insecure_private_key'

  config.vm.define 'ansible-db-restore' do |machine|
    machine.vm.box = "bento/ubuntu-16.04"
    # machine.vm.box = "ubuntu/trusty64"
    #machine.vm.box = "ubuntu/precise64"
    #machine.vm.box = "debian/jessie64"
    #machine.vm.box = "debian/wheezy64"
    #machine.vm.box = "chef/centos-7.1"
    #machine.vm.box = "chef/centos-6.6"

    machine.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--cpuexecutioncap", 55]
      v.customize ["modifyvm", :id, "--memory", 512]
    end

    machine.vm.network :forwarded_port, guest: 5432, host: 55432 # PostgreSQL port
    machine.vm.network :private_network, ip: '10.110.0.10'

    machine.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'tests/playbooks/vagrant.yml'
      ansible.sudo = true
      ansible.inventory_path = 'tests/inventory/test'
      ansible.host_key_checking = false
      ansible.limit = "vagrant"
    end
  end
end