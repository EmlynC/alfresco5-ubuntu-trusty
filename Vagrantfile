# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  # set the virtual machine box to Ubuntu 14.04 LTS.
  config.vm.box = "ubuntu/trusty64"

  # forward port 8080 to port 9090 on the host, this is so we can see Apache Tomcat
  # from the host
  config.vm.network "forwarded_port", guest: 8080, host: 9090

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", ip: "192.168.33.10"

  # Configure the Virtualbox
  config.vm.provider "virtualbox" do |vb|
    
    # Call the virtualmachine ubuntu-alfresco5
    vb.name = "ubuntu-alfresco5"

    # Alfresco asks for a minimum of 2GB RAM, 2048Mb and two cores
    vb.memory = 2048
    vb.cpus = 2
  end

end
