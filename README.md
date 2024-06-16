# Packer

install packer
---------------
cd /opt

sudo yum update -y

sudo yum install jq -y

LATEST_VERSION=$(curl -s https://checkpoint-api.hashicorp.com/v1/check/packer | jq -r .current_version)

wget https://releases.hashicorp.com/packer/${LATEST_VERSION}/packer_${LATEST_VERSION}_linux_amd64.zip

unzip packer_${LATEST_VERSION}_linux_amd64.zip

sudo mv packer /usr/local/bin/

packer --version
