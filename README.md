# Gole Gang unofficial support team here to take your request


# Specifications 
Higole Gole 1 Pro 5.5" Industrial Tablet Mini PC

## Hardware
|   Hardware  |     Details       |  
|-------------|-------------------|
| Display     |  5.5" 720*1280(IPS)|
|    CPU      |  Intel Celeron J4125| 
|    GPU      |  Intel HD600     |
|   Memory   |  8GB LPDDR4       |
| Storage   |     128GB eMMC  |
| WIFI 6.0       | Realtek 8723BS    |
| Bluetooth 5.2   |  Realtek 8723BS   |
| Battery     |     2500mAh LiPo |
| Dimensions |  	142×91×19mm |

## I/O
|  Interface |    Details   |
|------------|---------------|
|   USB      |    x4 USB 3.0|
|  SD Card Reader |   x1 (Up To 128GB) |
|  Audio Jack |   x1 3.5mm   |
|   HDMI     |   x1 HDMI 1.4  |
|   RJ45    |    x1 1000Mbps GB Lan |
| Type-C(Charging Only) | x1 Type-C 3.1 DC 12V/3A |


## Working
| Hardware | Windows 11  |   Linux 6.0+  |
|---------|--------------|----------|
|         |              |          |
|         |              |          |



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


# WiFi

## Drivers
Drivers for the Fn-Link 6252C-PUB Wi-Fi6 Module (Realtek RTL8852BE-CG)

Windows 11: https://golerugged.com/supports/335.html

Linux: https://github.com/lwfinger/rtw89 (NEEDS WORK)

Open issue with driver maintainer can be found here https://github.com/lwfinger/rtw89/issues/242


## Change WiFi name back to wlan0, wlan1 
In recent versions of Parrot OS Linux and some other Linux distributions, the traditional naming convention for network interfaces (such as wlan0, wlan1, eth0, etc.) has been replaced by a new naming scheme called "Predictable Network Interface Names" or "Consistent Network Device Naming." This change was made to provide more consistent and predictable naming for network interfaces.

Under the new naming scheme, network interfaces are assigned names based on their physical location or other characteristics. For example, the name may include information about the PCI bus, the slot number, or the MAC address of the device.

To determine the names of your Wi-Fi adapters or other network interfaces in Parrot OS Linux, you can use the following command:
```ip link show```



This command will display a list of network interfaces along with their assigned names. Look for interfaces starting with "wlan" to identify your Wi-Fi adapters.

If you prefer to use the traditional naming convention (e.g., wlan0, wlan1), you can disable the Predictable Network Interface Names and revert to the old naming scheme. Here's how:

1. Open a terminal or command prompt.
2. Edit the GRUB configuration file using a text editor. For example:
```
sudo nano /etc/default/grub
```

3. Locate the line that starts with GRUB_CMDLINE_LINUX_DEFAULT and add the following parameter:
``` 
net.ifnames=0
```
The line should look something like this after adding the parameter:
``` 
GRUB_CMDLINE_LINUX_DEFAULT="quiet swish net.ifnames=0"
```
4. Save the changes to the GRUB configuration file and exit the text editor.
5. Update GRUB using the following command:
``` 
sudo update-grub
```
6. Reboot your system.
```
sudo reboot
```
After rebooting, your network interfaces should be named using the traditional convention (e.g., wlan0, wlan1, eth0, etc.).

-tested by ringmast4r





# Temperature Management
While this device is built for passive cooling, running resource heavy software can still cause overheating. Here are some tips and tricks to help mitigate this issue

## Using thermald (Linux Only)
Linux thermal daemon (thermald) monitors and controls temperature in laptops, tablet PC's with the latest Intel sandy bridge and latest Intel CPU releases. Once the system temperature reaches a certain threshold, the Linux daemon activates various cooling methods to try to cool the system.
### Instalation
Arch:
```
sudo pacman -S thermald
or
yay -S thermald
```
Debian/Ubuntu:
```
sudo apt install thermald
```
### Start and Endable
Systemd:
```
sudo systemctl enable thermald
sudo systemctl start thermald
```
Openrc:
(For distros using Openrc, thermald is packaged as such "thermald-openrc")
```
sudo rc-service thermald start
sudo rc-update add thermald default
```





