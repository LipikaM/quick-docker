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

#Important Docker Jargons:#

Images:

- Images are read only templates used to create containers.
- Images can have layers of other images
- Imgaes are stored in Docker registry

Containers:

- Image is a classes then contaners are the instance of a class.
- Containers	are	lightweight	and	portable	encapsulations	of	an	environment	in	which	to	run	applications.
- Containers	are	created	from	images.	Inside	a	container,	it	has	all	the	binaries	and	dependencies	needed	to	run	the	application.



