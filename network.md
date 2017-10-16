# Create network in docker

$ docker create network <name>

# Launch container on a specific network

$ docker container run -d --name redis --network <networkName> <containerImage>

# Ping an instance from a container

In this case we have this node.js app running called moby-container.
This app connect to redis and we have another container called
redis.  Doing this command will make the container moby-counter try
to ping the redis one.  

$ docker container exec moby-counter ping -c 3 redis

# Get all the host of a specific node app

$ docker container exec moby-counter cat /etc/hosts

The last entries here will be the container id and
the ip address associated to this container

# Network alias

In docker we cannot have two container running with the same
name at the same time.  If in your code you need a specific name
to resolve a DNS you can create a network alias.


$ docker container run -d --name redis2 --network moby-counter2 --network-alias redis redis:alpine

# NSLookup

This command check for a specific container to a specific IP address
if this container can resolve the other container 

$ docker container exec moby-counter2 nslookup redis 127.0.0.11

# Get info for a specific network

$ docker network inspect <moby-counter>

# Remove all not used network

$ docker network prune

# Get list of all volume in the machine

$ docker volume ls

# Bind redis to a specific volume

The big ID is the id associated to one of the volume in the machine

$ docker container run -d --name redis -v 719d0cc415dbc76fed5e9b8893e2cf547f0ac6c91233451604fdba31f0dd2d2a:/data --network moby-counter redis:alpine

# Create a volume 

$ docker volume create redis_data

$ docker container run -d --name redis -v redis_data:/data --network moby-counter redis:alpine

# Inspect volume

$ docker volume inspect <redis_data>