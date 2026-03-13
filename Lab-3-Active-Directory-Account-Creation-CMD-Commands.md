<h1>Overview:  Lab 3 Creating Help Desk Accounts in Active Directory and Using CMD Commands</h1>

This section of my home lab documentation demonstrates the creation of a dedicated **Help Desk account** in **Active Directory (AD)** and managing it using **command-line tools (CMD)**. This task highlights the practical steps involved in provisioning accounts for IT support personnel, ensuring proper permissions, and configurations, and automating the process to streamline account management. Additionally, this project focuses on the administrative tasks that a Help Desk account might handle, such as password resets and user account modifications.

<h2>Objectives</h2>

- Create a specialized **Help Desk account** in Active Directory.
- Use **CMD commands** to verify account creation and configuration.
- Assign appropriate **permissions** to the Help Desk account for administrative tasks.
- Enable the **Recycle Bin** through Active Directory Administrative Center to enhance account recovery processes.

<h2>Documentation</h2>

For this home lab, we will create a Help Desk account with the appropriate permissions for administrative tasks through Active Directory. We will also enable certain features in our Active Directory settings and use specific CMD lines to automate and verify account creation and configuration.

Before creating the Help Desk account, let's begin by enabling the Recycle Bin to restore deleted items if needed. To do this, search for "Active Directory Administrative Center" in the search bar at the bottom left and open it.



1.
<p align="center">
<img src="https://i.imgur.com/1bU0W3t.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

In the Active Directory Administrative Center, select "SimoTech.com (local)," then click on "Enable Recycle Bin." Click "OK" to confirm and enable the Recycle Bin feature.

2.
<p align="center">
<img src="https://i.imgur.com/Dmiucqu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Once you enable the Recycle Bin, the "Enable Recycle Bin" option should be grayed out, and you should now see "Deleted Objects" listed under your local domain in the Active Directory Administrative Center. This confirms that the Recycle Bin feature has been successfully enabled.

3.
<p align="center">
<img src="https://i.imgur.com/i2pNP7C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Now lets open up Server Manager by searching it in our search bar on the bottom left. 

4.
<p align="center">
<img src="https://i.imgur.com/b7lrdO4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

With Server Manager open, on the top right, select “Tools” then “Active Directory Users and Computers”. Lets also pin Server Manager and Active Directory Users and Computers to our task bar by right clicking the icons on the bottom and select “Pin to task bar”.

5.
<p align="center">
<img src="https://i.imgur.com/mohZN1v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



6.
<p align="center">
<img src="https://i.imgur.com/gnJE2Za.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Now, open "Active Directory Users and Computers," click on "View" at the top, and then select "Advanced Features" to enable advanced options in the interface.

7.
<p align="center">
<img src="https://i.imgur.com/Cho8b1V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

In the "SimoTech.com" domain, select "Users," then right-click on the "Administrator" account and choose "Copy." This will replicate the appropriate permissions from the Administrator account to the new Help Desk account, ensuring it has the necessary administrative permissions for tasks.

8.
<p align="center">
<img src="https://i.imgur.com/FkltsWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

For the new Help Desk account, use "Helpdesk" as both the first name and last name, and set the same for the User logon name (Helpdesk). This will help maintain consistency and clarity for the account.

9.
<p align="center">
<img src="https://i.imgur.com/oQpYidQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Create a password for our helpdesk account. Then select “finish”.

10.
<p align="center">
<img src="https://i.imgur.com/Q3uUnKG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



11.
<p align="center">
<img src="https://i.imgur.com/3ad9ZD7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Now we can see that our Helpdesk account is part of the same groups as our Administrator account. 

12.
<p align="center">
<img src="https://i.imgur.com/YA9YOEN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Now, let's focus on important CMD lines for admins and the helpdesk. First, open the Command Prompt by searching for "Command Prompt" in the search bar at the bottom left and selecting it from the results.

13.
<p align="center">
<img src="https://i.imgur.com/kbhbn7Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

For our first command, type ipconfig and press Enter. This command will display details about your computer's network setup, including your IPv4 address, subnet mask, and other network configuration information.

14.
<p align="center">
<img src="https://i.imgur.com/4H1V733.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />

We can also type “ipconfig /all” which will display our computer's entire network configuration. It displays all network adapters, our settings, and additional information not shown by the basic ipconfig command such as the DHCP server, DHCP enabled, Lease Obtained and Lease Expires.


15.
<p align="center">
<img src="https://i.imgur.com/G3F1hZb.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />

Another useful command is net use. This command is used for managing, connecting, and disconnecting network resources, such as printers, shared disks, and other devices. Although we don’t have any resources mapped yet, it will allow us to view existing connections to shared resources or map shared network resources to a drive letter.

16.
<p align="center">
<img src="https://i.imgur.com/tYbtKcX.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />

The next command is net user helpdesk /domain. This command provides comprehensive details about the "helpdesk" user account, including group memberships, password restrictions, and login configurations. It’s especially useful when managing domain user accounts on a computer that is part of a domain, allowing you to view attributes and settings related to the designated account.

17.
<p align="center">
<img src="https://i.imgur.com/sN5N6Wg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Congratulations! We have successfully created the Helpdesk account using Active Directory Users and Computers and executed essential command-line tasks that are crucial in a Helpdesk environment. Great work!


 👉 [Next Lab 4 : Windows 10, Join PC to Domain (Helpdesk), RSAT Tool, Server Manager](https://github.com/BlakeHaywood/IT-Helpdesk-Lab-Series/blob/main/Lab-4-Windows-10-Join-PC-to-Domain-Helpdesk-RSAT-Tool-Server-Manager.md)
