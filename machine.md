# Docker Machine

## Create a docker machine using hyperv driver

$ docker-machine create --driver hyperv docker-local

## Configure local docker client to docker machine

In this case the local machine is named docker-local

At the end this will give you a command to run to configure your
shell

$ docker-machine env docker-local

## Connect to the docker local machine with SSH

$ docker-machine ssh docker-local

## If failure happen 

I currently work around the problem by:

After the failure, running "docker-machine start [machinename]"
Wait for the machine to start fully
Running "docker-machine regenerate-certs [machinename]"