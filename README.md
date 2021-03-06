# dwm - dynamic window manager
dwm is an extremely fast, small, and dynamic window manager for X.

---
## Requirements
In order to build dwm you need the Xlib header files.

---
## Installation
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


---
## Running dwm

### For those who have a desktop environment
If you want to have option to change between your DE such as xfce and DWM in the login window. Use this:
- Put the Desktop file and Scripts in their Places

`.desktop` file goes into `/usr/share/xsessions/`.

Scripts goes into `/usr/bin/` [Scripts](Scripts/README.md)

#### For Status bar I use DwmBlocks
[DwmBlocks](https://github.com/HimanshuGoswamiii/dwmblocks)

---
### For those who don't have an already existing Desktop Environment
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

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

## Patching Done


---
## Keybindings

|Key    | Application   |
-------------------------
|Super + o | Rofi   |

