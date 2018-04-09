# How to run re-create docker image

**mvn clean package docker:build**

# To run image

## Create network

**docker network create ms-net**

## Run logspout

**docker run --name="logspout" --volume=/var/run/docker.sock:/var/run/docker.sock gliderlabs/logspout syslog+tls://logs4.papertrailapp.com:54713**

## Run image

**docker run -p 8761:8761 --name ms-eureka --network ms-net tesei7/ms-eureka**
  