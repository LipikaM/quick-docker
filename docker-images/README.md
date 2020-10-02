
# Docker Layers and Images


 - Images are read only templates used to create containers.
 - Images can have layers of other images
 - Images are stored in Docker registry
 - All changes made into the running containers will be written into the writable layer
 - When the container is deleted the writable layer is also deleted but the underlying image remains unchanged.
 - Multiple containers can share access to the same underlying image.
 
  
 # Example : Get busybox docker image layers

docker history busybox:1.32.0

IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
6858809bf669        3 weeks ago         /bin/sh -c #(nop)  CMD ["sh"]                   0B
<missing>           3 weeks ago         /bin/sh -c #(nop) ADD file:72be520892d0a903d…   1.23MB
 
# Two ways to build a docker image
- Commit changes in a docker container
- Write a docker file


# Steps to build a docker image by committing changes in a docker container
- Spin up a container by base image
- Install Git package in the container
- commit changes made in the container

# Dockerfile and instruction
- A docker file is a text document that contains all the instructions users provide to assemble an image.
- Each instruction will create a new image layer to the image.
- Instructions specify steps to follow while building an image.


