## Docker network types

1. Closed	Network	/	None Network
2. Bridge	Network
3. Host	Network
4. Overlay	Network

# None network:
 - Provides	the	maximum	level	of	network	protection.
 - Not	a	good	choice	if	network	or	Internet	connection	is	required.
 - Suites	well	where	the	container	require	the	maximum	level	of	network	security	and	network	access	is	not	necessary.
 
 Lists the networks:
 docker network ls
 
 # Bridge network
 - A bridge network is a Link Layer device which forwards traffic between network segments.
 - A bridge network uses a software bridge which allows containers connected to the same bridge network to communicate, while providing isolation from containers which are not connected to that bridge network.
 - Bridge networks apply to containers running on the same Docker daemon host
 
 # Host network
 - The	least	protected	network	model,	it	adds	a	container	on	the	host's	network	stack. 
 - Containers	deployed	on	the	host	stack	have	full	access	to	the	host's	interface. 
 - This	kind	of	containers	are	usually	called	open	containers.
 - Minimum	network	security	level.
 - No	isolation	on	this	type	of	open	containers,	thus	leave	the	container	widely	unprotected.
 - Containers	running	in	the	host	network	stack	should	see	a	higher	level	of	performance	than	those	traversing	the	docker0	bridge	and	iptablesport	mappings.
 
 # Overlay network
 - The overlay network driver creates a distributed network among multiple Docker daemon hosts.
 - This network sits on top of (overlays) the host-specific networks, allowing containers connected to it (including swarm service containers) to communicate securely when encryption is enabled. Docker transparently handles routing of each packet to and from the correct Docker daemon host and the correct destination container.
 
 
 Sources : https://docs.docker.com/
 
 
 
