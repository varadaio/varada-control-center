# Varada Control Center

In order to start working with the varada control center and spinning up varada clusters please follow the steps below

 - [Setup](#setup)
 - [Configure](#Configure)
 - [Run](#Run)
---

## Setup

First you'll need to have a machine with both docker and docker-compose.

Get both of them by running the 
following commands

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

Open the `docker-compose.yaml` file and change the next place holders to fit your environment

- S3-PATH - valid s3 path to save cluster metadata
- AWS-REGION - current aws region
- CLUSTER-MANAGER-SCHEMA - unique name for cluster manager schema at glue or hive metasotre

---
## Run

In the same folder as the `docker-compose.yaml` file run the next line
```
docker-compose up -d
```
