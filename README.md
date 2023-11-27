# HomeLab
Home Lab
Originally, it was just my pen test vm lab. 
And a library of vulnerable machines and OS's. 
All the data is real from my actual daily computer and gaming computer. 
My next step is to add the iptables to draw websites for my Burp Pro. 


# Design

![(./img/Network Design.jpg)](https://github.com/georgekovachjr/HomeLab/blob/main/img/Network%20Design.png)



# Tools
Router - DD WRT on a Nighthawk Router with PIA VPN and iptables to mirror
Hypervisor - VMWare ESXi on an HP z420 Server with 50 VM's of various types
SIEM - SecurityOnion
IDS/IPS - Snort 2 on Debian 11
Firewall - pfSense


# Windows Integration Script
$ProgressPreference = 'SilentlyContinue'
Invoke-WebRequest -Uri https://artifacts.elastic.co/downloads/beats/elastic-agent/elastic-agent-8.10.4-windows-x86_64.zip -OutFile elastic-agent-8.10.4-windows-x86_64.zip
Expand-Archive .\elastic-agent-8.10.4-windows-x86_64.zip -DestinationPath .
cd elastic-agent-8.10.4-windows-x86_64
.\elastic-agent.exe install --url=https://192.168.1.111:8220 --enrollment-token=bTRCVENvd0JCYVhfVVVJXzZrVXc6Q1Rlbm51WGZRUUtOVDhFWDl0dmlNZw== --insecure

# Router
![(./img/DD WRT Log.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/DD%20WRT%20Log.png)
![(./img/DD WRT Nighthawk Router.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/DD%20WRT%20Nighthawk%20Router.png)
![(./img/DD WRT VPN.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/DD%20WRT%20VPN.png)
![(./img/DD WRT iptables.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/DD%20WRT%20iptables.png)


# ESXi
![(./img/Home Server ESXi.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/Home%20Server%20ESXi.png)
![(./img/ESXi VM List 1.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/ESXi%20VM%20List%201.png)
![(./img/ESXi VM List 2.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/ESXi%20VM%20List%202.png)
![(./img/ESXi VM List 3.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/ESXi%20VM%20List%203.png)

# SIEM/IPS/IDS/Firewall
![(./img/SecurityOnion.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/SecurityOnion.png)
![(./img/SecurityOnion Integration.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/SecurityOnion%20Integration.png)https://github.com/georgekovachjr/HomeLab/blob/main/img/SecurityOnion%20Integration.png
![(./img/pfSense.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/pfSense.png)https://github.com/georgekovachjr/HomeLab/blob/main/img/pfSense.png

# VM's Locally
![(./img/Workstation VMs.png)](https://github.com/georgekovachjr/HomeLab/blob/main/img/Workstation%20VMs.png)https://github.com/georgekovachjr/HomeLab/blob/main/img/Workstation%20VMs.png
