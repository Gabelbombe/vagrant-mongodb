# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant::Config.run do | config |
  config.vm.hostname = "mongod.io"
  config.vm.box      = "hashicorp/precise64"

  # config.vm.network "33.33.33.10"

  #TODO: WILL NOT RUN UNDER CONFIG 2
  config.vm.forward_port 27017, 27018

  config.vm.provision :puppet do | puppet |
    puppet.manifests_path = "manifests"
    puppet.manifest_file  = "init.pp"
    puppet.module_path    = "modules"
  end
end
