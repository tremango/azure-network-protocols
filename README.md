<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (ICMP,SSH, RDH, DNS, HTTP/S, )
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 Configure Network Security Groups (NSGs):
- Step 2 Use Wireshark to Capture Traffic:
- Step 3 Analyze Traffic Using Command Lines:

<h2>Actions and Observations</h2>

<p>
<img width="755" alt="Screenshot 2024-12-28 at 9 42 26 PM" src="https://github.com/user-attachments/assets/3b8796fb-4eef-4e17-b10a-7360fb9153c6" />

</p>
<p>
To analyze networks you need to install and open a packet sniffing program the one i used here is Wire shark this what the interface looks like after you connect to your network.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-12-28 at 9 46 21 PM" src="https://github.com/user-attachments/assets/afd722a8-5fcc-4b7e-8b76-fe887081fc81" />

</p>
<p>
To manipulate network traffic you will need to use command line prompts so you will need to open a program called powershell for windows 
</p>
<br />

<p>
<img width="750" alt="Screenshot 2024-12-28 at 9 47 40 PM" src="https://github.com/user-attachments/assets/be673f31-ad8e-4cd2-98a4-3132e02ff844" />

</p>
<p>
Once you are setup, in Wireshark, you can filter the scan for whatever type of traffic you would like to monitor. Here i am filtering for ICMP traffic and later will filter for SSH DHCP
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-12-28 at 10 02 17 PM" src="https://github.com/user-attachments/assets/d96c9de7-a4b0-4eb4-a1bd-f74672052336" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="750" alt="Screenshot 2024-12-28 at 9 48 25 PM" src="https://github.com/user-attachments/assets/2ff02d9a-47b1-4280-b9cb-67908fac3ef5" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="751" alt="Screenshot 2024-12-28 at 10 38 38 PM" src="https://github.com/user-attachments/assets/40db2c5c-a360-4770-a2db-415c571aee9a" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-12-28 at 10 50 32 PM" src="https://github.com/user-attachments/assets/5e6e3725-bfa1-4172-abf6-511d24c1325c" />


</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2025-01-02 at 9 36 48 PM" src="https://github.com/user-attachments/assets/b3820c0b-0cdb-4922-9158-b3cba640a093" />

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
