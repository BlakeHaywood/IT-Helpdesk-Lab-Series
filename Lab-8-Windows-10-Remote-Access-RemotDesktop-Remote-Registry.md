# Overview: Lab 8 Windows 10 Remote Access: Remote Desktop, Remote Registry

This section of my home lab documentation focuses on setting up and using **Remote Desktop** and **Remote Registry** for remote access to a **Windows 10** machine in a VirtualBox environment. The project covers the steps for enabling, configuring, and troubleshooting remote access services to allow users and administrators to connect to and manage a Windows 10 PC remotely. 

## Objectives

1. **Windows 10 Remote Management:** Configuring and managing remote access to Windows 10 systems.
2. **Remote Registry:** Exploring the **Remote Registry** feature to manage registry settings from another computer.
3. **Remote Desktop:** Setting up and utilizing **Remote Desktop** for secure remote control of Windows 10 systems.
4. **C$ Administrative Share:** Understanding and using the hidden **C$ administrative share** for file and system access.

---

## Documentation

In this home lab, we will focus on using Windows 10 Remote Management, Remote Registry, Remote Desktop, and accessing C$. Let's begin by enabling Windows 10 Remote Desktop Services on Desktop2 for Bob. On Desktop2, open File Explorer, right-click on "This PC," and select "Advanced System Settings." Next, use your Helpdesk administrative permissions to enable "Allow Remote Connections" and click on "Select Users" to add the necessary users.

1. <p align="center">
   <img src="https://i.imgur.com/1cXKTYj.png" height="60%" width="60%" alt="Disk Sanitization Steps 1"/>
   </p>
   <br />

Select “Add” then add Helpdesk then select “OK” then “Apply”. 

2. <p align="center">
   <img src="https://i.imgur.com/XbAGBXS.png" height="80%" width="60%" alt="Disk Sanitization Steps 2"/>
   </p>
   <br />

Now that Remote Desktop is enabled, let's switch to the Helpdesk account. Search for "Remote Desktop Connection" in the Windows search bar and open the application. In the "Computer" field, type "Desktop2" and log in using your Helpdesk credentials. Once the remote session is active, you can select "Yes" to disconnect Bob's session, allowing you to log in to Desktop2 under the Helpdesk account.

3. <p align="center">
   <img src="https://i.imgur.com/Rpq9Pxr.png" height="80%" width="80%" alt="Disk Sanitization Steps 3"/>
   </p>
   <br />

Now that we're remotely accessing Bob's computer from the Helpdesk account, we can perform various tasks. For example, we can create a new folder for Bob by navigating to his folder, then opening the "Desktop" directory and creating a folder there.

4. <p align="center">
   <img src="https://i.imgur.com/ghmYbaK.png" height="80%" width="80%" alt="Disk Sanitization Steps 4"/>
   </p>
   <br />

We can also delete things in Bob’s download’s folder if Bob wants to. 

5. <p align="center">
   <img src="https://i.imgur.com/uo3TTn5.png" height="80%" width="80%" alt="Disk Sanitization Steps 5"/>
   </p>
   <br />

We can also access Bob’s AppData folder by navigating to User → Bob and typing `\appdata` in the File Explorer search bar. This will allow us to view and manage the contents of Bob’s AppData directory.

6. <p align="center">
   <img src="https://i.imgur.com/EuHIgSH.png" height="80%" width="80%" alt="Disk Sanitization Steps 6"/>
   </p>
   <br />

Let's disconnect from the Remote Desktop Connection and log back in as Bob on Desktop2. Once logged in, we should see the "Test" folder on Bob's desktop.

7. <p align="center">
   <img src="https://i.imgur.com/0a4KmpO.png" height="80%" width="80%" alt="Disk Sanitization Steps 7"/>
   </p>
   <br />

Next, let's show how to determine shared drives. On Desktop2, open Command Prompt (CMD) and type `net use`. This will display a list of all the network drives currently mapped to the system.

8. <p align="center">
   <img src="https://i.imgur.com/gpL5pb9.png" height="80%" width="80%" alt="Disk Sanitization Steps 8"/>
   </p>
   <br />

Another way to determine shared drives is to search for "Services" in the Windows search bar and run it as Administrator. Use Helpdesk credentials to bypass. In the Services window, search for "Remote Registry," right-click on it, and select "Properties." Change the "Startup type" from "Disabled" to "Automatic," then click "Apply" and "OK." After that, click "Start" to enable the Remote Registry service. This will allow access to registry information, including shared drives.

9. <p align="center">
   <img src="https://i.imgur.com/Fs2sQSD.png" height="80%" width="80%" alt="Disk Sanitization Steps 8"/>
   </p>
   <br />

Now lets go to our Helpdesk account, search up “Registry Editor” 

10. <p align="center">
    <img src="https://i.imgur.com/VlLbOmm.png" height="80%" width="80%" alt="Disk Sanitization Steps 9"/>
    </p>
    <br />

Select File on the top left → Connect Network Registry → then search “Desktop2” then “OK”.

11. <p align="center">
    <img src="https://i.imgur.com/kpcEXnj.png" height="80%" width="80%" alt="Disk Sanitization Steps 10"/>
    </p>
    <br />

12. <p align="center">
    <img src="https://i.imgur.com/JlnOulQ.png" height="80%" width="80%" alt="Disk Sanitization Steps 11"/>
    </p>
    <br />

Under HKEY_USERS, we need to browse through the folders to find the one associated with the "Z" drive under the "Network" section. This will show the shared drives that are mapped to the system. The drive letter "Z" will be listed within the registry key associated with the network shares, which helps to identify the shared drives connected to the machine.

13. <p align="center">
    <img src="https://i.imgur.com/n6tPIcN.png" height="80%" width="80%" alt="Disk Sanitization Steps 12"/>
    </p>
    <br />

Now, let's use the C$ command with our Helpdesk account, which allows administrators to remotely access the root of the C: drive on the local user account. To do this, open File Explorer on Helpdesk and type `\\Desktop2\c$` in the search bar, then press Enter. This will grant access to the C: drive of Desktop2 remotely.

14. <p align="center">
    <img src="https://i.imgur.com/aCyFvnO.png" height="80%" width="80%" alt="Disk Sanitization Steps 13"/>
    </p>
    <br />

From here, we can delete the "Test" folder we created remotely. Navigate to Users → Bob → Desktop, and then locate the "Test" folder. Once found, simply delete the folder to remove it from Bob's desktop.

15. <p align="center">
    <img src="https://i.imgur.com/yJXfmoG.png" height="80%" width="80%" alt="Disk Sanitization Steps 14"/>
    </p>
    <br />

Now if we check back on Bob’s computer we see that the “Test” folder is no longer in Bob’s desktop. 

16. <p align="center">
    <img src="https://i.imgur.com/rw6OoWC.png" height="80%" width="80%" alt="Disk Sanitization Steps 15"/>
    </p>
    <br />

Another way to remote into a users is using Windows Remote Assistance by typing “Windows Remote Assistance” in the Windows search on Desktop2 → then select “Invite someone you trust to help you”. 

17. <p align="center">
    <img src="https://i.imgur.com/OEPIXil.png" height="80%" width="80%" alt="Disk Sanitization Steps 16"/>
    </p>
    <br />

Select “Save this invitation as file” on desktop.

18. <p align="center">
    <img src="https://i.imgur.com/cpyO0fx.png" height="80%" width="80%" alt="Disk Sanitization Steps 17"/>
    </p>
    <br />

Now, back on the Helpdesk account, open Windows Remote Assistance and select Help Someone Who Has Invited You. In the prompt, type `\\Desktop2\C$` to access the invitation file. Once connected, navigate to Users → Bob → Desktop and locate the invitation file there. Afterward, you can enter the password provided in the invitation to establish the remote session.

19. <p align="center">
    <img src="https://i.imgur.com/eJfR0eX.png" height="80%" width="80%" alt="Disk Sanitization Steps 18"/>
    </p>
    <br />

A prompt will ask if we want to allow Helpdesk to remote access, select “Yes”. 

20. <p align="center">
    <img src="https://i.imgur.com/tmIzR1L.png" height="80%" width="80%" alt="Disk Sanitization Steps 19"/>
    </p>
    <br />

Now we have remote control of Bob’s computer on Helpdesk. 

21. <p align="center">
    <img src="https://i.imgur.com/faOfkv9.png" height="80%" width="80%" alt="Disk Sanitization Steps 20"/>
    </p>
    <br />

Now we can send chats to Bob, request control access on the top left.

22. <p align="center">
    <img src="https://i.imgur.com/M8Ejl3I.png" height="90%" width="90%" alt="Disk Sanitization Steps 21"/>
    </p>
    <br />

Congratulations! We have successfully accessed **Windows 10 Remote Management**, explored the Remote Registry feature, set up and utilized Remote Desktop for secure remote control of Windows 10 systems, and used **C$.**

 👉 [Next Lab 9 : RSOP, Group Policy, Task Manager, Disable Logoff](Lab-9-RSOP-Group-Policy.md)
