# DNS configuration for Active Directory 

This section shows how i configured the Domain Name System (DNS) on my Windows Server 2022 Domain Controller to ensure proper name resolution within the domain environment.

# DNS Role Configuration 

During the Active Directory Domain Services (AD DS) installation and domain promotion process, DNS Server role was installed automatically. 

# Key Settings: 

- Forward Lookup Zone: ozlab.local (Active Directory-integrated) 
- Reverse Lookup Zone: 

# DNS Manager Showing the Forward Lookup Zone for ozlab.local 

# Reverse Lookup Zone Creation Wizard 

# Zone Type 
<img width="764" height="440" alt="image" src="https://github.com/user-attachments/assets/9b0d60bf-ab23-4ac9-9dc2-72bec6185fed" />

# AD Zone Replication Scope 
<img width="766" height="363" alt="image" src="https://github.com/user-attachments/assets/3f897202-3125-4765-94f0-e70d35544d7b" />

# Zone Name 
<img width="768" height="377" alt="image" src="https://github.com/user-attachments/assets/663653e6-fae1-4012-9f21-e8f092285547" />

# Zone Name Network ID 
<img width="768" height="381" alt="image" src="https://github.com/user-attachments/assets/4316081f-6f4a-4ea9-a384-99d6cf891a7f" />

# Dynamic Updates 
<img width="761" height="378" alt="image" src="https://github.com/user-attachments/assets/774c2a9d-2eab-4dc2-bc6a-02ec67c96bd9" />






