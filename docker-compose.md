# Use docker compose command

## To launch a docker compose file in detach mode

$ docker-compose up -d

## See the list of process launch from the docker compose

$ docker-compose ps

## Validate the compose YML file

If the file has no error the YAML file will
be print to the screen, if not output is show
this mean the file have an error

$ docker-compose config

## Get the error of the compose YAML file

$ docker-compose config -q

## Pull all image inside the compose file

$ docker-compose pull

## Execute any build in the compose file

$ docker-compose build

## Create all container from the compose file without launching them

This will create all container but won't launch them

$ docker-compose create

## Instruct container

Those commands will affect all container inside the 
compose file

$ docker-compose start
$ docker-compose stop
$ docker-compose restart
$ docker-compose pause
$ docker-compose unpause

## Affect only one service (container)

$ docker-compose pause <nameOfContainer>
$ docker-compose unpause <nameOfContainer>

## Display info of running container

$ docker-compose top

## Scale a service

$ docker-compose up -d --scale <worker>=3
$ docker-compose up -d --scale vote=3

## Kill compose app

Be carefull the kill command won't close gracefully  the
compose application, this can cause datalost.

$ docker-compose kill

## Start compose app

$ docker-compose up

## Stop compose app

That will remove the containers and the networks created when running docker-compose up

$ docker-compose down

## Remove everything when stopping

$ docker-compose down --rmi all --volumes