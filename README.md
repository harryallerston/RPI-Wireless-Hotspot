RPI-Wireless-Hotspot
====================

Configures your Raspberry Pi with an attatched WiFi dongle or a Raspberry Pi3 with built in WiFi as a hotspot,
broadcasting your ethernet connection to other devices. Could be useful in hotel rooms, college dorms
or if you just don't feel like buying a router!


Features:
---------
* Hotspot automatically starts on boot without extra configuration.

* Configured WiFi network uses WPA encryption.

* The default SSID is "RaspberryPiFi" and the WPA key is "0123456789A," which can be changed during installation.

* Pi's local network functions continue to operate normally after setup.

* Easy setup of custom or preconfigured DNS server, including unblock-us for bypassing Netflix geoblocks.

* Router enumeration for WiFi network.

* Enables Chromecast compatibility with unblock-us by intercepting Google's DNS requests on the Pi.


Requirements:
-------------

1. A Raspberry Pi model B or Pi3 running raspbian

2. A Raspbian compatible Wifi adapter. This script assumes that your adapter uses the nl80211 drivers in hostapd (the majority of new products should support this). Others can be made to work, but require a custom compilation of hostapd (guides are out there).

3. An active ethernet connection


Installation:
-------------

* In the terminal, run:
    `git clone https://github.com/harryallerston/RPI-Wireless-Hotspot.git`

* Navigate to folder, and execute: `sudo ./install`

* Confirm that you are happy for changes to be made

* Choose a preconfigured DNSalternative DNS or configure a custom DNS

* If you require chromecast support with unblock-us select the appropriate option

* This should automatically set everything up and leave you ready to go


Notes and configuration
-----------------------

* To change default WiFi channel, edit /etc/hostapd/hostapd.conf accordingly.

* This setup has been tested on a fresh install of raspbian.

* It is advised that this be set up on a fresh install.

* If set up on an existing install then any current config files will be backed up with the extension ".old" in the relevant folders prior to installation. (this allows returning to original network settings if required)

