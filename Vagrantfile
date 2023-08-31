
# Apenas testando o Vagrant
# Vagrant.configure("2") do |config|
#   config.vm.box = "ubuntu/bionic64"  # Imagem da máquina virtual
#   config.vm.network "private_network", type: "dhcp"  # Configuração de rede
#   config.vm.provider "virtualbox" do |vb|  # Configurações do VirtualBox
#     vb.memory = "1024"  # Quantidade de memória RAM
#     vb.cpus = 2  # Número de CPUs
#   end
# end

# Iniciando a máquina virtual - servidor web com Nginx
# Vagrant.configure("2") do |config|
#   config.vm.box = "ubuntu/bionic64"
#   config.vm.network "forwarded_port", guest: 80, host: 8080

#   config.vm.provision "shell", inline: <<-SHELL
#     sudo apt-get update
#     sudo apt-get install -y nginx
#   SHELL
# end

# DESAFIO
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y apache2 htop nano python3
    sudo mkdir /home/vagrant/dir-compartilhado
  SHELL

  # config.vm.synced_folder "/home/mogleson/Área de Trabalho/iTalent/Atividades/vagrant/projeto-01", "./dir-compartilhado"

  config.vm.network "private_network", type: "dhcp"
  config.vm.network "public_network", ip: "192.168.0.3"
  config.vm.network "public_network", ip: "10.10.1.100"

end

