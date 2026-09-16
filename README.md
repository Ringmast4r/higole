<div align="center">

<img width="100%" alt="HIGOLE" src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,100:1F3A6F&height=220&section=header&text=HIGOLE&fontSize=60&fontColor=ffffff&animation=twinkling&fontAlignY=35&desc=Windows%20%7C%20Linux%20%7C%20Markdown%20%7C%20Hardware&descSize=16&descAlignY=58"/>

`Windows` `Linux` [`Markdown`](https://www.markdownguide.org/) `Hardware` - Community support resource for Higole Gole 1 Pro 5.5" Industrial Tablet Mini PC. Hardware specs, Windows/Linux setup guides, WiFi drivers, temperature management, and compatibility documentation.

[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=20&pause=1000&color=1F3A6F&center=true&vCenter=true&multiline=true&repeat=true&width=950&height=90&lines=Community+support+resource+for+Higole+Gole+1+Pro+5.5%22+Industrial+Tablet...%3BWindows+%2F+Linux+%2F+Markdown+%2F+Hardware)](https://git.io/typing-svg)

<br>

[![Project](https://img.shields.io/badge/Project-higole-1F3A6F?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Ringmast4r/higole)
[![Format](https://img.shields.io/badge/Format-Linux-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Ringmast4r/higole/tree/main)

[![Stars](https://img.shields.io/github/stars/Ringmast4r/higole?style=flat-square&color=1F3A6F)](https://github.com/Ringmast4r/higole/stargazers)
[![Forks](https://img.shields.io/github/forks/Ringmast4r/higole?style=flat-square&color=1F3A6F)](https://github.com/Ringmast4r/higole/network/members)
[![Repo Size](https://img.shields.io/github/repo-size/Ringmast4r/higole?style=flat-square&color=1F3A6F)](https://github.com/Ringmast4r/higole)
[![Last Commit](https://img.shields.io/github/last-commit/Ringmast4r/higole?style=flat-square&color=1F3A6F)](https://github.com/Ringmast4r/higole/commits/main)

</div>

---

# Gole Gang unofficial support team here to take your request



# Specifications 
Higole Gole 1 Pro 5.5" Industrial Tablet Mini PC

<a id="hardware"></a>
## `> hardware`
|   Hardware  |     Details       |  
|-------------|-------------------|
| Display     |  5.5" 720*1280(IPS)|
|    CPU      |  Intel Celeron J4125| 
|    GPU      |  Intel HD600     |
|   Memory   |  8GB LPDDR4       |
| Storage   |     128GB eMMC  |
| WIFI 6.0       | Realtek RTL8852BE    |
| Bluetooth 5.2   |  Realtek RTL8852BE  |
| Battery     |     2500mAh LiPo |
| Dimensions |  	142×91×19mm |

<a id="io"></a>
## `> io`
|  Interface |    Details   |
|------------|---------------|
|   USB      |    x4 USB 3.0|
|  SD Card Reader |   x1 (Up To 128GB) |
|  Audio Jack |   x1 3.5mm   |
|   HDMI     |   x2 HDMI 1.4  |
|   RJ45    |    x1 1000Mbps GB Lan |
| Type-C(Charging Only) | x1 Type-C 3.1 DC 12V/3A |

<a id="working"></a>
## `> working`
| Hardware | Windows 10  | Windows 11  |   Linux 6.0+  |
|---------|--------------|--------------|----------|
|  wifi   |  ✓           |  ✓           |    x     |
|Bluetooth|  ✓           |   ?          |    ?     |
|Touchscreen|  ✓           |  ✓         |   ✓      |
| Sound   |  ✓           |    ✓         |   x      |

# Build Guides

[Windows 10](Win_10_build_guide.md)

# Accessories
<a id="possible-case-options"></a>
## `> possible_case_options`
- https://a.co/d/go6dnKG
- https://a.co/d/9tBpxil
- https://a.co/d/aZ67kRv
- https://a.co/d/hxNJGWD (image of use in ig group)
- https://a.co/d/iCT9XTF
- https://a.co/d/1aHPJct
- https://a.co/d/cUuw2CU
- pelican 1040 (tested by Off Grid)


# WiFi

<a id="drivers"></a>
## `> drivers`
Drivers for the Fn-Link 6252C-PUB Wi-Fi6 Module (Realtek RTL8852BE)

Windows 11: https://golerugged.com/supports/335.html

Linux: https://github.com/lwfinger/rtw89 (NEEDS WORK)

Open issue with driver maintainer can be found here https://github.com/lwfinger/rtw89/issues/242


<a id="change-wifi-name-back-to-wlan0-wlan1"></a>
## `> change_wifi_name_back_to_wlan0_wlan1`
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
```
Arch:

sudo pacman -S thermald
or
yay -S thermald

Debian/Ubuntu:

sudo apt install thermald
```
### Start and Endable
```
Systemd:

sudo systemctl enable thermald
sudo systemctl start thermald

Openrc:
(For distros using Openrc, thermald is packaged as such "thermald-openrc")

sudo rc-service thermald start
sudo rc-update add thermald default
```
## Hardware Hacks For Cooling

---

<div align="center">

<img width="100%" alt="HIGOLE footer" src="https://capsule-render.vercel.app/api?type=waving&color=0:1F3A6F,100:000000&height=120&section=footer&text=RINGMAST4R%20%2F%2F%20HARDWARE&fontSize=18&fontColor=ffffff&fontAlignY=65"/>

</div>
