<h1>Raspberrypi-AP-Setup</h1>
<h2>Description</h2>
I initiated the project by ensuring that my system's packages were up-to-date through the commands `apt update` and `apt upgrade`. Subsequently, I installed two key components: Hostapd, which facilitates the conversion of my device into an access point, and Dnsmasq, a software serving as a combined DNS and DHCP server.

To configure Dnsmasq, I specified the interface as wlan0, set up a DHCP range for the IP addresses to be assigned, and determined the lease time for each address. Additionally, I included domain information, such as the name of my Raspberry Pi, "raspberryos," and added a specific address.

Moving on, I installed Dhcpcd, a program designed to automatically obtain IP addresses from a DHCP server on the network. After installation, I configured Dhcpcd for wlan0, assigning a static IP address to my Raspberry Pi, specifying the subnet, static router (ISP router's IP address), static domain name, and a static IP range.

Next, I turned my attention to configuring Hostapd. In the configuration file, I specified the interface (wlan0), set the SSID (the name for my wireless network, in this case, "Brugoil"), chose hardware mode 'g' for a 2GHz network, selected channel 8, and set the country to Poland. For security, I opted for WiFi Protected Access 2 (WPA2) and defined a passphrase for network access.

To ensure these configurations took effect, I updated the Hostapd default file by specifying the path to the hostapd.conf file. I uncommented the line `DAEMON_CONF` and set it to `/etc/hostapd/hostapd.conf`. After saving the changes, I removed the comment symbol (#) from the line to activate the alterations.

To start the services, I first unmasked Hostapd, thereby removing any restrictions that prevented it from starting. I then initiated both Hostapd and Dnsmasq. Finally, to guarantee these services started during bootup, I adjusted the necessary settings.

The entire process was completed by rebooting the Raspberry Pi to ensure all changes took effect.

I hope this summary accurately captures the steps you will take in your project! 


<h2>Resources Provided</h2>

- <b>Raspberrypi 4B (Hardware)</b> 
- <b>Micro SD Card (32GB)</b>
- <b>Ethernet Cable</b>
- <b>ISP Router</b>

<h2>Environments Used </h2>

- <b>Home </b>

<h2>Program walk-through:</h2>

<p align="center">
Enable IP Forwarding: <br/>
<img src="https://i.imgur.com/XKDcuy4.png?1" height="80%" width="80%" alt="Task 1"/>
<br />
  <img src="https://i.imgur.com/P3B8kBu.png?1" height="80%" width="80%" alt="Task 1"/><br/>
   <img src="https://i.imgur.com/ymdcage.png?1" height="80%" width="80%" alt="Task 1"/>
  
  
<br />
Install Netfilter-Persistent And IP Tables Persistent:  <br/>
<img src="https://i.imgur.com/YM1weOZ.png?1" height="80%" width="80%" alt="Task 2"/>
<br />
<br />
Using IP Tables To Set Up NAT: <br/>
<img src="https://i.imgur.com/WbLEzGc.png?1" height="80%" width="80%" alt="Task 3"/><br/>
<img src="https://i.imgur.com/gTpdfnW.png?1" height="80%" width="80%" alt="Task 3"/><br/>
<img src="https://i.imgur.com/8kQewfW.png?1" height="80%" width="80%" alt="Task 3"/>
<br /><br/>
Start And Check Dhcpcd Status:  <br/>
<img src="" height="80%" width="80%" alt="Task 4"/>
<br /><img src="https://i.imgur.com/V14D9wY.png?1" height="80%" width="80%" alt="Task 4"/>
<br />
<br />
Reboot Raspberrypi:  <br/>
<img src="https://i.imgur.com/dAI3zg2.png?1" height="80%" width="80%" alt="Task 5"/>

<br />
Checking Connectivity:  <br/>
<img src="https://i.imgur.com/1TKXfia.png?1" height="80%" width="80%" alt="Task 6"/>
<br /><img src="https://i.imgur.com/E257snW.png?1" height="80%" width="80%" alt="Task 6"/>
<br />

</p>
