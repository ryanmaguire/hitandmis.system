## Deployment

### Camdaemon

Download camdaemon files. Unzip into a local folder.

To access, do:

    cd (Wherever the file is)
  
To sync time with main computer, do:

    ./sync.sh --server=(IP from ifconfig) --user=ikon --time

To sync the code (Send from main computer to the camera's computer), do:

    ./sync.sh --server=(IP from ifconfig) --user=ikon --camera=pixis --code

###Server

Download server files. Unzip into a local folder.

To access, do:

    cd (Wherever the file is)

To setup the server, do:

        ./sync.sh --server=(IP from ifconfig) --user=ikon --code

To sync the time to the server, do:

        ./sync.sh --server=(IP from ifconfig) --user=ikon --time

### Double Check for Deployment

Check that camdaemon and server will respawn.

        cat /etc/inittab
You should see `cd:2345:respawn:/home/ikon/camdaemon/daemon.sh` and ` hs:2345:respawn:/home/ikon/hitandmis.server/server.sh` at the bottom. If not, do:

        sudo pico /etc/inittab

and add them.

###Capturing an Image

To issue a capture command, do: (From Camera's Computer)

    telnet localhost 3000
    
Or, from another computer

    telnet (IP from ifconfig) 3000

In the telnet prompt, do:

    capture (Exposure time is milliseconds)

To access images, use filezilla or an equivalent

  


