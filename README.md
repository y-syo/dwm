# yswm - yosyo's own build of dwm

dwm is an extremely fast, small, and dynamic window manager for X.

Requirements

In order to build dwm you need the Xlib header files.

Installation
------------
Edit config.mk to match your local setup.

Afterwards enter the following command to build and install dwm :

    make clean dwm

Don't forget to add it to the path, or do this if you have sudo privileges

    sudo make install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
