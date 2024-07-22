<h1>Active Directory Home Lab</h1>

<h2>Description</h2>
In this project I create a miniature corporate network environment using Oracle VM VirtualBox and add 1k+ user to Active Directory using a Powershell script. The corporate environment consists of a Domain Controller running Windows Server 2019 and a Client PC running Windows 10. The Domain Controller will be where I add the users via Active Directory and it will also serve as the DHCP server. The Client PC represents an end user PC in a corporate network.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle VM VirtualBox</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Windows Server 2019</b>

<h2>Program walk-through:</h2>

<p align="center">
Create the Domain Controller VM running Windows Server 2019: <br/>
<img src="https://imgur.com/R3mUcjc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Give the Domain Controller two Network Adapters. One which connects to the Public Internet, and one that connects to the corporate Intranet (shown below):  <br/>
<img src="https://imgur.com/3BpCnmq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure the Internal Network Adapter IP settings: <br/>
<img src="https://imgur.com/P225X4b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Promoting the Server to a Domain Controller:  <br/>
<img src="https://imgur.com/YLd2QDX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create an Admin group in Active Directory. Below I have add myself as an admin:  <br/>
<img src="https://imgur.com/hadDUFU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I add my account to the Domain Admins group in AD:  <br/>
<img src="https://imgur.com/wLtidhd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Log into the domain admin account (notice MYDOMAIN has appeared below with password):  <br/>
<img src="https://imgur.com/WyemxD2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure RAS and NAT:  <br/>
<img src="https://imgur.com/2qz5XE9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Establish the scope of the DHCP server (which is simultaneously the Domain Controller):  <br/>
<img src="https://imgur.com/v08LlTL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add 1k Users to Active Directory using a Powershell script, pulling from a names.txt file:  <br/>
<img src="https://imgur.com/wBB18cM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1k+ Users have been created in Active Directory using the Powershell Script:  <br/>
<img src="https://imgur.com/gGI1QXD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create the Windows 10 VM names Client1 in Oracle VirtualBox:  <br/>
<img src="https://imgur.com/Gdp4v3w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here is the virtualized network with the Domain Controller and the Windows 10 client machine interfacing with it and gaining access to the internet through it:  <br/>
<img src="https://imgur.com/PWWoTmO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ping www.google.com to verify internet connectivity and proper DNS setting on DHCP server:  <br/>
<img src="https://imgur.com/zKsgFab.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Change the computer name and join it to the domain at the same time:  <br/>
<img src="https://imgur.com/3w95a7l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here is the client computer listed in Address Leases in the DHCP and in Active Directory settings on the Domain Controller:  <br/>
<img src="https://imgur.com/YYsTlHp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Login to the client computer with one of the 1k user credentials added via Active Directory:  <br/>
<img src="https://imgur.com/0Uiyam1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here you can see the successful login as user dearls which demonstrates the successful functioning of the network infrastructure:  <br/>
<img src="https://imgur.com/FuUO2YH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
