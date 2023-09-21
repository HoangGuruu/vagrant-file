Vagrant.configure("2") do |config|
    config.hostmanager.enabled = true 
    config.hostmanager.manage_host = true
    
  ### CP0  ####
    config.vm.define "cp0" do |cp0|
      cp0.vm.box = "ubuntu/focal64"
      cp0.vm.hostname = "cp0"
      cp0.vm.network "private_network", ip: "66.152.182.12"
      cp0.vm.provider "virtualbox" do |vb|
       vb.memory = "600"
     end
    end
    
  ### WOKER-1 ###
     config.vm.define "w01" do |w01|
      w01.vm.box = "ubuntu/focal64"
      w01.vm.hostname = "w01"
      w01.vm.network "private_network", ip: "66.152.182.13"
      w01.vm.provider "virtualbox" do |vb|
       vb.memory = "800"
     end
     end
  ### WOKER-1 ###
  config.vm.define "host" do |host|
    host.vm.box = "ubuntu/focal64"
    host.vm.hostname = "host"
    host.vm.network "private_network", ip: "66.152.182.14"
    host.vm.provider "virtualbox" do |vb|
     vb.memory = "800"
   end
   end   
    
  ### Vmext VM ###
    config.vm.define "vmext" do |vmext|
        vmext.vm.box = "ubuntu/focal64"
      vmext.vm.hostname = "vmext"
    vmext.vm.network "private_network", ip: "66.152.182.11"
    vmext.vm.network "forwarded_port", guest: 10443, host: 10443
    vmext.vm.network "forwarded_port", guest: 11443, host: 11443
    vmext.vm.network "forwarded_port", guest: 12443, host: 12443
    vmext.vm.provider "virtualbox" do |vb|
       vb.gui = true
       vb.memory = "800"
     end
  end
    
  end