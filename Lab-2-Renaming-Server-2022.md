# Overview: Lab 2 Renaming Windows Server 2022 and Installing Active Directory

In this home lab, I will be demonstrating the process of **Renaming Server 2022** and **Installing Active Directory** in a home lab environment. I'll be using **VirtualBox** and be focusing on simulating a real-world IT setup. It serves as a practical demonstration of key IT administrative tasks, such as configuring server names, setting up Active Directory, and managing domain services.

## Objectives

- Rename a Windows Server 2022 instance to meet organizational standards.
- Install and configure **Active Directory Domain Services** (AD DS).
- Create and manage user accounts, groups, and security policies within Active Directory.

---

## Documentation

Now that we have Windows Server 2022 set up, we can proceed with installing Active Directory on our virtual machine home lab. Before that, let's rename our computer to keep things simple. To do so, open File Explorer from the taskbar, right-click on "This PC," and select "Properties."

1. <p align="center">
   <img src="https://i.imgur.com/XvenmB7.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

2. <p align="center">
   <img src="https://i.imgur.com/uYlujf4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

In the "About" section, scroll down until you see "Rename this PC (Advanced)" and click on it.

3. <p align="center">
   <img src="https://i.imgur.com/VTC2k8N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

Select “Change”.

4. <p align="center">
   <img src="https://i.imgur.com/GcNTHQD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

We will rename the computer to "Server2022" and then click "OK." A prompt will appear asking you to restart your virtual machine, which is normal. Click "OK," then select "Restart Now" to apply the changes.

5. <p align="center">
   <img src="https://i.imgur.com/YqOov2s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

6. <p align="center">
   <img src="https://i.imgur.com/sQF9VF9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

Proceed to log in the same way as before. Once you’ve logged into your administrator account, verify the renamed computer by following the same steps: open File Explorer, click on "This PC," then "Properties," and select "Rename this PC (Advanced)." Under "Full computer name," you should now see "Server2022.”

7. <p align="center">
   <img src="https://i.imgur.com/HbRCora.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

To optimize our performance for running virtual labs more efficiently, let's go to the search bar at the bottom left, type "About your PC," and select "Advanced system settings." In the "System Properties" window, click on the "Settings..." button under the "Performance" section. In the "Performance Options" window, select "Adjust for best performance," then click "OK" to apply the changes.

8. <p align="center">
   <img src="https://i.imgur.com/9OhH2oY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

9. <p align="center">
   <img src="https://i.imgur.com/pvOJZpC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />

10. <p align="center">
    <img src="https://i.imgur.com/4TP9DVT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

11. <p align="center">
    <img src="https://i.imgur.com/5Jffi9f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

Next, we will install Active Directory on our Server2022. Open Server Manager, click on "Manage" in the top right corner, then select "Add Roles and Features." Click "Next," then choose "Role-based or feature-based installation" and click "Next" again to proceed.

12. <p align="center">
    <img src="https://i.imgur.com/FoiXpG7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

13. <p align="center">
    <img src="https://i.imgur.com/K4P2K94.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

14. <p align="center">
    <img src="https://i.imgur.com/GKhkZCM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

15. <p align="center">
    <img src="https://i.imgur.com/LUebu8H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

Select "Active Directory Domain Services," then click "Add Features" when prompted. After that, click "Next" to continue.

16. <p align="center">
    <img src="https://i.imgur.com/MMCXYbz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

17. <p align="center">
    <img src="https://i.imgur.com/BgI6tA2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

Finally select “Install”.

18. <p align="center">
    <img src="https://i.imgur.com/JWuD12V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

Select “Promote this server to a domain controller”.

19. <p align="center">
    <img src="https://i.imgur.com/gidEDIi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

Select "Add a new forest" and enter "SimoTech.com" as the root domain name. Then click "Next" to proceed.

20. <p align="center">
    <img src="https://i.imgur.com/csM8jvS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

Create a password for our Directory Service Restore Mode (DSRM) then click “Next”. 

21. <p align="center">
    <img src="https://i.imgur.com/GTMq1Un.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

We can uncheck “Create DNS delegation” then click “Next” then “Install”.

22. <p align="center">
    <img src="https://i.imgur.com/bs33zRO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

23. <p align="center">
    <img src="https://i.imgur.com/CzE1uT1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

After this process, the virtual machine will restart to install Active Directory Domain Services. Once the restart is complete, sign back in by selecting "Input" and clicking the "Ctrl + Alt + Del" button. You will notice that the domain controller is now listed as "SIMOTECH\Administrator." Go ahead and sign in to your account using the domain credentials.

24. <p align="center">
    <img src="https://i.imgur.com/89Pj0lt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
    </p>
    <br />

Once signed in, with Server Manager open, click on "Tools" in the top right corner, then select "Active Directory Users and Computers" from the dropdown menu.

25.<p align="center">
<img src="https://i.imgur.com/aa27wJy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Congratulations we have successfully created a domain controller (SimoTech.com) with Active Directory installed! 

26.
<p align="center">
<img src="https://i.imgur.com/G7Kyyzj.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<br />
<br />

 👉 [Next Lab 3 : Active Directory Account Creation, CMD Commands](#)
