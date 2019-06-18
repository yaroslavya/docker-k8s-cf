what can we do with this?
=========================

###1. stop and start the container

docker start <container_id_or_name>
docker stop <container_id_or_name>

###2. attach to the running container

docker attach <container_id_or_name>
if you ctrl+x it will stop the container as the sigkill will be sent to the container from your input. 
you can use ctrl+p,ctrl+q to detach from the container while leaving it running

**HACK:**

attach to container like that:

docker attach <container_id_or_name> --detach-keys="<sequence>"
	where sequence can contain
- a-z, @, [, \\, underscore, ^

###3. get inside the container to see its files
docker exec -it <container_name> /bin/sh

###4. change these files to see the effect immediately

default website is at /usr/share/nginx/html
change its contents to something fancy by opening the html file and editing it

###5. executing command without being in the container

docker exec -t <container_name> /bin/sh -c "any command here"
