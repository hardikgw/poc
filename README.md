# Docker images on Ubuntu 14.04 with Puppet, Ansible and Fabric

git clone https://github.com/hardikgw/poc.git

cd poc

## Puppet

cd puppet/server
docker build .
#### start container with port 8140 open
docker run -it -p 8140:8140 --name=puppet-server <image_id>

#### update /etc/hosts with correct ip addresses as below
127.0.0.1 thispuppet.com localhost puppet
::1 localhost ip6-localhost ip6-loopback
172.17.0.<<xx>> <<container-id>>
172.17.0.<<xx>> thispuppetclient.com puppetclient

#### start puppet server
service puppetserver start

#### start agents and update /etc/hosts of each client

cd puppet/agent
docekr build
docker run -it --name=puppet-agent <image_id>

#### update host file in running container /etc/hosts by adding server address
172.17.0.<<ip>> thispuppetserver.com puppetmaster puppet

#### start the agent
./usr/local/run.sh


## Ansible
cd ansible/server
docker build .

## Fabric
cd fabric/server
docker build .
