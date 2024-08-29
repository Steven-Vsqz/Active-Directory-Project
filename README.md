<h1 align="center">Active Directory Lab with Splunk, Sysmon, and Kali Linux</h1>

This project showcases a hands-on Active Directory lab environment designed to simulate real-world scenarios involving network security, attack detection, and incident response.
<br />
<p align="center">
<img src="https://i.imgur.com/ABECAaP.png" height="80%" width="80%" alt="Failed RDP Steps"/>
</p>

<h2>🛠️Utilities & Tools Used</h2>

![image](https://img.shields.io/badge/Splunk-000000?style=for-the-badge&logo=Splunk&logoColor=white)
![image](https://img.shields.io/badge/powershell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![image](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white)
![image](https://img.shields.io/badge/VirtualBox-21416b?style=for-the-badge&logo=VirtualBox&logoColor=white)

<details open>
<summary><h2>👨‍💻Project Overview</h2></summary>

In this lab, I created a network environment using VirtualBox, featuring multiple virtual machines all interconnected within a single network. The key components of this setup include:

- <strong>Network Diagram:</strong> A visual layout of the entire network infrastructure to illustrate the relationships between virtual machines and the flow of data.
- <strong>Splunk Server:</strong> A dedicated virtual machine set up to collect and analyze telemetry data from the Windows machines. Splunk is configured to process and visualize data, aiding in the detection of malicious activities.
- <strong>Windows 10 Server & Host Computer:</strong> Both machines have Sysmon configured to collect detailed system telemetry, which is then forwarded to the Splunk server for analysis.
- <strong>Active Directory Domain Controller:</strong> The backbone of the network, this server manages the domain, users, and security policies, allowing for the exploration and learning of Active Directory fundamentals.
- <strong>Kali Linux Attacker:</strong> A virtual machine configured to simulate attacks on the host computer, generating detectable events that can be analyzed using Splunk.
 
</details>

<details open>
<summary><h2>Key Learnings</h2></summary>

From completing this project, I have gained:

- <strong>Hands-on experience with Active Directory:</strong> Understanding how to set up and manage an Active Directory domain, including user management, group policies, and domain security.
- <strong>Proficiency in Sysmon configuration:</strong> Learning how to configure Sysmon to collect detailed event data on Windows systems, and understanding the significance of different event types for security monitoring.
- <strong>Skills in Splunk for security analysis:</strong> Configuring Splunk to ingest, process, and visualize telemetry data from Sysmon, and using this data to detect and investigate security incidents.
- <strong>Understanding of cyber attack simulation and detection:</strong> Simulating cyber attacks using Kali Linux and learning how to detect these attacks through the data collected by Splunk.
- <strong>Experience in building a secure virtual network:</strong> Setting up a secure and functional network environment using VirtualBox, enhancing my overall understanding of network security principles.

</details>

![createUnit](https://github.com/user-attachments/assets/1943a6ea-abd8-4f85-8225-09c093b94706)
![addUser](https://github.com/user-attachments/assets/40c9a545-7089-4a22-a92c-b80e500f6ac5)
![verifyingLogin](https://github.com/user-attachments/assets/a74cea02-0db7-4983-8f7e-77dbff610cb0)


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
