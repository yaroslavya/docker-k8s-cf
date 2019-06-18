Docker commands
===============

docker run hello-world

Thats the "hello world" of docker. You can notice that some things are happening already:

- we send the command to docker via cli
- docker daemon checks if "hello-world" image is present
- if not - image is being pulled
- docker daemon starts the container, based on the image

Lets use some more commands to check what do we have:

- **docker ps** # lists all the running containers we have so far
- **docker ps -a** #or 
- **docker ps --all** # lists all the containers we have on the local machine

- **docker run --rm hello-world** 

the **--rm** flag will remove the container when it exists, so we dont have the container in our list of containers.

- **docker start &lt;container-name/container-id&gt;**
if you have a container that was started and was never removed you can start it again.

**docker rm &lt;container-name/container-id&gt;**

**docker rm $(sudo docker ps -a | grep hello )**

**docker container run --rm -it -p 8088:80 nginx**

**it** - run in the foreground and show all the logs container is making to the console

**-p** map the ports -p <host_port:container_port>
so **-p 8088:80** means map the host machine port 8088 to container port 80.
