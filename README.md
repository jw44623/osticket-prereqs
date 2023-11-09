<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Resource Group
  ![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/26bbae34-e7b8-4772-a552-b7d205161ded)

- Create a Windows 10 Virtual Machine (VM) with 2 Virtual CPUs and a Linux (Ubuntu 20.04) Virtual Machine with 2 Virtual CPUs
  ![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/e39dda9e-885a-4774-82cb-50b96cf8eb77)
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/d170dd36-d539-4a25-a15d-9d9237e708da)


<h2>Installation Steps</h2>


Install / Enable IIS in Windows WITH
CGI and Common HTTP Features

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/23280825-972b-4f9d-9416-98c0ac168623)
</p>
<br />

Download and install PHP Manager for IIS and the Rewrite Module
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/7f651181-1c3b-43a7-a534-83a173cd2bb8)

Create the directory C:\PHP

Download PHP and unzip the contents into C:\PHP
![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/6e950c31-aaa8-4444-98b1-9775ec7676e9)

Download and install VC_redist

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/a496a6ca-004b-4997-a239-92b1a6013971)

Download and install MySQL

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/fbd7361f-1887-4257-b36d-5bbc89e7010f)

Open IIS as an Administrator

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/556a3c7b-f640-4ea6-9b4a-b11fe0c999f3)

Register PHP from within IIS

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/a16690a6-ba0d-4cda-8d5c-35684f708b91)

Reload IIS (Open IIS, Stop and Start the server)

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/8cabb63b-499b-4a5d-80e9-e9c55b5cb54a)

Install osTicket v1.15.8

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/eccc85f0-62fc-45a5-8d8f-70d9e036549b)

Go back to IIS sites -> Select Default -> Select osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable php_imap.dll
Enable php_intl.dll
Enable php_opcache.dll
Refresh the osTicket site in your browser

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/393ce80c-b6d9-421b-b245-b308ca237464)

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/902cacec-6a58-430d-8fc7-8afb7453d063)

Set up osTicket in the browser with User and E-mail

Download and install HeidiSQL

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/ddbfa155-bc26-40ee-aea9-27ca76b4edfc)

Open Heidi SQL,
the create a new session,
then connect to the session,
and then create a database

![image](https://github.com/jw44623/osticket-prereqs/assets/150184762/23c0a5bc-71f0-4ce8-9143-bd1b87b167f4)

Click Install Now
