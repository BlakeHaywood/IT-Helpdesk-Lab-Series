# Overview: Lab 13 Understanding Tickets Using Spiceworks

This repository documents my home lab focused on **Understanding Tickets Using Spiceworks** within a **VirtualBox** environment. The lab aims to explore how Spiceworks can be used to manage IT tickets, track service requests, and streamline support workflows. 

## Objectives

- **Learn Spiceworks Ticketing System:** Set up and configure Spiceworks to create, manage, and track IT support tickets.
- **Ticket Management:** Understand how to categorize, prioritize, and assign tickets to team members within a virtualized network environment.
- **Reporting and Analysis:** Learn how to generate reports on ticket resolution times, trends, and overall support performance.

---

## Documentation

In this lab, we will focus on Spiceworks ticketing services, which is free to use, and explore how Remote Support can assist users.

To begin, we will create an account for Spiceworks using an email. After the account creation, we will set up a domain, which will be the same domain we've been using in our previous labs, `SimoTech.com`. Once the account and domain are ready, we will launch the IT Cloud Helpdesk through the IT tools tab at the top of the Spiceworks interface.

1. <p align="center">
   <img src="https://i.imgur.com/DwLU0mo.png" height="80%" width="80%" alt="Disk Sanitization Steps 1"/>
   </p>
   <br />

Here on the Spiceworks dashboard, we have a centralized interface for IT professionals. It provides a clear overview of key metrics, including new, open, and unassigned tickets. Additionally, it displays network inventory, device health, and alerts.

2. <p align="center">
   <img src="https://i.imgur.com/e3abN4G.png" height="80%" width="80%" alt="Disk Sanitization Steps 2"/>
   </p>
   <br />

Let's take a look at creating a ticket and the properties involved. Start by selecting the **Ticket** tab on the left-side panel, then click on the blue **"New Ticket"** button at the top right.

3. <p align="center">
   <img src="https://i.imgur.com/aCgaJue.png" height="80%" width="80%" alt="Disk Sanitization Steps 3"/>
   </p>
   <br />

### Ticket Properties Breakdown:

- **Organization**: The domain or company the helpdesk is working for.
- **Contact**: The person reporting the issue (employee or external user).
- **Assignee**: The IT support member or team assigned to resolve the issue.
- **Summary**: A brief description explaining the situation.
- **Priority**: Indicates urgency (Low to High).
- **Category**: Classifies the ticket (Email, Hardware, Network, Software, etc.).

4. <p align="center">
   <img src="https://i.imgur.com/kAErlSa.png" height="80%" width="80%" alt="Disk Sanitization Steps 4"/>
   </p>
   <br />

To get started with a helpdesk environment, we need to add a technician:
1. Go to **Settings**.
2. Select **Employee Administration**.
3. Click **Add Employee**.

5. <p align="center">
   <img src="https://i.imgur.com/4wtqxNR.png" height="80%" width="80%" alt="Disk Sanitization Steps 5"/>
   </p>
   <br />

6. <p align="center">
   <img src="https://i.imgur.com/YESwr8B.png" height="80%" width="80%" alt="Disk Sanitization Steps 6"/>
   </p>
   <br />

7. <p align="center">
   <img src="https://i.imgur.com/eESbm7Q.png" height="80%" width="80%" alt="Disk Sanitization Steps 7"/>
   </p>
   <br />

In this scenario, Bob is experiencing a lockout. Bob sends an email to: `help@simotech.on.spiceworks.com`.

8. <p align="center">
   <img src="https://i.imgur.com/BMCgDiM.png" height="80%" width="80%" alt="Disk Sanitization Steps 8"/>
   </p>
   <br />

Once the email arrives, it automatically generates a new ticket.

9. <p align="center">
   <img src="https://i.imgur.com/HJIdoQd.png" height="80%" width="80%" alt="Disk Sanitization Steps 9"/>
   </p>
   <br />

Accept the ticket and assign it to the helpdesk tech, **Kevin**.

10. <p align="center">
    <img src="https://i.imgur.com/HwgBoZM.png" height="80%" width="80%" alt="Disk Sanitization Steps 10"/>
    </p>
    <br />

Set the Priority to **High** (user cannot work) and set a **Due Date**.

11. <p align="center">
    <img src="https://i.imgur.com/tgkVLrg.png" height="80%" width="80%" alt="Disk Sanitization Steps 11"/>
    </p>
    <br />

We can track time spent by selecting the **“+15m”** option.

12. <p align="center">
    <img src="https://i.imgur.com/NSHaT5l.png" height="80%" width="80%" alt="Disk Sanitization Steps 12"/>
    </p>
    <br />

After resolving the issue, we contact the user and **Close** the ticket.

13. <p align="center">
    <img src="https://i.imgur.com/hj70RuL.png" height="80%" width="80%" alt="Disk Sanitization Steps 13"/>
    </p>
    <br />

Past tickets can be viewed by filtering the view from **“Open”** to **“Closed”**.

14. <p align="center">
    <img src="https://i.imgur.com/3rAog5D.png" height="80%" width="80%" alt="Disk Sanitization Steps 14"/>
    </p>
    <br />

To use Remote Support, navigate to **Tools** → **Remote Support**.

15. <p align="center">
    <img src="https://i.imgur.com/Q0QeR0b.png" height="80%" width="80%" alt="Disk Sanitization Steps 15"/>
    </p>
    <br />

Select **Start Remote Session** to generate a code for the user.

16. <p align="center">
    <img src="https://i.imgur.com/jNMmeUG.png" height="80%" width="80%" alt="Disk Sanitization Steps 16"/>
    </p>
    <br />

On Desktop2, switch from static IP to **NAT/DHCP** to access the internet, then join the session via `join.zoho.com`.

17. <p align="center">
    <img src="https://i.imgur.com/wpdBHnn.png" height="80%" width="80%" alt="Disk Sanitization Steps 17"/>
    </p>
    <br />

18. <p align="center">
    <img src="https://i.imgur.com/w4SZOZP.png" height="80%" width="80%" alt="Disk Sanitization Steps 18"/>
    </p>
    <br />

Now we have full remote access to Desktop2.

19. <p align="center">
    <img src="https://i.imgur.com/xK3myyU.png" height="80%" width="80%" alt="Disk Sanitization Steps 19"/>
    </p>
    <br />

Use the **Chat** feature to communicate with the user during the session.

20. <p align="center">
    <img src="https://i.imgur.com/m7B0aNZ.png" height="80%" width="80%" alt="Disk Sanitization Steps 20"/>
    </p>
    <br />

21. <p align="center">
    <img src="https://i.imgur.com/VGY1zfJ.png" height="80%" width="80%" alt="Disk Sanitization Steps 21"/>
    </p>
    <br />

We can remotely launch **Command Prompt** or **Device Manager**.

22. <p align="center">
    <img src="https://i.imgur.com/SDtraHe.png" height="80%" width="80%" alt="Disk Sanitization Steps 22"/>
    </p>
    <br />

23. <p align="center">
    <img src="https://i.imgur.com/OSQvJac.png" height="8

👉 [Next Lab 14 : Delegate Control and Account Lockout Management](https://github.com/BlakeHaywood/IT-Helpdesk-Lab-Series/blob/main/Lab-14-Delegate-Control-and-Account-Lockout-Management.md)
