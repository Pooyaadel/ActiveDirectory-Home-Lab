<h1> Active Directory Home Lab <h1/>
<h2>Description</h2>
Project consists of using VirtualBox to set up a HomeLab Environment to practice running Active Directory, Configuring DHCP for the Domain Controller, Adding users to AD through a Powershell Script, and lasty joining in the Domain (DC) with the client server machine.
<br />


<h2>Languages Used</h2>

- <b>PowerShell</b> 


<h2>Environments Used </h2>

- <b>VirtualBox</b>
- <b>Windows 10 ISO <b/>
- <b> Server 2019 ISO

<h2>Walk-Through:</h2>

<p align="center">
Configure Ipv4 for the Internal Network (Domain Controller): <br/>
<img src= "https://i.imgur.com/6ajFemH.png"/>
<br />

 
<br />
<br />
Install Active Directory and Domain Services:  <br/>
<img src="https://i.imgur.com/hOLXilS.png" height="80%" width="80%" alt="Active Directory HomeLab"/>
<br />
<br />
Create an Organizational Unit for Domain Admins using AD: <br/>
<img src="https://i.imgur.com/HwUz0U9.png" height="80%" width="80%" alt="Active Directory HomeLab"/>

<br />
<br />
Install RAS(Remote Access Service)/NAT(Network Address Translation) to allow Windows 10 client on virtual network to be able to access the DC network:  <br/>
<img src="https://i.imgur.com/PQIogLH.png"/>
<br />
<br />
 Using a PowerShell Script to add in users into Active Directory:

 <br/>
<img src="https://i.imgur.com/zFifLaP.png" height="80%" width="80%" alt="Active Directory HomeLab"/>
<br />
<br />
 Create Windows 10 Client Server VM:  <br/>
<img src="https://i.imgur.com/GG7Rjks.png" height="80%" width="80%" alt="Active Directory HomeLab"/>
<br />
<br />
 <br/>

 Observe Confirmation of Client Server successfully joined into the DC:
<img src="https://i.imgur.com/DShFjwt.png" height="80%" width="80%" alt="Active Directory HomeLab"/>
 
<br />
<br />

Testing out by signing into Client Server with random name from account creation script in PowerShell (Suzanne Snell) 
<img src="https://i.imgur.com/vB4qV42.png" height="80%" width="80%" alt="Active Directory HomeLab"/>

</p>
