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
Open the `docker-compose.yaml` file and change the following place holders to fit your environment:
- S3-PATH: A valid S3 path to save cluster metadata.
- AWS-REGION: Your current AWS region.
- CLUSTER-MANAGER-SCHEMA: A unique name for the cluster manager schema in the Glue or Hive metastore
---
## Run
In the same folder as the `docker-compose.yaml` file run the following command:
```
docker-compose up -d
```
