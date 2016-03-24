##Network
For some reason the  `/etc/network/interfaces` will look like this

	# The loopback network interface
	auto lo
	iface lo inet loopback

	auto eth0
	niface eth0 inet dhcp

but it needs to be

	# The loopback network interface
	auto lo
	iface lo inet loopback

	# The eth1 interface
	auto eth1
	iface eth1 inet dhcp

and bring *eth1* online by

	$ ifup eth1



####apt-get

Put the following lines in `/etc/apt/sources.list`

	deb http://archive.debian.org/debian/ lenny contrib main non-free
	deb http://archive.debian.org/debian-security lenny/updates main

and then update apt by

	$ apt-get update

and update key-ring by

	$ apt-get install debian-archive-keyring

Reference [unix.stackexchange.com](http://unix.stackexchange.com/questions/66830/are-there-any-source-apt-repositories-for-debian-lenny). There will be a [GPG error... NO_PUBKEY...](http://askubuntu.com/questions/13065/how-do-i-fix-the-gpg-error-no-pubkey) issue that can be fixed by

	$ apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8BAF9A6F



####sudo
	$ apt-get install sudo



####ssh
	$ apt-get install openssh-server



####build-essential
	$ apt-get install build-essential



####beep
Required for virtual

		$ apt-get install beep



####libusb-dev
Required for ikon

	$ apt-get install libusb-dev



####libraw1394-dev
Required for pixis

	$ apt-get install libraw1394-dev
