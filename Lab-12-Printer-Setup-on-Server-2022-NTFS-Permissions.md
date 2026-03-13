# Overview: Lab 12 Printer Setup on Server 2022, NTFS Permissions

This repository documents my home lab focused on **Printer Setup on Server 2022** and **NTFS Permissions** using **VirtualBox**. The lab explores configuring printers on a Windows Server 2022 machine, setting up shared printers for network use, and managing NTFS file permissions to control access to shared resources. 

## Objectives

- **Printer Setup on Server 2022:** Learn how to install and configure printers on Windows Server 2022 and share them with network users.
- **NTFS Permissions:** Understand how to set and manage NTFS file permissions for controlling access to shared resources on the server.
- **Printer Sharing:** Configure printer sharing and permissions to ensure that only authorized users can access and print to the shared printers.

---

## Documentation

In this home lab, we will focus on how to install and configure network printers, as well as explore file and printer security through NTFS permissions.

Let's open up **Server Manager** on our **Windows Server 2022** VM. Select **Manage** → **Add Roles and Features**.

1. <p align="center">
   <img src="https://i.imgur.com/WQZTWKw.png" height="80%" width="80%" alt="Disk Sanitization Steps 1"/>
   </p>
   <br />

Select Next until you reach Select Server Roles, then click on **Print and Document Services**. Select **Add Features**, then click Next.

2. <p align="center">
   <img src="https://i.imgur.com/gQd6b1I.png" height="80%" width="80%" alt="Disk Sanitization Steps 2"/>
   </p>
   <br />

For Role Services, it shows the different service installations, such as options for using Internet Printing Services or UNIX-based computers for LPD printing. In this case, we will focus on **Print Server**. Select Next, then click **Install**.

3. <p align="center">
   <img src="https://i.imgur.com/TDU9KzX.png" height="80%" width="80%" alt="Disk Sanitization Steps 3"/>
   </p>
   <br />

4. <p align="center">
   <img src="https://i.imgur.com/7WpZ5B1.png" height="80%" width="80%" alt="Disk Sanitization Steps 4"/>
   </p>
   <br />

Once the installation is complete, we can verify that the printing services are installed by reopening Server Manager. We should notice that **Print Services** appears on the left side.

5. <p align="center">
   <img src="https://i.imgur.com/fpPYPFL.png" height="80%" width="80%" alt="Disk Sanitization Steps 5"/>
   </p>
   <br />

Lets open up **“Tools”** → **“Print Management”**.

6. <p align="center">
   <img src="https://i.imgur.com/Io8lfNl.png" height="80%" width="80%" alt="Disk Sanitization Steps 6"/>
   </p>
   <br />

In Print Management, we can see the different drivers, printers, ports, and the server "Server2022 (local)" for our Desktop2 computer.

7. <p align="center">
   <img src="https://i.imgur.com/hoCsKZi.png" height="80%" width="80%" alt="Disk Sanitization Steps 7"/>
   </p>
   <br />

Now lets create a printer: right-click then select **“Add Printer..”**.

8. <p align="center">
   <img src="https://i.imgur.com/FhUnte4.png" height="80%" width="80%" alt="Disk Sanitization Steps 8"/>
   </p>
   <br />

Select **“Add a new printer using an existing port:”**.

9. <p align="center">
   <img src="https://i.imgur.com/eVun6T7.png" height="80%" width="80%" alt="Disk Sanitization Steps 9"/>
   </p>
   <br />

Then select **“Install a new driver”**.

10. <p align="center">
    <img src="https://i.imgur.com/2Pj6cLW.png" height="80%" width="80%" alt="Disk Sanitization Steps 10"/>
    </p>
    <br />

Here, we will select any driver. I will select **"Microsoft MS-XPS Class Driver 2"**, then click Next.

11. <p align="center">
    <img src="https://i.imgur.com/sHFlt3e.png" height="80%" width="80%" alt="Disk Sanitization Steps 11"/>
    </p>
    <br />

Make sure to uncheck **"Share this printer"**, then click Next and finally select Finish.

12. <p align="center">
    <img src="https://i.imgur.com/xNCzyAz.png" height="80%" width="80%" alt="Disk Sanitization Steps 12"/>
    </p>
    <br />

13. <p align="center">
    <img src="https://i.imgur.com/6ZVsb0L.png" height="80%" width="80%" alt="Disk Sanitization Steps 13"/>
    </p>
    <br />

Now, when we look into the properties of our new printer, we can see the different settings we can configure. For example, if we wanted to list the printer in Active Directory for another user to install, we could do that in the Sharing tab. We will enable this in just a bit.

14. <p align="center">
    <img src="https://i.imgur.com/K5Fhp82.png" height="80%" width="80%" alt="Disk Sanitization Steps 14"/>
    </p>
    <br />

We can also see the different ports available for the printer in the Ports tab.

15. <p align="center">
    <img src="https://i.imgur.com/lM77ZRE.png" height="80%" width="80%" alt="Disk Sanitization Steps 15"/>
    </p>
    <br />

Lets look into the **“Security”** tab in the properties of our printer. Here we want to remove the users **“EVERYONE”** and limit certain users to have access to our printer. Click on **“Advanced”**.

16. <p align="center">
    <img src="https://i.imgur.com/Xamq2T0.png" height="80%" width="80%" alt="Disk Sanitization Steps 16"/>
    </p>
    <br />

Select **"Everyone"**, then click Remove.

17. <p align="center">
    <img src="https://i.imgur.com/1hH0eRv.png" height="80%" width="80%" alt="Disk Sanitization Steps 17"/>
    </p>
    <br />

Now, let's add HR to the permissions by clicking on Add, then **Select a principal** → type in **"HR"**, and select OK. For basic permissions, we will only allow HR to **Print**, then click OK → Apply, and finally OK.

18. <p align="center">
    <img src="https://i.imgur.com/MyWbFL9.png" height="80%" width="80%" alt="Disk Sanitization Steps 18"/>
    </p>
    <br />

Now, we can see in the Security tab that HR is a member of this security group, and it shows the permissions HR has for this printer. This printer should also automatically show up for anyone in the HR group.

19. <p align="center">
    <img src="https://i.imgur.com/dm3Ak0s.png" height="80%" width="80%" alt="Disk Sanitization Steps 19"/>
    </p>
    <br />

Now, let's list this printer in the directory. Click on the **Sharing** tab, then enable **"Share this printer"** and **"List in the directory"**, and click Apply.

20. <p align="center">
    <img src="https://i.imgur.com/XoOV1UZ.png" height="80%" width="80%" alt="Disk Sanitization Steps 20"/>
    </p>
    <br />

Let's verify that by going to **Active Directory Users and Computers**, right-clicking on the domain `SimoTech.com`, selecting **"Find"**, then selecting the dropdown under **"Find:"** and choosing **"Printers"**.

21. <p align="center">
    <img src="https://i.imgur.com/0MTOYbX.png" height="80%" width="80%" alt="Disk Sanitization Steps 21"/>
    </p>
    <br />

22. <p align="center">
    <img src="https://i.imgur.com/SzROBgh.png" height="80%" width="80%" alt="Disk Sanitization Steps 22"/>
    </p>
    <br />

Click on **"Find Now"**, and our printer should show up in the directory.

23. <p align="center">
    <img src="https://i.imgur.com/lK0aF2Y.png" height="80%" width="80%" alt="Disk Sanitization Steps 23"/>
    </p>
    <br />

Now that the printer is in the directory, let's log into **Desktop2** as Bob and install the printer from the directory. Open up **Control Panel** on Desktop2 → **View Devices and Printers** → **Add Printer**. The scan will search for the printer in the directory. Select Next, then Finish.

24. <p align="center">
    <img src="https://i.imgur.com/57wqkqt.png" height="80%" width="80%" alt="Disk Sanitization Steps 24"/>
    </p>
    <br />

25. <p align="center">
    <img src="https://i.imgur.com/H1IpjR7.png" height="80%" width="80%" alt="Disk Sanitization Steps 25"/>
    </p>
    <br />

Congratulations! We have successfully added a printer on our Server 2022 domain and explored file and printer security through NTFS permissions for effective access control.

 👉 [Next Lab 13 : Understanding Tickets Using Spiceworks](Lab-13-Spiceworks-Ticketing.md)
