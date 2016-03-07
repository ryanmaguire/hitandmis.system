# hitandmis.system
Libraries and system dependancies required to setup the hit&amp;mis.

##Setup (Internet connection required)
Debian setup for EBox3100 is [here](../master/linux_setup.md). Install the dependancies as shown [here](../master/install_dependencies.md)

##Deployment (Internet connection not required)
The `hitandmis.server` and the `camdaemon` can be deployed via the network from a development computer using the sync scripts in each repository.
#####camdaemon
	./sync.sh --server=192.168.1.2 --user=ikon --camera=pixis --time --code

#####hitandmis.server
	./sync.sh --server=192.168.1.2 --user=ikon --time --code

finally append the following lines to `/etc/inittab` to setup persistent services

	cd:2345:respawn:/home/ikon/camdaemon/daemon.sh
	hs:2345:respawn:/home/ikon/hitandmis.server/server.sh
