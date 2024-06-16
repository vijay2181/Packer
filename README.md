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

- dont use instance.json file, it is supported for older version of packer

packer init instance.json

```
Error: Packer plugins currently only works with HCL2 configuration templates
Please manually install plugins with the plugins command or use a HCL2
configuration that will do that for you.
```

```
ls
packer.pkr.hcl  userdata.sh instance.json

packer init packer.pkr.hcl
packer validate packer.pkr.hcl
packer build packer.pkr.hcl
```
