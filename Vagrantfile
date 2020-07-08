# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "frontend" do |frontend|
    frontend.vm.box = "ubuntu/bionic64"
    frontend.vm.network "private_network", ip: "10.0.0.10"
      ansible.playbook = "playbook_frontend.yml"
      ansible.sudo = true
  end

  config.vm.define "backend" do |backend|
    backend.vm.box = "ubuntu/bionic64"
    backend.vm.network "private_network", ip: "10.0.0.20"
      ansible.playbook = "playbook__frontend.yml"
      ansible.sudo = true
  end

  config.vm.define "database" do |database|
    database.vm.box = "ubuntu/bionic64"
    database.vm.network "private_network", ip: "10.0.0.30"
      ansible.playbook = "playbook__database.yml"
      ansible.sudo = true
  end
end
