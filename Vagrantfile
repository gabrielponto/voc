# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev git default-jre default-jdk ant python3.4 python3.4-venv
	curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer |bash
	echo "export PATH=\"\$HOME/.pyenv/bin:\$PATH\"" >> /root/.bashrc
	echo "eval \"\$(pyenv init -)\"" >> /root/.bashrc
	echo "eval \"\$(pyenv virtualenv-init -)\"" >> /root/.bashrc
  SHELL
end
