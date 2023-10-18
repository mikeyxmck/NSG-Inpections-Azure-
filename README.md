# NSG-Inpections-Azure
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Creating our Resources in Azure
- Observe The ICMP Traffic
- Observe the SSH Traffic
- Observe the DHCP Traffic
- Observe the DNS Traffic
- Observe the RDP Traffic

<h2>Actions and Observations</h2>

<p>

<img src="https://i.imgur.com/KE4PZht.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/STqEe7H.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/wfG4u8a.png" height="80%" width="70%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/GjY25a7.png" height="80%" width="70%" alt="Disk Sanitization Steps"/>

</p>
<p>
1) Go to portal.azure.com, and create Resource Group, this is where we will put our Virtual Machines.

2) The next step is to make your first VM, we will name it VM1 and select Windows 10 for the Operating System, select the previously made Resource Group and allow the VM to create a new Vnet, and Subnet.

3)For the Second VM will we name it VM2 and choose Linux (Ubuntu) for the Operating System. Choose the same Resource Group, and Vnet as VM1.

</p>
<p>
  <img src="https://i.imgur.com/InBuT70.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
</p>
<p>
  4) Afterwards go back to your Resource Group and check to see if your VMs are there. It should look something like the picture above.
</p>

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
