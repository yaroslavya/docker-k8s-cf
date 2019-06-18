docker networks
===============

there are 5 types of docker networks:
host, bridge, macvlan, overlay and none.

you'll probably only need 3 of them most of the time.
these are host, bridge and, maybe none( probably not ).

###1. To list the docker networks that you currently have use

docker network ls

###2. To check what network your container is attached to use
docker inspect <container_name> and list down to the network part.

###3. lets create a container with another type of network
docker run --rm --name container1 nginx
docker inspect container1 
docker network connect host container1
**gives an ugly error**
docker network disconnect bridge container1
**works**

###4. lets really create a container with another type of network
docker run --network host --rm --name container1 nginx
docker inspect container1
curl localhost:80/ - gives default nginx page