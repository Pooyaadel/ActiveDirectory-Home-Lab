<h1> Active Directory Home Lab <h1/>
<h2>Description</h2>
I set up a HomeLab environment using VirtualBox to practice running Active Directory. This involved configuring DHCP for the Domain Controller, adding users to AD through a pre-set PowerShell script for educational purposes, and joining a client server machine to the Domain. This project demonstrates my proactive approach to learning and my commitment to enhancing my technical skills.
<br />


<h2>Languages Used</h2>

- <b>PowerShell</b>

 <p align="center">
Powershell Script to Use:
<img src= "https://i.imgur.com/mYPAEwy.png"/>


<p align="center">
Dummy List of names that will be used by PowerShell Script to create and Add Users:
<img src= "https://i.imgur.com/VJqFz9A.png"/>


<h2>What Exactly does the powershell script do?</h2>
  <p>For Learning purposes, I utilized a pre-made PowerShell Script found online and incorporated it into my Home Lab for Active Directory Purposes </p>




 <p> 1.) $password = ConvertTo-SecureString $PASSWORD_FOR_USERS -AsPlainText -Force
<p> - Converts a password into a secure string which ensures that sensitive information is being handled properly </p>

 <p> 2.) New-ADOrganizationalUnit -Name _USERS -ProtectedFromAccidentalDeletion $false
 <p> - Creates an Organzational Unit(OU) and organizes users into a speciic containter streamlining policy and user management</p>

 <p> 3.) foreach ($n in $USER_FIRST_LAST_LIST) {
  <p> - Loops through the user list and and iterates each user in the list to automate handling multiple users </p>

 <P> 4.) $first = $n.Split(" ")[0].ToLower() $last = $n.Split(" ")[1].ToLower()
      <p> - Splits the full name into first and last name to create a consistent format</p>
      
  <p> 5.) $username = "$($first.Substring(0,1))$($last)".ToLower()</p> 

   <p> -Creates username by combining the first letter of the firstname with the last name essential for user identification </p>

   <p> 6.)                    </p>



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
