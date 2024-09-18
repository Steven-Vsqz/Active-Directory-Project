<h1 align="center">Active Directory Lab with Splunk, Sysmon, and Kali Linux</h1>

This project showcases a hands-on Active Directory lab environment designed to simulate real-world scenarios involving network security, attack detection, and incident response.
<br />

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
<summary><h2>Active Directory Setup</h2></summary>

This guide covers the steps to configure an Active Directory (AD) environment, including domain controller setup, Group Policy administration, user/group management, and DNS configuration.

<h3>1. Domain Controller Setup</h3>
Install Active Directory Domain Services (AD DS):

- Open Server Manager > Add Roles and Features.
- Select Active Directory Domain Services and follow the prompts.
- Once installed, click the flag icon in Server Manager to promote the server to a domain controller.

<h3>Promote Server to Domain Controller:</h3>

- Choose Add a new forest and specify your root domain (e.g., myhomelab.local).
- Configure the Domain and Forest functional levels, and set the Directory Services Restore Mode (DSRM) password.
- Let the system configure DNS and other services, then restart the server.

<h3>Verify AD Installation:</h3>

- Open Active Directory Users and Computers to confirm the domain creation.

<img src="https://github.com/user-attachments/assets/4ee4d081-2892-40b7-b3cd-db6e5283fafe" style="height: 85%; width: 85%;">
  
<h2>2. Group Policy Management</h2>
Access Group Policy Management:

- Open Group Policy Management in Server Manager or via the Start Menu.
- Create an Organizational Unit (OU):
- In Active Directory Users and Computers, right-click the domain, select New > Organizational Unit, and name it (e.g., HR).

<img src="https://github.com/user-attachments/assets/94cc8298-e26f-4cce-be76-6986cb0361b7" style="height: 85%; width: 85%;">

Create and Edit Group Policy Objects (GPOs):

- In Group Policy Management, right-click the domain or OU and select Create a GPO.
- Configure security settings such as password policies:
- Go to Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy.
- Adjust settings like password complexity and lockout policies.
<img src="https://github.com/user-attachments/assets/5654fc28-ab0a-4f34-aa93-0d7c4c9c32df" style="height: 85%; width: 85%;">

<h2>3. User and Group Management</h2>
Create User Accounts:

- In Active Directory Users and Computers, right-click the OU you created and select New > User.
- Complete the wizard to create users and set an initial password.
<img src="https://github.com/user-attachments/assets/a68a4805-628a-49a7-917c-93c0f12fd972" style="height: 85%; width: 85%;">

Create Security Groups:

- In the same OU, right-click and select New > Group.
- Define group names and select Security as the group type.
<img src="https://github.com/user-attachments/assets/98c199e6-61c5-4c2e-8f0c-ccbd786a81bf" style="height: 85%; width: 85%;">

Assign Users to Groups:

- Right-click a user account, choose Add to a group, and select the security group (e.g., HR_Admins).
<img src="https://github.com/user-attachments/assets/b415eaaa-23df-416f-901c-ab5a09c28366" style="height: 85%; width: 85%;">

<h2>4. DNS Configuration</h2>
Configure DNS Forward Lookup Zone:

- Open DNS Manager from Server Manager.
- Right-click Forward Lookup Zones > New Zone, and create a zone for your domain (e.g., myhomelab.local).
<img src="https://github.com/user-attachments/assets/c0bb3e5a-b54d-45bb-871e-7047f0ff9fd0" style="height: 85%; width: 85%;">

Create DNS Records:

- Add necessary records (e.g., A records) for servers or services.
<img src="https://github.com/user-attachments/assets/355c73db-3f36-4546-80e5-82240ce56785" style="height: 85%; width: 85%;">

Test DNS Resolution:

- On a domain-joined client, open command prompt and run `nslookup myhomelab.local` on  to ensure DNS is functioning correctly.
<img src="https://github.com/user-attachments/assets/72f0aac9-180d-4661-9c74-3ce3267bc113" style="height: 15%; width: 30%;">
</details>


