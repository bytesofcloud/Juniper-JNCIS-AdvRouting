<h1>******** README ********<br>
******** JUNIPER JNCIS ADV. ROUTING LAB &amp; CONFIGS ********</h1>

This series of configurations were configured for the JUNIPER JNCIS-ENT examination topics. These configurations should help the student understanding of the topic and provide an option to adjust the configuration values to understand traffic patterns.

<b>//// HARDWARE | SOFTWARE SPECIFICATIONS \\\\</b><p>
<i> Virtualized Network Devices:</i>
<blockquote>
Vendor:: Juniper<br>
Model:: vMX<br>
OS Version:: Junos: 19.1R3.9 <br>
Virtualization Platform:: <br>
Application: EVE-NG COMMUNITY <br>
Version: 2.0.3-112, QEMU 2.4.0<p>
</blockquote>

<i>System Hardware/Environment:</i>
<blockquote>
Host: 		EVE-NG Kernel: 4.20.17-eve-ng-ukms+ x86_64 (64 bit) Console: tty 2 Distro: Ubuntu 16.04 xenial <br>
<b>Machine Details:</b><br>
System: 	LENOVO product: 30B5005XUS v: ThinkStation P510<br>
Mobo: 		LENOVO model: 102F Bios: LENOVO v: S00KT40A date: 05/04/2017<br>
CPU:       	Hexa core Intel Xeon E5-1650 v4 (-HT-MCP-) speed/max: 1809/4000 MHz<br>
Graphics:  	Card: NVIDIA GP106GL [Quadro P2000], Display Server: N/A driver: N/A tty size: 160x46 Advanced <br>
Network:   	Card: Intel Ethernet Connection (2) I218-LM driver: e1000e<br>
Drives:    	HDD Total Size: 1024.2GB<br>
</blockquote>
<p>
This lab is based on a bare metal install of the EVE-NG Community Edition. It may be run within VMWare Workstation and other hypervisors. Resource utilization, on above server specifications, for this lab/system:

<p><blockquote>
  CPU: 		78%<br>
  MEM: 		53%<br>
  SWAP: 		87%<br>
  QEMU Nodes: 22<br>
</blockquote>
<p>

<b>//// CODE REQUIREMENTS \\\\</b>

To obtain the JUNOS code, you will need to create an account at <a target=_blank href="HTTPS://WWW.JUNIPER.NET" rel="nofollow">HTTPS://WWW.JUNIPER.NET</a>. Virtual code contains certain restrictions and is regulated by the vendor.
<p>
<b>//// LAB DESCRIPTION \\\\</b><p>
This lab focuses on layer-3 route/switching across two data centers and a backbone network. This lab focuses on layer-3 connectivity and may be modified to support BGP, IS-IS, and OSPF deployments. If you are studying for the JNCx certification, this lab will provide a "standard" deployment where you may customize, destroy, and then spin up. It's good to get familiar with all the options.
<p>
  <i>Lab Requirements/Objectives:</i>
  <ul>
    <li> Deploy IPv4 addressing for WAN/LAN links</li> 
    <li> Exchange full routes with all devices</li> 
    <li> Leverage route policies to control backbone and edge route advertisements</li> 
    <li> Deploy IPv6 addresses and consider address allocation</li> 
    <li> Advertise IPv6 addresses for route convergance</li> 
    <li> Practice IPv4 and IPv6 tunneling methodologies</li>  
  </ul>
  <p>

<i>Lab Details:</i>
<p>
  <b><i>Management interfaces:</i></b>
<blockquote>
<ul>
  <li>CSR1/VCP1: 192.168.21.101<br></li>
  <li>CSR2/VCP2: 192.168.21.102<br></li>
  <li>CSR3/VCP3: 192.168.21.103<br></li>
  <li>CSR4/VCP4: 192.168.21.104<br></li>
  <li>CSR5/VCP5: 192.168.21.105<br></li>
  <li>CSR6/VCP6: 192.168.21.106<br></li>
  <li>CSR7/VCP7: 192.168.21.107<br></li>
  <li>CSR8/VCP8: 192.168.21.108<br></li>
  <li>CSR9/VCP9: 192.168.21.109<br></li>
  <li>CSR10/VCP10: 192.168.21.110<br></li>
  <li>CSR11/VCP11: 192.168.21.111<br></li>
 </ul>
<ul>
  <li> WAN: 2001:db8:cafe::/48</li>
  <li> Loopback: 2001:db8:cafe::a:/96</li>
</blockquote>
<p>
  <b><i>Subnet IP Scheme:</i></b>
<ul>
  <li>WAN Links: 172.16.255.0/24 (Subdivide to /30)</li>
  <li>Loopback Interfaces: 10.255.255.0/24 (Subdivide to /32)</li>
  <li>VLANs: 192.168.0.0/16 (Subdivide to /24)</li>
</ul><p>
<b><i>Lab User Accounts (username / password)</b></i>
  <ul>
    <li>root / abc123</li>
    <li>admin / abc123</li>
  </ul><p>
<b>//// VENDOR GUIDES \\\\</b>
<p><a target=_blank href="https://support.juniper.net" rel="nofollow">Juniper Support </a></p>
<p><a target=_blank href="https://learningportal.juniper.net" rel="nofollow">Juniper Learning Portal</a></p>
<p><a target=_blank href="https://www.eve-ng.net/index.php/documentation/" rel="nofollow">EVE-NG Documentation</a></p>

<b>//// LAB IMAGE \\\\</b>

![Juniper-JNCIS-OSPF](https://user-images.githubusercontent.com/40407552/140651742-e9e7e60b-9425-4c3e-8ae7-c6e97fbbb3f5.jpg)
