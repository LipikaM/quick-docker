
# Docker Layers and Images

 - All changes made into the running containers will be written into the writable layer
 - When the container is deleted the writable layer is also deleted but the underlying image remains unchanged.
 - Multiple containers can share access to the same underlying image.
