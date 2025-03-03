![Network Diagram](https://github.com/ToothGrinderx/HomeNetwork/blob/main/networkdiagram.png)
# HomeNetwork
Design of my home network.

**Original Equipment:**  

TP-Link Archer AC1700 wi-fi router

**Upgraded Equipment:**

Protectli Vault V1210-2 Port running pfSense

TP-Link EAP610 - Wireless Access Point

TP-Link TL-SG108PE - 8 Port Switch

**Clients:**

Windows PC - Main computer

Dell G5505 SE - Fedora Linux

Synology DS223j - Network Attached Storage

**Network Upgrade:**

  Originally, I had a single wi-fi router supplying internet to all devices in my home. The router is fairly outdated, although it worked fine for general use I wanted to upgrade and enhance my network to allow for new devices and increased security. My network upgrade consisted of replacing the router and adding a firewall appliance, switch, and wireless access point. I chose the Protectli Vault as my firewall appliance, installed pfSense and began to setup my home network. I added firewall rules to ensure internet connection was established. The purpose of moving to pfSense was to have more control over my network and security posturing. Although most routers allow for these features, I found that being able to customize and monitor my network to my liking allowed me to practice networking and security skills at home. In order to heighten network security, within pfSense I configured a VPN with Private Internet Access, installed Snort, and pgBlockerNG.

>Snort: Intrusion Prevention/Dectection System - Allows me to monitor the network for suspicious traffic. Any anomolies can be reseached and blocked or suppressed if necessary.
>pfBlockerNG: Allows me to block website trackers to enhance online privacy. Stops websites and advertises from collecting personal data which allows them analyze browsing habits and preferences across the internet.
>VPN: Allows me to create a secure tunnel to further enhance my online privacy. 
  
  The next step was to re-establish a wireless network to allow for mobile devices to connect to the internet. Originally, the old router took care of this but the pfSense router/firewall does not have a wireless connection so I had to install an access point. I added the TP-Link EAP610 wireless AP to my network. It has a smaller form factor than a router and was able to be mounted in the ceiling where it is out of the way and discrete. It is powered over PoE provided by the switch.

  Finally, to tie everything together and create the network I installed a TP-Link TLSG108PE switch. The firewall is connected to this switch which establishes internet connection for any device that is also connected to the switch such as the wireless AP and my PC. The next project for this switch is to learn how to create VLANs to segregate the network futher. I would like to create a seperate guest network so they do not have network access to my devices but still able to connect to the internet.

**Clients:**

  I had an old Dell G5505 SE that I used as a gaming and study PC while I was in school. I decided to remove Windows from the device and install Fedora Linux. The purpose for this is to have a Linux device where I can get familiar with the operating system. I also installed Emby, a media server, on this device. 
  
  The Synology NAS is an entry level network attached storage device. It is only a 2-bay NAS with a fairly weak CPU and minimal RAM. Originally, I was hosting my Emby server on this device but migrated it to the Linux Laptop because it is far more powerful than the NAS and can handle transcoding and multiple streams where the NAS would struggle. The NAS works better as just a storage device.
