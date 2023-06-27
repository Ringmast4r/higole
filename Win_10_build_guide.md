# Windows 10 Build Guide

Upon a successful installation of Windows 10, you will see the following missing drivers in Device Manager:

![Missing Drivers in Device Manager](images/device_manager_fresh_install_win_10.png)

# Windows Update

Because the wifi driver is not yet installed, we must use wired ethernet via the RJ45 jack to connect to the internet.

Begin by running Windows Update and installing all missing updates until the system is completely up to date.

Start -> Settings -> Update & Security -> Check for Updates

# Wifi Driver

The wifi driver can be downloaded from the HiGole webstie here: https://golerugged.com/supports/335.html

![Higole Gole1 Pro Wifi Driver](images/install_wifi_driver.png)

Run setup.exe inside the Wifi folder to install the driver

The missing driver for "Network Controller" should now be satisfied and removed from the list.  You can now switch from wired to wireless.

![Higole Gole1 Pro Wifi Driver Installed](images/after_wifi_driver_install.png)

# Sound Card Driver

The Sound Card Driver can be downloaded from the HiGole website here: https://golerugged.com/supports/333.html

![Higole Gole1 Pro Sound Card Driver](images/Sound_card_driver.png)

Right click "InstallPackage.bat" and click "Run as Administrator"

The results will not be visible in the missing drivers in Device Manager as sound was already partially working out of the box.

# Optional Windows Updates

Installing optional windows updates will satisfy all but 3 of the remaining missing drivers.

Start -> Settings -> Update & Security - > View optional updates

![Higole Gole1 Pro Optional Windows Updates](images/Optional_windows_updates.png)

Device Manager should now look like this:

![Higole Gole1 Pro After Optional Windows Updates](images/After_optional_updates.png)

# Goodix Touch Driver (TouchScreen)

One of the two remaining "Unknown device" requires the Goodix Touch Driver which can be downloaded from the HiGole website here: https://golerugged.com/supports/336.html

![Higole Gole1 Pro Touch Driver](images/Touch_driver.png)

This driver must be manually installed.  Double click one of the "Unknon device" in Device Manager and click the "Update Driver" button then click "Browse my computer for drivers" and select the folder where you have extracted the driver.  If this fails, repeat the process with the other "Unknown Device".

# Gravity Sensor (Accelerometer)

The accelerometer driver, which allows the device to auto rotate between portrait and landscape, can be downloaded here: https://golerugged.com/supports/337.html

![Higole Gole1 Pro Accelerometer Driver](images/Accelerometer_driver.png)

This driver must be manually installed.  Double click the "Unknon device" in Device Manager and click the "Update Driver" button then click "Browse my computer for drivers" and select the folder where you have extracted the driver.

# On Screen Keyboard

The on screen keyboard can be acessed on the login page by clicking the "Ease of access" button in the bottom right and selecting ""On-Screen Keyboard"

![Higole Gole1 Pro On-Screen Keyboard Login](images/Onscreen_keyboard_login_screen.png)

The keyboard can then be used by opening the notifications pane and enabling Tablet mode

![Higole Gole1 Pro On-Screen Keyboard Tablet Mode](images/tablet_mode.png)

# Remote Desktop

To enable Remote Desktop, go to Start -> Settings -> System -> Remote Desktop and set to yes
