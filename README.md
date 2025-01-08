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
Once you are setup, in Wireshark, you can filter the scan for whatever type of traffic you would like to monitor. Here i am filtering for ICMP traffic and later will repeat this filter process for SSH,DHCP,DNS,RDP traffic respectively.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-12-28 at 10 02 17 PM" src="https://github.com/user-attachments/assets/d96c9de7-a4b0-4eb4-a1bd-f74672052336" />

</p>
<p>
Retrieve the private IP address of whatever other computer you are testing connectivity to and attempt to ping it from within the Windows 10 VM
using Powershell typing in the prompt: ping (ip address) *In the above example i ping the linux VM*
</p>
<br />

<p>
<img width="750" alt="Screenshot 2024-12-28 at 9 48 25 PM" src="https://github.com/user-attachments/assets/2ff02d9a-47b1-4280-b9cb-67908fac3ef5" />

</p>
<p>
Observe the traffic in Wireshark
</p>
<br />

<p>
<img width="751" alt="Screenshot 2024-12-28 at 10 38 38 PM" src="https://github.com/user-attachments/assets/40db2c5c-a360-4770-a2db-415c571aee9a" />

</p>
<p>
Reset your traffic filter in Wireshark to SSH only
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-12-28 at 10 50 32 PM" src="https://github.com/user-attachments/assets/5e6e3725-bfa1-4172-abf6-511d24c1325c" />


</p>
<p>
Open PowerShell, and type: ssh labuser@<private IP address>,Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark


</p>
<br />

<p>
<img width="1470" alt="Screenshot 2025-01-02 at 9 36 48 PM" src="https://github.com/user-attachments/assets/b3820c0b-0cdb-4922-9158-b3cba640a093" />

</p>
<p>
In Wireshark, filter for DHCP traffic only and Open PowerShell as admin and run: ipconfig /renew
 
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2025-01-07 at 11 38 04 AM" src="https://github.com/user-attachments/assets/05d0cf6b-9f65-4818-b392-52b81305cef5" />


</p>
<p>
In Wireshark, filter for DNS traffic only and Open PowerShell as admin and run: nslookup (url of your choice). In the my example I use disney.com *note that using this prompt gives you the ip address of the website and that can be used if youre trying to find out the website name associated with the ip address.* 
 
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2025-01-07 at 11 37 41 AM" src="https://github.com/user-attachments/assets/6b8b8286-782d-405f-b522-790e498da5a0" />


</p>
<p>
After obtaining the ip address  you can use it in a web browser to search up the webpage. *Due to security reasons disneys website cant be accessed this way but you can tell its disney related*
 
</p>
<br />

<p>
<img width="770" alt="Screenshot 2025-01-07 at 11 48 17 AM" src="https://github.com/user-attachments/assets/543d24ab-92d1-43e1-984a-76589d02f00a" />


</p>
<p>
In Wireshark set your filter for RDP traffic only byt using "tcp.port==3389" since we are already remotely accessing the computer in a VM there is constant traffic already happening.
 
</p>
<br />
