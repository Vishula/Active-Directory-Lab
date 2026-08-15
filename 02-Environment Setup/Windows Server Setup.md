<img width="709" height="386" alt="image" src="https://github.com/user-attachments/assets/7719518e-26bc-4f28-a1aa-d3f0ac3f4a15" /># Windows Server 2022 Setup 

In this state, I installed and configured Windows Server 2022 as the Domain Controller (DC) for my lab environment. The process included setting a static IP, changing the computer name, installing AD DS, and promoting the server to a DC. 

# Installation 

- Created a new virutal machine in ESXi with a 8GB RAM, 2 CPUs, 40GB

<img width="1026" height="794" alt="image" src="https://github.com/user-attachments/assets/9ddb2ecc-0968-403e-9a9e-00a607b80226" />


# First Boot Desktop After installation finish 

<img width="1030" height="633" alt="image" src="https://github.com/user-attachments/assets/4df11459-edb8-4af5-a655-a29bf7aa0aa8" />

# Initial Configuration 

After installation, I performed the following: 

- Changed the machine name to WinServer2022
- Set a static IP address: 192.168.1.10
- Configured DNS to point to itself (192.168.1.10)
- Set the computer's time zone

# Network settings shows static IP and DNS config 

If DNS setup isn't done, internet will not work. You can use 8.8.4.4 if you want to access the internet on the server
<img width="941" height="423" alt="image" src="https://github.com/user-attachments/assets/fee5bd21-634d-4806-b997-cc7f554ba6f2" />

# System > About > Computer Name 
<img width="354" height="308" alt="image" src="https://github.com/user-attachments/assets/f55c67ff-6908-4c5c-adc6-ef4771c8490e" />

# Installing AD DS Role 

- Opened Server Manager > Dashboard Section
- Selected Add Roles and Features
- Installation Type > Role based or Feature based installation 
- Installed the Active Directory Domain Services (AD DS) role

<img width="703" height="464" alt="image" src="https://github.com/user-attachments/assets/4325b3f5-8199-424c-aad6-366ce461e0f0" />

# Promoting to Domain Controller 

- Promoted the server to a DC using the post installation wizard
- Created a new forest named ozlab.local
- Accepted the default NetBIOS name: OZLAB
- Paths for db, logs C:\\Windows\NTDS
- Rebooted the machine after setup completed
- Created a DSRM password. DSRM password is a local admin password used to log into Windows AD DC when its running in safe repair mode. It lets you fix, restore, troubleshoot broken AD database when normal directory services are turned off.

- Domain Configuration Summary Before Installation 
<img width="531" height="391" alt="image" src="https://github.com/user-attachments/assets/8df0dbd3-741c-47d3-a795-d91aa593a9a1" />

# Installation started 
<img width="533" height="396" alt="image" src="https://github.com/user-attachments/assets/4b47eaf0-614b-42e3-991a-4c1b15e55af6" />

# Confirmation of Successful Promotion 
<img width="709" height="386" alt="image" src="https://github.com/user-attachments/assets/a3514f0f-879b-4196-aeba-c7edcb897e5c" />

# Windows Server restarted. Applying computer settings now. 
<img width="438" height="263" alt="image" src="https://github.com/user-attachments/assets/829b808e-02a0-4883-9542-c0ef4e853d3a" />

# ADUC initial screen after restart. 
- At this point nothing is created in the domain controller. 
<img width="532" height="374" alt="image" src="https://github.com/user-attachments/assets/4292b67a-37f9-49ca-ac63-b403b4be6518" />

# Post Installation Checks 

- Logged in using the domain admin account
- Verified domain controller health using dcdiag in PowerShell
- Ensured DNS was properly installed and functioning
- Confirmed that AD related services are running 

# PS with dcdiag /V results 

<img width="1423" height="988" alt="image" src="https://github.com/user-attachments/assets/b82b2650-b463-4db7-b6b6-8b81e587903b" />
<img width="1421" height="1014" alt="image" src="https://github.com/user-attachments/assets/150a649b-8d12-475d-9770-0f3c4692ab76" />
<img width="1426" height="1003" alt="image" src="https://github.com/user-attachments/assets/18b88858-5960-4c1b-8213-75848e54980c" />

# DNS Manager Showing Forward Lookup Zone for ozlab.local 
<img width="527" height="369" alt="image" src="https://github.com/user-attachments/assets/be633178-4d0c-483b-b09d-3f62f6da382e" />

# Summary 

- Server Name: WinServer2022
- Staic IP: 192.168.1.10
- DNS Server: 192.168.1.10 (local)
- Domain Controller Type: New Forest 
- Domain Name: ozlab.local
- AD Role Installed: AD DS 


