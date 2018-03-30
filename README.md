# How to run re-create docker image

**mvn clean package docker:build**

# To run image

## Create network

**docker network create ms-net**

## Run image

**docker run
  -p 8761:8761
  --name ms-eureka
  --network ms-net
  tesei7/ms-eureka**