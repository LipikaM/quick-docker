## docker build command:

C:\Users\default.DESKTOP-0NMG7L4\dckrfile\quick-docker\web-app-deployment>docker build -t dockerapp:v0.1 .

## check docker image for the above build image
C:\Users\default.DESKTOP-0NMG7L4\dckrfile\quick-docker\web-app-deployment>docker images
REPOSITORY              TAG                 IMAGE ID            CREATED              SIZE
dockerapp               v0.1                3be706b166d4        About a minute ago   882MB

## run the docker container with the build image id
C:\Users\default.DESKTOP-0NMG7L4\dckrfile\quick-docker\web-app-deployment>docker run -d -p 5000:5000 3be706b166d4
474d58045830db362715e30ba358c2d3db38c5835c8c771459a6a36f95b55242

## check the URL
check at localhost:5000

## Run a command in a running container

get docker container id
C:\Users\default.DESKTOP-0NMG7L4\dckrfile\quick-docker\web-app-deployment>docker ps

run any command (in this case bash with the container id)
C:\Users\default.DESKTOP-0NMG7L4\dckrfile\quick-docker\web-app-deployment>docker exec -it 474d58045830 bash


