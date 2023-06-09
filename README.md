# azure-network-protocols<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this lab, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1: Create Virtual Machines in Azure
- Step 2: Download Wireshark
- Step 3: Observe traffic via various protocols

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/K8P3sw0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, we create a resource group in Azure followed by two virtual machines. One running Windows 10, the other running an Ubuntu server. We set them to access the same resource group, use the same region, and share the same network. Next, we can remotely connect into the Windows 10 VM. 
</p>
<br />

<p>
<img src="https://i.imgur.com/257YKX9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After connecting to the Windows 10 VM, navigate to the Wireshark website and download it. This will allow us to see our network traffic between both of our Virtual Machines by analyzing packets. We will download the Windows 64 installer and follow its directions. 
</p>
<br />

<p>
<img src="https://i.imgur.com/kiE8lmQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Wireshark, filter traffic through various protocols such as ICMP, SSH, DHCP, etc. 
Started by grapping the private IP address of the Ubuntu Server VM and pinging it then monitoring ICMP traffic. 
We can do the same for DNS for example by using nslookup in the command line for a website and observing the traffic through the DNS filter.
</p>
<br />
