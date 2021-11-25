
# Chromium-Browser
# Source
https://bartsimons.me/raspberry-pi-kiosk-tutorial/

https://die-antwort.eu/techblog/2017-12-setup-raspberry-pi-for-kiosk-mode/

sudo apt-get install --no-install-recommends xserver-xorg x11-xserver-utils xinit

sudo apt-get install --no-install-recommends chromium-browser

sudo apt-get install upower

## Manuly start chromium browser only with pi user
export DISPLAY=:0 && /nites/youtube

# #
add below line in .profile 
 
[[ -z $DISPLAY && $XDG_VTNR -eq 1 ]] && startx -- -nocursor


# youtubetv
Youtube TV for Raspberry Pi 4

# Source
https://www.linuxuprising.com/2021/04/how-to-cast-youtube-videos-from-your.html

# Help Docs
https://forums.raspberrypi.com/viewtopic.php?t=189006

To start chromium-browser on HDMI

DISPLAY=:0 chromium-browser -kiosk

# Autohide Cursor
sudo apt-get install unclutter

unclutter -idle 0.01 -root


# resolution_fix
Fix resolution in screen

# How to Adjust Screen Resolution

Type in the following command if you are using a television: /opt/vc/bin/tvservice -m CEA or

type in the following command if you are using a PC monitor: /opt/vc/bin/tvservice -m DMT

hdmi_group=1

hdmi_mode=39


# To remove Black boarders around screen
disable_overscan=1
