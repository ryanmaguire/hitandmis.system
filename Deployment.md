## Deployment

Go to camdaemon folder and download the zip file. Unzip into a local folder.

To access, do:

    cd (Wherever the file is)
  
To sync time with main computer, do:

    ./sync.sh --server=(IP from ifconfig) --user=ikon --time

To sync the code (Send from main computer to the camera's computer), do:

    ./sync.sh --server=(IP from ifconfig) --user=ikon --camera=pixis --code

To issue a capture command, do: (From Camera's Computer)

    telnet localhost 3000
    
Or, from another computer

    telnet (IP from ifconfig) 3000

In the telnet prompt, do:

    capture (Exposure time is milliseconds)

To access images, use filezilla or an equivalent

  


