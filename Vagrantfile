# -*- mode: ruby -*-
# vi: set ft=ruby :

#bootstrap = <<SCRIPT
#  useradd -m chris --groups sudo
#  su -c "printf 'cd /home/chris\nsudo su chris' >> .bash_profile" -s /bin/sh vagrant
#SCRIPT

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
   Vagrant.configure("2") do |config|
     config.vm.box = "bento/ubuntu-18.04"

     config.vm.synced_folder "scripts", "/home/vagrant/scripts"
     config.vm.synced_folder "data", "/home/vagrant/data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
    config.vm.provider "virtualbox" do |vb|
     vb.cpus = "2"
     vb.memory = "2048"
   end
   config.vm.host_name = "blue"
  #
  # Please see the
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y tcl8.6 zip
     ln -s /usr/bin/tclsh8.6 /usr/bin/tclsh
     apt-get install -y environment-modules
#     git clone  https://github.com/chrisbpawsey/maali-1.5.git
     wget http://swcarpentry.github.io/shell-novice/data/data-shell.zip
     unzip data-shell.zip
     rm data-shell.zip
     chown -R vagrant:vagrant data-shell
#     chown -R vagrant:vagrant maali-1.5
#    cd maali-1.5
#    sudo -H -u vagrant bash -c ./install_scripts/Install_maali_vagrant.sh
#     echo "module path variable is $MODULEPATH"

#    sudo -H -u vagrant bash -c './maali -t maali -v 1.5h -c vagrant -d'
#     sudo -H -u vagrant bash -c 'source ~/.bashrc'

   SHELL

end
