# Overview: Lab 11 PDQ Inventory: Hardware and Software Reporting

This repository documents my home lab focused on **PDQ Inventory: Hardware and Software Reporting** using **VirtualBox**. The lab aims to explore PDQ Inventory's capabilities for gathering detailed reports on hardware and software configurations across a network of virtual machines. The project includes setting up PDQ Inventory, creating custom reports, and automating hardware/software data collection for system management and network monitoring.

## Objectives

- **Learn PDQ Inventory:** Explore how to set up PDQ Inventory and configure it for comprehensive hardware and software reporting.
- **Create Custom Reports:** Learn how to build and customize reports to track hardware specifications, software installations, and system configurations.

---

## Documentation

In this home lab, I will showcase the installation and uses of **PDQ Inventory**. To start, open **File Explorer** and navigate to the **SimoTech** folder. Inside, you should find the **PDQ Inventory** application.

1. <p align="center">
   <img src="https://i.imgur.com/aVTqfoM.png" height="80%" width="80%" alt="Disk Sanitization Steps 1"/>
   </p>
   <br />

Double click on the application to start the installation and follow the prompts to finish. Launch the application once complete. 

2. <p align="center">
   <img src="https://i.imgur.com/lv9hlxL.png" height="80%" width="80%" alt="Disk Sanitization Steps 2"/>
   </p>
   <br />

Lets add Desktop2 to PDQ Inventory. To do that, select **“Computers”** at the top → **“Add computers”** → **“Active Directory - Browse by Name”**, then select **“Desktop2.SimoTech.com”** as the target and select **“OK”**.

3. <p align="center">
   <img src="https://i.imgur.com/1m4gB68.png" height="80%" width="80%" alt="Disk Sanitization Steps 3"/>
   </p>
   <br />

**PDQ Inventory** is a powerful IT asset management tool that helps track and manage hardware and software across a network. It provides real-time insights, automates reporting, and integrates seamlessly with tools like **PDQ Deploy** for efficient software updates and policy compliance.

Here are some of the features we can use in PDQ Inventory: Right-click on **Desktop2**, then select **Run Report** → **Share Folders** to generate a report on the shared folders available on that machine.

4. <p align="center">
   <img src="https://i.imgur.com/laDMEG7.png" height="80%" width="80%" alt="Disk Sanitization Steps 4"/>
   </p>
   <br />

This shows us all the folders that are mapped on it. Lets double click on **“ADMIN$”**.

5. <p align="center">
   <img src="https://i.imgur.com/SuSndJy.png" height="80%" width="80%" alt="Disk Sanitization Steps 5"/>
   </p>
   <br />

It will give us all the details and specifications that are on that computer, such as who is logged in currently, what the domain controller is, the host name, the operating system, and the version of Windows it is using.

6. <p align="center">
   <img src="https://i.imgur.com/bNlYnPT.png" height="80%" width="80%" alt="Disk Sanitization Steps 6"/>
   </p>
   <br />

On the left-hand side, we can see all the items we can explore on Desktop2. Let's take a look at the **Applications** by clicking on it. This is a great way to check what applications are installed on the computer. If something is missing, we can use this feature to identify the missing software and deploy it accordingly.

7. <p align="center">
   <img src="https://i.imgur.com/Bujt4R7.png" height="80%" width="80%" alt="Disk Sanitization Steps 7"/>
   </p>
   <br />

To verify if we have these applications downloaded, let's go to our Desktop2 VM and open **Control Panel** → **Uninstall a Program**. This will display the list of applications installed on Desktop2 under Bob's account.

8. <p align="center">
   <img src="https://i.imgur.com/dvox4rY.png" height="80%" width="80%" alt="Disk Sanitization Steps 8"/>
   </p>
   <br />

We can also navigate to the **CPU** section on the left to see how many CPU cores are available on Desktop2. It will also provide information about the processors being used on the system.

9. <p align="center">
   <img src="https://i.imgur.com/3huXb17.png" height="80%" width="80%" alt="Disk Sanitization Steps 9"/>
   </p>
   <br />

The **Environment** tab on the left shows us the path directories configured on Desktop2 as well.

10. <p align="center">
    <img src="https://i.imgur.com/StwnqcS.png" height="80%" width="80%" alt="Disk Sanitization Steps 10"/>
    </p>
    <br />

We can look into **Printers** and see which printer machines are installed on Desktop2 as well.

11. <p align="center">
    <img src="https://i.imgur.com/SXQjW4O.png" height="80%" width="80%" alt="Disk Sanitization Steps 11"/>
    </p>
    <br />

On the **Shares** tab, we can see our shared drives.

12. <p align="center">
    <img src="https://i.imgur.com/kQ7k19W.png" height="80%" width="80%" alt="Disk Sanitization Steps 12"/>
    </p>
    <br />

If we wanted to remote admin into Desktop2, double click on **“ADMIN$”**. Here we can see things on a system level. 

13. <p align="center">
    <img src="https://i.imgur.com/HAO88iZ.png" height="80%" width="80%" alt="Disk Sanitization Steps 13"/>
    </p>
    <br />

If we wanted to add a specific file to Desktop2, we can double click on **“C$”** and add anything in there.

14. <p align="center">
    <img src="https://i.imgur.com/6bvtR44.png" height="80%" width="80%" alt="Disk Sanitization Steps 14"/>
    </p>
    <br />

Lets copy the text document **“results”** then go into **“Users”** → **“Bob”** → **“Desktop”**.

15. <p align="center">
    <img src="https://i.imgur.com/YWO78cG.png" height="80%" width="80%" alt="Disk Sanitization Steps 15"/>
    </p>
    <br />

Paste the copied "results" file onto the Desktop. We can see that the file was successfully transferred to our Desktop2 VM from our Windows Server 2022 VM using PDQ Inventory.

16. <p align="center">
    <img src="https://i.imgur.com/2K9XLFc.png" height="80%" width="80%" alt="Disk Sanitization Steps 16"/>
    </p>
    <br />

Some additional features in PDQ Inventory include **Manage with MMC**, which allows us to manage Computer Management on the Desktop2 VM directly from PDQ Inventory. To use this, select **Tools** at the top, then choose **Manage with MMC**.

17. <p align="center">
    <img src="https://i.imgur.com/cAE4kPX.png" height="80%" width="80%" alt="Disk Sanitization Steps 17"/>
    </p>
    <br />

We can create a new user on Desktop2 if we wanted to by using this feature. 

18. <p align="center">
    <img src="https://i.imgur.com/8J9OPlj.png" height="80%" width="80%" alt="Disk Sanitization Steps 18"/>
    </p>
    <br />

Another tool we can use is **“Remote Desktop”** if we want to remote into Desktop2 from PDQ Inventory. 

19. <p align="center">
    <img src="https://i.imgur.com/cBMl5cV.png" height="80%" width="80%" alt="Disk Sanitization Steps 19"/>
    </p>
    <br />

20. <p align="center">
    <img src="https://i.imgur.com/4OcMfH2.png" height="80%" width="80%" alt="Disk Sanitization Steps 20"/>
    </p>
    <br />

Another powerful feature we can use is remotely rebooting Desktop2. To do this, select **Tools**, then choose **Reboot/Shutdown**.

21. <p align="center">
    <img src="https://i.imgur.com/aWlZ8Kh.png" height="80%" width="80%" alt="Disk Sanitization Steps 21"/>
    </p>
    <br />

22. <p align="center">
    <img src="https://i.imgur.com/xFQVlog.png" height="80%" width="80%" alt="Disk Sanitization Steps 22"/>
    </p>
    <br />

Now, let's print a report on Desktop2. Return to the home page in All Computers, right-click on Desktop2, and select **Print Preview**. This feature is useful if, for example, a manager requests a report on a specific user's computer.

23. <p align="center">
    <img src="https://i.imgur.com/kiRk8vA.png" height="80%" width="80%" alt="Disk Sanitization Steps 23"/>
    </p>
    <br />

Now, let's print a report on the hardware devices on Desktop2. Right-click on Desktop2, then select **Run Report** → **Hardware Devices**. This will generate a report of all the hardware devices installed on Desktop2.

24. <p align="center">
    <img src="https://i.imgur.com/FVWvsfR.png" height="80%" width="80%" alt="Disk Sanitization Steps 24"/>
    </p>
    <br />

Select the printer icon on the top left to preview the report. This will display a list of all the hardware devices associated with Desktop2.

25. <p align="center">
    <img src="https://i.imgur.com/W46F0kZ.png" height="80%" width="80%" alt="Disk Sanitization Steps 25"/>
    </p>
    <br />

Lastly, we can launch PDQ Deploy for Desktop2 through PDQ Inventory. In All Computers, right-click on Desktop2, select **Tools**, and then choose **Run PDQ Deploy**.

26. <p align="center">
    <img src="https://i.imgur.com/mhHBfp1.png" height="80%" width="80%" alt="Disk Sanitization Steps 26"/>
    </p>
    <br />

From here, we can deploy applications or software packages onto Desktop2 using this feature. Let's select the Mozilla Firefox package that we previously installed on our Windows Server 2022 VM, then click **OK** to deploy it onto the Desktop2 VM.

27. <p align="center">
    <img src="https://i.imgur.com/PVeEPKM.png" height="80%" width="80%" alt="Disk Sanitization Steps 27"/>
    </p>
    <br />

Notice on the left that `Desktop2.SimoTech.com` is the target for the Firefox application deployment. Now, select **Deploy Now** to begin the deployment process.

28. <p align="center">
    <img src="https://i.imgur.com/rpr7ihk.png" height="80%" width="80%" alt="Disk Sanitization Steps 28"/>
    </p>
    <br />

Now, we can see that Firefox has been successfully installed on our Desktop2 VM through the PDQ Deploy deployment process.

29. <p align="center">
    <img src="https://i.imgur.com/8IWjtmv.png" height="80%" width="80%" alt="Disk Sanitization Steps 29"/>
    </p>
    <br />

Congratulations! We have successfully completed Home Lab 11 on **PDQ Deploy** and **Inventory**!

This project focused on using **PDQ Inventory** within a **VirtualBox** environment to track and manage hardware and software across virtual machines. We explored creating and analyzing reports, gaining insights into user resources, and generating reports for managers or supervisors.

 👉 [Next Lab 12 : Printer Setup on Server 2022, NTFS Permissions](https://github.com/BlakeHaywood/IT-Helpdesk-Lab-Series/blob/main/Lab-12-Printer-Setup-on-Server-2022-NTFS-Permissions.md)
