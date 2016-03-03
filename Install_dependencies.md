##Dependancies unavailable with apt
Most of these packages are obsolete so a copy of the required dependencies will be held here.

###[libncurses5](ftp://ftp.gnome.org/mirror/debian-archive/pool/main/n/ncurses/libncurses5_5.7+20100313-5_i386.deb)
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/libncurses5_5.7%2B20100313-5_i386.deb


and install by

	$ dpkg --install libncurses5_5.7+20100313-5_i386.deb



###[coreutils](ftp://ftp.gnome.org/mirror/debian-archive/pool/main/c/coreutils/coreutils_8.5-1_i386.deb)
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/coreutils_8.5-1_i386.deb

and install

	$ dpkg --install coreutils_8.5-1_i386.deb



###Kernel Headers
These headers are provided by the vendor
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/linux-headers-2.6.34.10-vortex86-sg_1.2_i386.deb

and install

	$ dpkg --install linux-headers-2.6.34.10-vortex86-sg_1.2_i386.deb

Needs the headers to be linked as described [here](http://askubuntu.com/questions/260176/lib-modules-2-6-38-8-generic-build-no-such-file-or-directory)

	$ ln -s /usr/src/linux-headers-2.6.34.10-vortex86-sg/ /lib/modules/2.6.34.10-vortex86-sg/build



###Kernel Image
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/linux-image-2.6.34.10-vortex86-sg_1.2_i386.deb

and install

	$ dpkg --install linux-image-2.6.34.10-vortex86-sg_1.3_i386.deb


##Princeton Instruments Pixis


###[dkms](ftp://ftp.gnome.org/mirror/ubuntu/pool/main/d/dkms/dkms_2.1.1.2-2ubuntu1_all.deb)
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/dkms_2.1.1.2-5_all.deb

and install

	$ dpkg --install dkms_2.1.1.2-5_all.deb


###[cfitsio](http://heasarc.gsfc.nasa.gov/FTP/software/fitsio/c/cfitsio3380.tar.gz)
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/cfitsio3380.tar.gz

	and install by

		$ tar xvf cfitsio3380.tar.gz
		$ cd cfitsio
		$ sudo ./install_andor
		$ ./configure --prefix=/usr/local
		$ make
		$ sudo make install


###Phidgets Spatial 1056_0 3/3/3 driver [libphidget](http://www.phidgets.com/downloads/libraries/libphidget.tar.gz)
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/libphidget_2.1.8.20151217.tar.gz

	and install by

		$ tar xvf libphidget_2.1.8.20151217.tar.gz
		$ ./configure
		$ make
		$ sudo make install


###[pixis camera driver](ftp://ftp.piacton.com/Public/Software/Official/Linux/pvcam-pilk-usb-dkms_1.0.3-1ubuntu1_all.deb)
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/pvcam-pilk-usb-dkms_1.0.3-1ubuntu1_all.deb

and install

	$ dpkg --install pvcam-pilk-usb-dkms_1.0.3-1ubuntu1_all.deb



###[libpvcam](ftp://ftp.piacton.com/Public/Software/Official/Linux/libpvcam.so.2.7.4.2.bin)

	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/libpvcam.so.2.7.4.2.bin

and set it up with

	$ mv libpvcam.so.2.7.4.2.bin /usr/lib/libpvcam.so.2.7.4.2



###[pvcam sdk](ftp://ftp.piacton.com/Public/Software/Official/Linux/pi_pvcam_sdk_installer-2.7.1.7.tar.gz)
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/pi_pvcam_sdk_installer-2.7.1.7.tar.gz

and install

	$ tar zxvf pi_pvcam_sdk_installer-2.7.1.7.tar.gz
	$ cd pvcam2.7.1.7
	$ ./install_sdk.sh


##[Andor iKon](http://my.andor.com/user/)

	$ wget --no-check-certificate  https://github.com/kuravih/hitandmis.system/raw/master/dependencies/andor-2.98.30010.0.tar.gz

and install

	$ tar zxvf andor-2.98.30010.0.tar.gz
	$ cd andor
	$ sudo ./install_andor
