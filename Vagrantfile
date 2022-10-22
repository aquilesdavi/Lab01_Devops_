Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "public_network"
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install vim
    apt-get install curl
    apt-get install telnet
    apt-get install unzip
    apt-get install wget
    apt-get install net-tools
    apt-get install htop
    apt-get install nmap
    apt-get install -y nginx-full
    hostnamectl set-hostname aquiles
    adduser -y aquiles
  SHELL
end
