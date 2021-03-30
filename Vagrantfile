# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "vm_grupo1" do |vm_grupo1|
    vm_grupo1.vm.box = "bento/ubuntu-20.04"
    vm_grupo1.vm.hostname = "vmgrupo1"
    vm_grupo1.ssh.username = 'vagrant'
    vm_grupo1.ssh.password = 'vagrant'
    vm_grupo1.ssh.insert_key = 'true'
    vm_grupo1.vm.network :forwarded_port, guest: 80, host: 8080
    vm_grupo1.vm.network :private_network, ip: "192.168.33.11"
    vm_grupo1.vm.provider "virtualbox" do |vb|
      vb.name   = "vmgrupo1"
      vb.memory = "1024"
      vb.cpus   = "1"
      vb.gui    = true #entorno gráfico
    end     
    config.vm.provision :shell, path: "inicializar.sh"
  end 
end