Simple Raspberry Pi MMAL project

Starting from a 2014-09-09-wheezy-raspbian.img this now compiles.  A couple of lines have had to be commented out so the functionality is reduced.

Build
-----
0. Install pre-required packages
   
    $ sudo apt-get install cmake libopencv-dev


1. Place  Raspberry Pi userland project in /home/pi/src/raspberrypi/userland
    
    $ mkdir -p /home/pi/src/raspberrypi
    
    $ cd /home/pi/src/raspberrypi
        
    $ git clone --depth 1 https://github.com/raspberrypi/userland.git


2. Build pre-required libraries
    
    $ make -C /opt/vc/src/hello_pi/libs/vgfont
    

3. Build project 

    $ mkdir build
    
    $ cd build
    
    $ cmake ../
    
    $ make 
    
    
