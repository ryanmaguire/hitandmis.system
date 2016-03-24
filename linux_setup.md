## Serial-to-USB
The following commands are on the "Host," computer. i.e. Not the camera computer.
Check to make sure the serial to usb controller is plugged in

	ls /dev/tty*
	
You should see `/dev/ttyUSB0` or 1, or 2, or serial, etc. If not, troubleshoot.

Next, use the `screen` command to talk to the camera's computer. (see [here](https://wiki.archlinux.org/index.php/working_with_the_serial_console#Screen))

	sudo screen /dev/ttyUSB0 115200
	
Then hit `Enter`
	
Now you shouid be in the Camera's computer.

To obtain the IP address for ssh, do the following (Using the camera computer's command line)

	sudo ifconfig

If you do not get an IP address, then go to Network for troubleshooting.

To exit from screen, do `CTRL + A`, then `CTRL + D`.

##Network
A common mistake is that `/etc/network/interfaces` looks like

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

To view, do

	sudo cat /etc/network/interfaces

To edit/view, do

	sudo pico /etc/network/interfaces
	
Change to what is needed, if applicable.
	
and bring *eth1* online by

	$ ifup eth1

If dhcp is available, you should see:

	iface eth1 inet dhcp
	#iface eth1 inet static
	#address 192.168.1.2
	#netmask 255.255.255.0

If dhcp is not available, change this too:

	#iface eth1 inet dhcp
	iface eth1 inet static
	address 192.168.1.2
	netmask 255.255.255.0

After any change to the `interfaces` file, you need to do:

	sudo ifdown eth1
	sudo ifup eth1
	
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
