# astroberry-server
Astroberry Server is a ready to use astronomy desktop system for Raspberry Pi 3
It is a standalone system for controlling astronomy equipment supported by INDI server.

The system features:
- Ubuntu Mate 16.04 Desktop
- Remote desktop accessible over VNC at astroberry.local:5900 or a web browser at https://astroberry.local
- KStars and Ekos with all available device drivers
- Astrometry with basic index files
- PHD2 for autoguiding
- Gnome Predict for satellite tracking
- StarPlot for 3-dimensional positions of stars in space
- oaCapture and wxAstroCapture for planetary imaging
- Astroberry PiFace drivers for a relay and focuser control

# How to start?
Unpack and flash your microSD card (minimum 16GB required) with the system image:
```
xz -d astroberry-XXX.img.xz
dd if=astroberry-XXX.img of=/dev/sdX bs=4M
```

# How to use it?
It's as simple as this:
- Start your Raspberry Pi 3 with the flashed microSD card.
- Connect to a astroberry wireless network (default password is astroberry)
- Point your browser to https://astroberry.local
- Have fun

# How to reconfigure it?
You can use it as any Ubuntu system, however there are some mission critical parameters to be configured by
embedded scripts i.e.
- aprename - to change access point name from astroberry to whatever you want
- appass - to change password to your astroberry access point
- wlanconf - to configure and connect Astroberry Server to your home wireless network
- wlanconf-gui - to configure and connect Astroberry Server to your home wireless network in GUI (available in menu and on the Ubuntu Mate taskbar)

# What is default username and password?
It's always astroberry:
- For SSH access run: ssh astroberry@astroberry.local
- For VNC access use astroberry.local:5900 for server and astroberry for username and password
- For your browser access use https://astroberry.local for server and astroberry for password

In case of any issue accessing astroberry.local just use 192.168.10.1 after connecting to astroberry access point or
your home network access after connecting to your wireless home network.

# Issues
File any issues on https://github.com/rkaczorek/astroberry-server
