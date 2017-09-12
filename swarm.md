# Note

A cluster in docker is called a swarm

The best pratice is to have a minimum and maximum of 3 managers

Only one leader will be available at the time to do change to the
swarm.

## Start the swarm

**--advertise-addr** Set the ip to the swarm

**--listen-addr** The address the node listen on to manage the traffic

$ docker swarm init --advertise-addr 172.31.12.161:2377 --listen-addr 172.31.12.16:2377  

**The port 2377** seems to be the standard port in docker swarm

## Add node to the swarm 

$ docker swarm join --token <token id> --advertise-addr <ip> --listen-addr <ip>

## Get list of nodes

$ docker node ls

## Create services

This will create the service web-fe with 5 replicas
of this services.  The services inside the 
docker swarm are the app running (web api, front end)

$ docker service create --name web-fe --replicas 5

## Check all services running

$ docker service ls

## Check all info on a specific service running

$ docker service ps <serviceName>

## Get more info on a specific service

One important info that you will find there is the 
service **endpoint**

$ docker service inspect psight1

## Scale a service

**=** After this service name the = 
tell how many replica of this service
we wants.

$ docker service scale <servicename>=7

**OR**

$ docker service update --replicas 10 <servicename>