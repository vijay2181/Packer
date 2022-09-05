# Packer

install packer
---------------
cd /opt

sudo yum update -y

sudo wget https://releases.hashicorp.com/packer/1.4.2/packer_1.4.2_linux_amd64.zip

sudo unzip packer_1.4.2_linux_amd64.zip

sudo mv packer /usr/local/bin/

packer --version
