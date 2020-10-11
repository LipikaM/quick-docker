# Dockerize dropwizard microservice

- Clone the git repo for sample microservice written in dropwizard (maven build) : <GIT link to be passed>
- Get the jar build out of the project and example.yml file under a folder with Dockerfile

## Docker build :

docker build -t service-quick-hello .

## Docker Run:

docker run -it -p 8080:8080 service-quick-hello

service will be up and running : http://localhost:8080/hello-world
