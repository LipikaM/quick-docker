
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

# More about Dockerfile...

## Chain run instructions :
 - Each	RUN	command	will	execute	the	command	on	the	top	writable	layer	of	the	container,	then	commit	the	container	as	a	new	image.
 - The	new	image	is	used	for	the	next	step	in	the	Dockerfile.	So	each	RUN	instruction	will	create	a	new	image	layer.
 - It	is	recommended	to	chain	the	RUN	instructions	in	the	Dockerfile to	reduce	the	number	of	image	layers	it	creates.
 
## CMD	Instructions :

- CMD	instruction	specifies	what	command	you	want	to	run	when	the	container	starts	up.	
- If	we	don't	specify	CMD	instruction	in	the	Dockerfile,	Docker will	use	the	default	command	defined	in	the	base	image.	
- The	CMD	instruction	doesn’t	run	when	building	the	image,	it	only	runs	when	the	container	starts	up.	
- You	can	specify	the	command	in	either	exec	form	which	is	preferred	or	in	shell	form.

## Docker Cache
- Each	time	Docker executes	an	instruction	it	builds a new image layer.
- The	next	time,	if	the	instruction	doesn't	change,	Docker will	simply	reuse	the	existing	layer.
- 
