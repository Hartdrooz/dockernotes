#Docker usefull command

## Get version

$ docker version

## Get info about container environment

This allow to see how many containers run
in our environment and more

$ docker info

## Get list of all installed images

$ docker images

## See all the running containers

$ docker ps

## See all previous running container

$ docker ps -a

## Get an image of the docker repository

$ docker pull <image_name>

## Download specific verion of a docker image

$ docker pull ubuntu:14.0.4

## Download example container 

This will try to run the container called
hello-world, because this container is not
present in the machine it will get it from
the docker public repository.

This container will just print fast an hello-world

$ docker run hello-world

