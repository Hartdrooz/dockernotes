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

## Remove specific image from local store

$ docker rmi <imageid>

## Start container

$ docker start <container>

## Stop container

$ docker stop <container>

## Remove container

$ docker rm <container>

## Run with more command

**-d** This will run the container in the background mode

**--name** Give a name to the container when it run

**-p** Map some network port to the container

[a link](https://firebasestorage.googleapis.com/v0/b/pictures-dc7c3.appspot.com/o/dockerimg1.png?alt=media&token=dc6e550a-2c87-4ad0-ab3e-eee0826d7bc3)

$ docker run -d --name web -p 80:8080

## Download example container 

This will try to run the container called
hello-world, because this container is not
present in the machine it will get it from
the docker public repository.

This container will just print fast an hello-world

$ docker run hello-world

