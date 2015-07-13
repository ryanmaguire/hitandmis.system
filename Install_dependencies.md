##Dependancies unavailable with apt
###Install libncurses5
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/libncurses5_5.7%2B20100313-5_i386.deb
	

and install
	
	$ dpkg --install libncurses5_5.7+20100313-5_i386.deb



###Install coreutils
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/coreutils_8.5-1_i386.deb

and install

	$ dpkg --install coreutils_8.5-1_i386.deb



###Install Kernel Headers
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/linux-headers-2.6.34.10-vortex86-sg_1.2_i386.deb
	
and install

	$ dpkg --install linux-headers-2.6.34.10-vortex86-sg_1.2_i386.deb

Needs the headers to be linked as described [here](http://askubuntu.com/questions/260176/lib-modules-2-6-38-8-generic-build-no-such-file-or-directory)

	$ ln -s /usr/src/linux-headers-2.6.34.10-vortex86-sg/ /lib/modules/2.6.34.10-vortex86-sg/build



###Install Kernel Image
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/linux-image-2.6.34.10-vortex86-sg_1.2_i386.deb
	
and install

	$ dpkg --install linux-image-2.6.34.10-vortex86-sg_1.3_i386.deb
	

##Princeton Instruments Pixis


###Install dkms
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/dkms_2.1.1.2-5_all.deb
	
and install

	$ dpkg --install dkms_2.1.1.2-5_all.deb



###Install pixis camera driver
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/pvcam-pilk-usb-dkms_1.0.3-1ubuntu1_all.deb
	
and install

	$ dpkg --install pvcam-pilk-usb-dkms_1.0.3-1ubuntu1_all.deb



###Setting up libpvcam

	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/libpvcam.so.2.7.4.2.bin
	
and set it up with

	$ mv libpvcam.so.2.7.4.2.bin /usr/lib/libpvcam.so.2.7.4.2
	
	
	
###Intall pvcam sdk
	$ wget --no-check-certificate https://github.com/kuravih/hitandmis.system/raw/master/dependencies/pi_pvcam_sdk_installer-2.7.1.7.tar.gz
	
and install

	$ tar zxvf pi_pvcam_sdk_installer-2.7.1.7.tar.gz
	$ cd pvcam2.7.1.7
	$ ./install_sdk.sh


##Andor iKon

	$ wget --no-check-certificate  https://github.com/kuravih/hitandmis.system/raw/master/dependencies/andor-2.98.30010.0.tar.gz

and install

	$ tar zxvf andor-2.98.30010.0.tar.gz
	$ cd andor
	$ sudo ./install_andor

















