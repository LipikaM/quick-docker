# Docker containers

- Image is a classes then contaners are the instance of a class.
- Containers are lightweight and portable encapsulations of an environment to run applications.
- Containers are created from images. Inside a container, it has all the binaries and dependencies needed to run the application.

# Container commands

- Containers can be run in detached mode with option -d
- docker ps command : to get all running processes
- docker inspect command : to get docker id details in JSON format


## Useful container commands
list the docker containers:
docker ps -a

list only the container ids:
docker ps -aq

list all the running docker containers:
docker ps

delete a docker container with id:
docker container rm docker_id

Look inside the docker container
docker exec -it container_id bash
