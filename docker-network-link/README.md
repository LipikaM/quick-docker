connection between spring boot microservice and mysql via docker network link...

Sample spring boot application : https://github.com/LipikaM/simplespringboot

docker run -d -p 6033:3306 --name=docker-mysql --env="MYSQL_ROOT_PASSWORD=root" --env="MYSQL_PASSWORD=root" --env="MYSQL_DATABASE=db_example" mysql
docker images ls
docker container ls
docker exec -it docker-mysql bash

mysql -uroot -p
show databases

db_example should be in the list

docker build -f Dockerfile -t simplespringboot .
docker run -t --link docker-mysql:mysql -p 8080:8080 simplespringboot
