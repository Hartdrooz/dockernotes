#Docker usefull command

## Get help

$ docker help

$ docker <command> help

## Login to docker repo

To pull some images you need
to be logged on the docker repo

$ docker login

## Get version

$ docker version

## Get info about container environment

This allow to see how many containers run
in our environment and more

$ docker info

## Get list of all installed images

$ docker images ls

## Get the label of a specific image 

$ docker image inspect <IMAGE_ID>

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

## See all containers running

$ docker container ls

## Start container

$ docker start <container>

## Stop container

$ docker stop <container>

## Remove container

$ docker rm <container>

## Attach the open terminal to running container

Doing so if you use some console log or print 
they will be show in the terminal when you attach
you open terminal session to a running container

$ docker container attach <runningContainerName>

## See the log of the container

If a container use console.log or some stdout 
this command can consult the log file

$ docker container logs --tail 5 <runningContainerName>

This command will see the log in real time

$ docker container logs -f <runningContainerName>

## Run with more command

**-d** This will run the container in the background mode

**--name** Give a name to the container when it run

**-p** Map some network port to the container

[Mapping port](https://firebasestorage.googleapis.com/v0/b/pictures-dc7c3.appspot.com/o/dockerimg1.png?alt=media&token=dc6e550a-2c87-4ad0-ab3e-eee0826d7bc3)

$ docker container run -d --name nginx-test -p 8080:80 nginx

This command will run the container nginx in background with the
name nginx-test and map the port 8080 **your machine** to the port
80 of the container.

After you can access the container with your browser doing only

**http://localhost:8080**

## Interactive mode inside a container

This will start a container and you enter it 
so you are inside the container

$ docker it <image>

## Exit when interactive mode container

**Be carefull** if the container have only one
process running the exit command will stop the container

$ exit 

**CTRL P+Q** will exit the container without killing it


## Download example container 

This will try to run the container called
hello-world, because this container is not
present in the machine it will get it from
the docker public repository.

This container will just print fast an hello-world

$ docker run hello-world

