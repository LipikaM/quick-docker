# quick-docker

A quick overview about docker for developers. 


Docker is one implementation of container based virtualization technologies.

Pre-Virtulaization Issues:
- Cost
- Slow deployment
- Hard to migrate

Hypervisor based virtualization:

Benefits:
- Cost effective 
- Easy to scale

Limitation:
- Kernel resource duplication
- Application portability issue

Container based virtulization:

Benefits:
- cost effective
- fast deployment
- Application portability

Difference : In hypervisor based system OS/Kernel duplication and virtulization at hardware level whereas container based system shares same kernel/OS 
which is container engine and the virtulization happens at the OS level. Hence more efficient and light weighted.

Why to run the applications in different containers not in one VM ?
- runtime isolations (In case application A requires JRE7 and application B requires JRE8)

Registries	and	Repositories:

- Images are stored under registries
- You can host your own registry or use docker's existing public registry which is called DockerHub.
- Inside the registry, images are stored under repositories.
- Docker repository	is	a	collection	of	different	docker images	with	the	same	name,	that	have	different	tags,	each	tag	usually	represents	a	different	version	of	the	image.

# Why using official docker images:
- Proper documentation
- Dedicated team for image content review
- Timely security update



