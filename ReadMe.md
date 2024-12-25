Docker Commands Guide

    docker run [container name]
    Runs the specified Docker container.

    docker ps
    Displays the details of currently running containers.

    docker stop [container]
    Stops the specified Docker container. (Note: The container needs to be running to stop it.)

    docker rm [container]
    Removes the specified Docker container. (Note: The container needs to be stopped before it can be removed.)

    docker run -d redis:9.6
    The command docker run -d redis:9.6 starts a Redis database container in the background, allowing it to run quietly without showing logs in the terminal. (Ensure the image name is correct, e.g., redis:9.6 instead of redis9.6.)
  
    docker ps -a

The docker ps -a command lists all Docker containers on your system, including those that are stopped, running, or exited.

Port binding in docker 

/*
The Concept of Port Binding:
When we start a Docker container, the service (like Redis, a web server, or a database) runs inside the container. By default, this service is isolated and cannot be accessed outside the container.

To allow the service to be accessible from our host machine (outside the container), we use port binding. Port binding connects a port on the host machine to a port inside the Docker container, allowing us to interact with the containerized application from the host
*/

sudo docker run -p [HOST_PORT]:[CONTAINER_PORT] redis


Docker Debugging Commands

1.  if our application is't being able to connect however we want to view logs to see how to start debugging
docker log [container id/name]

2.
 sudo docker run -d -p6000:6379 --name redis-latest redis   
 
 
 
 3.
 sudo docker exec -it 207455aba23e /bin/bash

 running this command opens a direct terminal inside the container, allowing you to perform operations just like you'd do in a normal Linux environment but isolated within the container.
