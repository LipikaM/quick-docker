
# Docker Layers and Images

 - All changes made into the running containers will be written into the writable layer
 - When the container is deleted the writable layer is also deleted but the underlying image remains unchanged.
 - Multiple containers can share access to the same underlying image.
 
  
 # Example : Get busybox docker image layers

docker history busybox:1.32.0

IMAGE               CREATED             CREATED BY                                      SIZE                COMMENT
6858809bf669        3 weeks ago         /bin/sh -c #(nop)  CMD ["sh"]                   0B
<missing>           3 weeks ago         /bin/sh -c #(nop) ADD file:72be520892d0a903d…   1.23MB
