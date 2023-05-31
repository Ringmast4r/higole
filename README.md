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




# Xorg (NOT READY)

## Create Higole Xorg configs
Create Intel xorg config at '/etc/X11/xorg.conf.d/20-intel.conf' with the following:

'''
Section "Device"
  Identifier    "Intel Graphics"
  Driver        "intel"
EndSection

'''


Create display cocnfig at '/etc/X11/xorg.conf.d/30-display.conf'
'''
Section "Monitor"
  Identifier    "DSI-1"
  Option        "Rotate"                 "right"
EndSection
'''

Create touchscreen config at '/etc/X11/xorg.conf.d/99-touchscreen.conf' with the following:

