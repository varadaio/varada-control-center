# Varada Control Center
To start working with the Varada Control Center and spinning up Varada clusters, complete the following steps:
 - [Setup](#set-up)
 - [Configure](#Configure)
 - [Run](#Run)
---
## Set Up
First you'll need a machine with both docker and docker-compose.
Get them both by running the following commands:
```
# install docker
sudo amazon-linux-extras install docker -y
sudo service docker start
sudo usermod -a -G docker ec2-user
# install docker-compose
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose
sudo chmod +x /usr/bin/docker-compose
```
---
## Configure
```
curl https://raw.githubusercontent.com/varadaio/varada-control-center/main/docker-compose.yml > docker-compose.yml
```
---
## Run
In the same folder as the `docker-compose.yaml` file run the following command:
```
sudo docker-compose up -d
```
