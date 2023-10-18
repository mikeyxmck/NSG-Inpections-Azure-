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
<img src="https://i.imgur.com/nsz4Msh.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/tDxSuMI.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
    <img src="https://i.imgur.com/SY6uY0B.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
    <img src="https://i.imgur.com/jnuetdS.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
     <img src="https://i.imgur.com/z2JqxST.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5)Go to your Remote Desktop Application and log into VM1, after logging in, download Wireshark.
  
6)Once inside Wireshark, filter for ICMP Traffic only, and retrieve the Private IP Address from the Linux VM (VM2) and ping it from withins Windows VM (VM1) using the Command Prompt Application.
</p>
<p>
<img src="https://i.imgur.com/4vNJzP9.png" "80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/AwRM30c.png" "50%" width="50%" alt="Disk Sanitization Steps"/>
   <img src="https://i.imgur.com/hffwmOo.png" "50%" width="50%" alt="Disk Sanitization Steps"/>
</p>

<p>
  7)Now we are going to mess around with the Network Secruity Groups inside the VMS, to test this we are going to go back to Command Prompt inside of VM1 and ping VM2 nonstop by typing 'ping 10.0.0.5 -t'.
  
  8) Next, we will go into VM2's NSG (Network Security Group) and disable incoming inbound (ICMP) Traffic. click to add a new inbound rule and set the Source and Destination to 'Any', then change the Protocol to ICMP and change the Action to Deny any incoming ICMP pings. If done correctly the ping should be timing out!

9) Next you will need to go back to VM2's NSG and reallow the ping and observe to see if it's pinging again inside of VM1's Wireshark/Command Prompt. Once you see that it's working again, stop the ping activity.
</p>
<br />

<p>
<img src="https://i.imgur.com/9cpnWEr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
</p>
<p>
10) Go back to wireshark and filter for SSH traffic only, then go into your command prompt and type 'ssh labuser@10.0.0.5' you should see the the traffic appear on both Wireshark and Command Prompt. Observe the traffic by using command prompts like, 'id', 'uname -a' 'pwd' once you are done with that, stop the traffic for SSH by typing 'exit' and pressing 'Enter.'
</p>

<p>
 <img src="https://i.imgur.com/smt7TO7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>

<p>
  11) The Next traffic will be observing is the DHCP Traffic, go into wireshark and change the fliter to DHCP. Then go into the Command Prompt and try changing the IP address by entering the 'ipconfig/renew' as the command.


  There you have it! We have looked through the Network Security Groups and have messed around with some of the command prompts and saw how the traffic was moving through each prompt! Make sure to clean up the lab and disconnect from your Virtual Machine!
</p>
<br />
