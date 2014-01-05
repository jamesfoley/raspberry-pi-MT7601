Raspberry Pi MediaTek MT7601
============================

Drivers for the MediaTek MT7601 USB Wifi adaptor.

1. Copy mt7601Usta.ko to /lib/modules/3.10.25/kernel/drivers/net/wireless

2. Copy RT2870STA.dat to /etc/Wireless/RT2870STA directory

3. Run sudo depmod -a

4. Add the below text to /etc/network/interfaces. Note that quotes around SSID and password are required
```
auto ra0
allow-hotplug ra0
iface ra0 inet dhcp
wpa-ssid "ENTER YOUR NETWORK SSID"
wpa-psk "ENTER YOUR NETWORK PASSWORD"
```



References:

http://gowthamgowtham.blogspot.co.uk/2013/11/mediatekralink-wifi-adapter-in.html

http://www.raspberrypi.org/phpBB3/viewtopic.php?p=179845#p179845
