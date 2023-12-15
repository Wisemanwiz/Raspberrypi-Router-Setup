<h1>Raspberrypi-AP-Setup</h1>
<h2>Description</h2>

This process serves as a continuation of my initial task, wherein I successfully created an Access Point (AP) using a Raspberry Pi. However, I encountered difficulty establishing internet connectivity. This task details how I enabled routing on my Raspberry Pi, transforming it into a functional router.

The process commenced by enabling IP forwarding on the Raspberry Pi. IP forwarding allows network traffic to pass from one interface to another, effectively bridging connections. To implement this, I checked the sysctl configuration file for `# net.ipv4_forward=1`. Specifically, I directed the system to forward IPv4 traffic between `eth0` (interface for the ISP router) and `wlan0` (the Raspberry Pi's wireless interface).

To apply these changes to the kernel, I utilized the `sysctl -p` command. Subsequently, I installed Netfilter-persistent and IP tables persistent—a Debian-based Linux system that ensures the persistent retention of firewall rules across system reboots. This step is crucial to maintaining consistent firewall configurations.

Moving forward, I employed iptables to set up Network Address Translation (NAT). NAT is responsible for translating private IP addresses to public addresses, enabling devices connected to the Raspberry Pi (acting as a router) to access the internet. To ensure the iptables rules persist through reboots, I edited the `/etc/rc.local` file.

It's worth noting that Dnsmasq and Dhcpcd were already configured in my previous task. As a final validation, I initiated and checked the status of Dhcpcd to confirm its functionality. The task culminated with a successful ping test to my DNS network, specifically raspberryos.


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
<br />
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
