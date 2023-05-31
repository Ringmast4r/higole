# Gole Gang unofficial support team here to take your request

# Accessories
## Possible case options.
- https://a.co/d/go6dnKG
- https://a.co/d/9tBpxil
- https://a.co/d/aZ67kRv
- https://a.co/d/hxNJGWD (image of use in ig group)
- https://a.co/d/iCT9XTF
- https://a.co/d/1aHPJct
- https://a.co/d/cUuw2CU
- pelican 1040 (tested by Off Grid)



# Xorg(NOT READY)
## Create Higole Xorg configs

Create Intel xorg config at `/etc/X11/xorg.conf.d/20-intel.conf` with the following:
```

Section "Device"
  Identifier    "Intel Graphics"
  Driver        "intel"
EndSection
```

Create display config at `/etc/X11/xorg.conf.d/30-display.conf`
```

Section "Monitor"
  Identifier    "DSI-1"
  Option        "Rotate"            "right"
  Option        "RandRRotation"     "on"
EndSection
```

Create touchscreen config at `/etc/X11/xorg.conf.d/99-touchscreen.conf` with the following:





# WiFi
## Change WiFi name back to wlan0, wlan1 
In recent versions of Parrot OS Linux and some other Linux distributions, the traditional naming convention for network interfaces (such as wlan0, wlan1, eth0, etc.) has been replaced by a new naming scheme called "Predictable Network Interface Names" or "Consistent Network Device Naming." This change was made to provide more consistent and predictable naming for network interfaces.

Under the new naming scheme, network interfaces are assigned names based on their physical location or other characteristics. For example, the name may include information about the PCI bus, the slot number, or the MAC address of the device.

To determine the names of your Wi-Fi adapters or other network interfaces in Parrot OS Linux, you can use the following command:
` ip link show
` ` ` 
This command will display a list of network interfaces along with their assigned names. Look for interfaces starting with "wlan" to identify your Wi-Fi adapters.

If you prefer to use the traditional naming convention (e.g., wlan0, wlan1), you can disable the Predictable Network Interface Names and revert to the old naming scheme. Here's how:

1. Open a terminal or command prompt.
2. Edit the GRUB configuration file using a text editor. For example:
` sudo nano /etc/default/grub` 
3. Locate the line that starts with GRUB_CMDLINE_LINUX_DEFAULT and add the following parameter:
` net.ifnames=0` 
The line should look something like this after adding the parameter:
` GRUB_CMDLINE_LINUX_DEFAULT="quiet swish net.ifnames=0"` 
4. Save the changes to the GRUB configuration file and exit the text editor.
5. Update GRUB using the following command:
` sudo update-grub` 
6. Reboot your system.

After rebooting, your network interfaces should be named using the traditional convention (e.g., wlan0, wlan1, eth0, etc.).

-test by ringmast4r
