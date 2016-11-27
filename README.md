RPI-Wireless-Hotspot
====================

Configures your Raspberry Pi with an attatched WiFi dongle or a Raspberry Pi3 with built in WiFi as a hotspot,
broadcasting your ethernet connection to other devices. Could be useful in hotel rooms, college dorms
or if you just don't feel like buying a router!


Features:
---------

* Configured hotspot starts automatically on boot, no extra configuration necessary

* Configured WiFi network is WPA encrypted.

* Default SSID of "RaspberryPiFi" and WPA key of "0123456789A" can be modified during install

* Once set up, the local network facilites of the Pi will still operate as normal

* Easy setup of either a custom or preconfigured DNS server (including unblock-us for removing netflix geoblocks)

* Router enumeration for WiFi network

* Allows chromecast compatibility with unblock-us by intercepting google's DNS requests on the pi

Requirements:
-------------

1. A Raspberry Pi model B or Pi3 running raspbian

2. A Raspbian compatible Wifi adapter. This script assumes that your adapter uses the nl80211 drivers in hostapd (the majority of new products should support this). Others can be made to work, but require a custom compilation of hostapd (guides are out there).

3. An active ethernet connection


Installation:
-------------

* In the terminal, run:
    git clone https://github.com/unixabg/RPI-Wireless-Hotspot.git

* Navigate to folder, and execute "sudo ./install"

* Confirm that you are happy for changes to be made

* Choose a preconfigured DNSalternative DNS or configure a custom DNS

* If you require chromecast support with unblock-us select the appropriate option

* This should automatically set everything up and leave you ready to go


Notes and configuration
-----------------------

* To change default WiFi channel, edit /etc/hostapd/hostapd.conf accordingly

* This setup has been tested on a fresh install of raspbian.

* It is advised that this be set up on a fresh install

* If set up on an existing install then any current config files will be backed up with the extension ".old" in the relevant folders prior to installation (this allows returning to original network settings if required)

