##Dependancies unavailable with apt
###Install libncurses5
	$ wget http://ftp.us.debian.org/debian/pool/main/n/ncurses/libncurses5_5.7+20100313-5_i386.deb

and install
	
	$ dpkg --install libncurses5_5.7+20100313-5_i386.deb



###Install coreutils
	$ wget http://ftp.us.debian.org/debian/pool/main/c/coreutils/coreutils_8.5-1_i386.deb`

and install

	$ dpkg --install coreutils_8.5-1_i386.deb`



###Install Kernel Headers
	$ wget ftp://vxdx:gc301@ftp.dmp.com.tw/Driver/Linux/kernel_package/linux-headers-2.6.34.10-vortex86-sg_1.2_i386.deb
	
and install

	$ dpkg --install linux-headers-2.6.34.10-vortex86-sg_1.2_i386.deb

Needs the headers to be linked as described [here](http://askubuntu.com/questions/260176/lib-modules-2-6-38-8-generic-build-no-such-file-or-directory)

	$ ln -s /usr/src/linux-headers-2.6.34.10-vortex86-sg/ /lib/modules/2.6.34.10-vortex86-sg/build



###Install Kernel Image
	$ wget ftp://vxdx:gc301@ftp.dmp.com.tw/Driver/Linux/kernel_package/linux-image-2.6.34.10-vortex86-sg_1.3_i386.deb
	
and install

	$ dpkg --install linux-image-2.6.34.10-vortex86-sg_1.3_i386.deb
	

##Princeton Instruments Pixis


###Install dkms
	$ wget http://ftp.us.debian.org/debian/pool/main/d/dkms/dkms_2.1.1.2-5_all.deb
	
and install

	$ dpkg --install dkms_2.1.1.2-5_all.deb



###Install pixis camera driver
	$ wget ftp://ftp.piacton.com/Public/Software/Official/Drivers/Linux/pvcam-pilk-usb-dkms_1.0.3-1ubuntu1_all.deb
	
and install

	$ dpkg --install pvcam-pilk-usb-dkms_1.0.3-1ubuntu1_all.deb



###Setting up libpvcam

	$ wget ftp://ftp.piacton.com/Public/Software/Official/Linux/libpvcam.so.2.7.4.2.bin
	
and set it up with

	$ mv libpvcam.so.2.7.4.2.bin /usr/lib/libpvcam.so.2.7.4.2
	
	
	
###Intall pvcam sdk
	$ wget ftp://ftp.piacton.com/Public/Software/Official/Linux/pi_pvcam_sdk_installer-2.7.1.7.tar.gz
	
and install

	$ tar zxvf pi_pvcam_sdk_installer-2.7.1.7.tar.gz
	$ cd pvcam2.7.1.7
	$ ./install_sdk.sh


##Andor iKon

	$ wget 

and install

	$ tar zxvf andor-2.98.30010.0.tar.gz
	$ cd ~/andor
	$ sudo ./install_andor

















