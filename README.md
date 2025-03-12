<h1> Active Directory Home Lab <h1/>
<h2>Description</h2>
Created a HomeLab environment using VirtualBox to practice running Active Directory. This involved configuring DHCP for the Domain Controller, adding users to AD through a pre-set PowerShell script for educational purposes, and joining a client server machine to the Domain. This project demonstrates my proactive approach to learning and my commitment to enhancing my technical skills.
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




 <p> 1.) $PASSWORD_FOR_USERS = "Password1"
<p> - This sets a default password (Password1) for all the users being created simplifyting the process of setting up multiple users with the same initial password. </p>

 <p> 2.) $USER_FIRST_LAST_LIST = Get-Content .\names.txt:

 <p> -This reads a list of names from a file called names.txt located in the same directory as the script and create users based on a list of names, making the script reusable for different sets of users. </p>

 <p> 3.)$password = ConvertTo-SecureString $PASSWORD_FOR_USERS -AsPlainText -Force
  <p> - This converts the plain-text password (Password1) into a SecureString, which is a secure way to handle passwords in PowerShell.</p>

 <P> 4.)New-ADOrganizationalUnit -Name _USERS -ProtectedFromAccidentalDeletion $false

   <p> -This creates a new Organizational Unit (OU) in Active Directory named _USERS.OUs are used to organize and manage user accounts in AD. This script places all newly created users in the _USERS OU for easier management. </p>
      
  <p> 5.) foreach ($n in $USER_FIRST_LAST_LIST) {</p> 

   <p> -This starts a loop that processes each name in the $USER_FIRST_LAST_LIST array (from names.txt). Essentially It allows the script to handle multiple users dynamically </p>

   <p> 6.)  $first = $n.Split(" ")[0].ToLower()
            $last = $n.Split(" ")[1].ToLower()             </p>
   <p>                                                      </p>



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
