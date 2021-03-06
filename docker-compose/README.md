# Docker compose:

Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration.

Using Compose is basically a three-step process:

1. Define your app’s environment with a Dockerfile so it can be reproduced anywhere.

2. Define the services that make up your app in docker-compose.yml so they can be run together in an isolated environment.

3. Run docker-compose up and Compose starts and runs your entire app.

Reference : https://docs.docker.com/compose/

Basic commands:

| Command  | Description |
| ------------- | ------------- |
| docker-compose -v  | check docker compose version |
| docker-compose	up  | starts	up	all	the	containers  |
| docker-compose	ps  | checks	the	status	of	the	containers	managed	by	dockercompose  |
| docker-compose	logs  | outputs	colored	and	aggregated	logs	for	the	compose-managed	containers  |
| docker-compose	logs -f  | outputs	appended	log	when	the	log	grows  |
| docker-compose	logs container_id  | outputs	the	logs	of	a	specific	container  |
| docker-compose	stop  | stops all running containers  |
| docker-compose	rm  | removes all the containers  |
| docker-compose	build  | rebuilds all the images  |


Sample spring boot application used for the docker-compose.yml is here : https://github.com/LipikaM/simplespringboot

Run : docker-compose up
This will execute Dockerfile commands and will run services defined in the docker-compose file.






