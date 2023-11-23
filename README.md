<p align="center">
<img src="https://i.pcmag.com/imagery/reviews/066pfhdQmzHcmyEMaZtToWq-77..v1653509931.jpg"/>
</p>

<h1>Proton Virtual Private Netowrk</h1>
This tutorial outlines the Setup and Usage of Virtual Private Networks using Proton VPN.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Proton VPN

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Resource Group
  ![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/26bbae34-e7b8-4772-a552-b7d205161ded)

- Create a Windows 10 Virtual Machine (VM) with 2 Virtual CPUs and a Linux (Ubuntu 20.04) Virtual Machine with 2 Virtual CPUs
  ![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/e39dda9e-885a-4774-82cb-50b96cf8eb77)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/d170dd36-d539-4a25-a15d-9d9237e708da)


<h2>Setup Steps</h2>


Install / Enable IIS in Windows WITH
CGI and Common HTTP Features

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/dbee9e2a-6a63-43fa-8f07-0f90a505b862)

</p>
<br />

Download and install PHP Manager for IIS and the Rewrite Module

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/6efedcd8-0bd6-4405-90e9-5125d6c944ea)



Create the directory C:\PHP

Download PHP and unzip the contents into C:\PHP

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/c4a5503b-b9d8-4fe0-8da5-f468f83009e7)


Download and install VC_redist

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/b976bdfe-18dc-4481-ac1c-66d923d491d0)

Download and install MySQL

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/a7ea3c13-13ee-4b07-a5b9-f3f2f2a6e512)

Select Typical Setup,
Launch Configuration Wizard when you are finished installing, 
Select Standard Configuration,
Create a Password

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/b948f2bc-32b6-485a-8329-bcd9e4874426)


Open IIS as an Administrator

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/543c9dd9-c30e-425f-b07c-993c94cd0482)


Register PHP from within IIS

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/b0ba25c2-7fe5-4e35-b463-323c313eec92)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/29e7af3c-8f44-448e-94e5-0c27a742503e)


Reload IIS (Open IIS, Stop and Start the server)

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/8cabb63b-499b-4a5d-80e9-e9c55b5cb54a)

Go to "sites", then "Default", then "osTicket", and click on "Browse *:80"

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/af2a7c5c-798a-4b36-8317-6ef39e915cf0)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/cc860e90-fe40-45fb-90d9-9fd445dcfe54)



Install osTicket v1.15.8

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/53286e96-8b01-47e6-b8a4-7e440a61fc28)


Go back to IIS sites -> Select Default -> Select osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable php_imap.dll
Enable php_intl.dll
Enable php_opcache.dll
Refresh the osTicket site in your browser

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/0dbadc96-512b-4d86-8025-cd8c4e57c865)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/cd21a942-28dd-4d24-aec9-0a8fc767c96b)



Assign Permissions: ost-config.php
Select "Disable inheritance", Select "Remove All
Select New Permissions, Type "Everyone", Select "All"

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/8a369e14-8326-4116-881f-410ac09ae015)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/3dacec3a-cd19-4cf8-b679-2ebce240ebeb)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/cc1e9777-231b-4765-87ea-0f4afae38c70)



Set up osTicket in the browser with User and E-mail

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/71ad3a42-b20b-4f31-906f-8db777caed6f)



Download and install HeidiSQL

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/a4d87d5b-89d8-46a1-b01b-c698b2cdbcd0)

Open Heidi SQL,
the create a new session,
then connect to the session,
and then create a database

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/8046f533-7505-430e-9bec-d31b837ee4d3)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/164b351b-e427-4ba0-ac91-88cfb0a18cb2)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/bf99b719-f4b7-4c7c-b153-b7dc7cbbfa3b)

Click Install Now

Delete C:\inetpub\wwwroot\osTicket\setup
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/2abc0220-b924-40ff-86a2-c7a5ea441a30)

Set Permissions to “Read” only on C:\inetpub\wwwroot\osTicket\include\ost-config.php
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/038c2570-2166-4b27-b4cc-b964c197b611)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/67c4d559-e60b-4b70-af38-eff93fddc4ab)

Congratulations! You have successfully installed osticket and are ready to begin ticketing services!
