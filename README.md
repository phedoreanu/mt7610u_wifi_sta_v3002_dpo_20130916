# mt7610u_wifi_sta_v3002_dpo_20130916

I've recently bought a Raspberry Pi 2 and attached a `MT7610U`/`AC600` [5Ghz nano USB dongle](http://www.amazon.co.uk/dp/B00VHB0EW0).

This dkms-module supports these chipsets:
* `mt7650u`
* `mt7630u`
* `mt7610u`

It's using the official [Mediatek](http://www.mediatek.com/en/downloads/mt7601u-usb/) driver along with two other patches:
* `kuid_t-kgid_t.patch`
* `__DATE__ & __TIME__macro-warning.patch`

to fix compilation issues.

Modified usb wifi driver for TP_link TL-WDN5200 on Linux. 
1. modified:   common/rtusb_dev_id.c 
 * add product id for TL-WDN5200
1. modified:   include/os/rt_linux.h 
1. modified:   os/linux/rt_linux.c
 * fix compile error from struct _OS_FS_INFO_
 * fix problem on 64bit
1. modified:   os/linux/config.mk
 * change default setting for Ubuntu 

# how to use
```
$ make
$ make install
$ reboot
```
refer to： http://hprath.com/2014/06/cisco-linksys-ae6000-ac580-media-tek-mt7610u-mt7630u-mt7650u-linux-x64-driver-patch/

