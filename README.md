<p align="center">
  
    <b>[Orange Pi Lite] Using micro USB OTG as host for usb camera</b><br />
    Posted by yam1  Posted February 2, 2019   
	
	Thanks to everyone for the work here, so if you use armbian-add-overlay on the created file below,  it should just work in the future.               usbotg2host.dts  

    https://forum.armbian.com/topic/8686-orange-pi-lite-using-micro-usb-otg-as-host-for-usb-camera/?do=findComment&comment=71634
	
	https://forum.armbian.com/topic/8686-orange-pi-lite-using-micro-usb-otg-as-host-for-usb-camera/

</p>


## Installation

Logged in as root

armbian-config

toggle usb on (when saved * should stay )
<img width="300" height="300" src="https://github.com/carl1961/Orange-PI-Lite-Usb-OTG-to-Host/blob/main/usb.PNG">
 

 This is how I was able to install using ssh terminal (putty)
 
 
 root@orangepilite:~#
 wget    https://github.com/carl1961/Orange-PI-Lite-Usb-OTG-to-Host/raw/main/usbotg2host.dts

  armbian-add-overlay usbotg2host.dts
  
  
  
  
  Results: gave power to OTG port  (USB Host not working)
  
  
  
  
root@orangepilite:~# armbian-add-overlay usbotg2host.dts

Compiling the overlay

Copying the compiled overlay file to /boot/overlay-user/

Reboot is required to apply the changes

root@orangepilite:~#


    wget      https://github.com/carl1961/Orange-PI-Lite-Usb-OTG-to-Host/raw/main/sun8i-h3-orangepi-lite.dts


    armbian-add-overlay sun8i-h3-orangepi-lite.dts
	
	
	
Results:   Usb Host working on OTG mini plug

root@orangepilite:~# armbian-add-overlay sun8i-h3-orangepi-lite.dts

Compiling the overlay

Copying the compiled overlay file to /boot/overlay-user/

Reboot is required to apply the changes

root@orangepilite:~#

usb key board and Touchscreen on main usb ports

Last login: Sat Oct  3 00:44:02 2020 from 192.168.1.8

root@orangepilite:~# lsusb

Bus 008 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 005 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 007 Device 003: ID 413c:2001 Dell Computer Corp. Keyboard HID Support

Bus 007 Device 002: ID 413c:1001 Dell Computer Corp. Keyboard Hub

Bus 007 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 004 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 006 Device 002: ID 0eef:0005 D-WAV Scientific Co., Ltd

Bus 006 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 002 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 009 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Keyboard removed


root@orangepilite:~# lsusb

Bus 008 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 005 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 007 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 004 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 006 Device 002: ID 0eef:0005 D-WAV Scientific Co., Ltd

Bus 006 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 002 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 009 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Key board on mini usb (OTG set to Host)

root@orangepilite:~# lsusb

Bus 008 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 005 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 007 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 004 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 006 Device 002: ID 0eef:0005 D-WAV Scientific Co., Ltd

Bus 006 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 002 Device 003: ID 413c:2001 Dell Computer Corp. Keyboard HID Support

Bus 002 Device 002: ID 413c:1001 Dell Computer Corp. Keyboard Hub

Bus 002 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub

Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 009 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

root@orangepilite:~#



	
	
