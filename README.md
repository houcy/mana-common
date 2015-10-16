# Mana Common SSID's
Uses Mana to Broadcast 7 popular SSID while turning Karma off to demonstrate the danager of having wireless networks saved on your phone.  

# What this does?

It broadcasts 7 SSID's at one time using the [CanaKit Ralink 5370 Chipset USB Wireless Card](http://www.amazon.com/dp/B00GFAN498/). 

I have it configured to broadcast: 
+ attwifi
+ dlink
+ belkin54g
+ NETGEAR
+ iPhone
+ linksys
+ xfinitywifi

#Demo 

![Demo Gif](https://raw.githubusercontent.com/jgamblin/mana-common/master/manacommon.gif)

#Installation

[Install and configure mana.](https://github.com/sensepost/mana)

cp dhcp-common.conf /etc/mana-toolkit/

cp hostapd-common.conf /etc/mana-toolkit/

cp start-nat-full-common.sh /?/run-mana/ 

cp start-nat-simple-common.sh /?/run-mana/


#Running
./start-nat-simple-full.sh

./start-nat-simple-common.sh

#Notes
./start-nat-simple-common.sh works with basic passs throuhg. 

./start-nat-full-common.sh works by creating a eth0:1 virtual interface.

These scripts assume that your wirless card that allows this many APs is WLAN1.  You may have to tweak it.  The TL-WN722N allows two SSID's if you want to edit it to use that. 
