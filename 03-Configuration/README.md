# Active Directory Configuration 

# Overview

This section of the AD lab focuses on the foundational setup and configuration of AD services. It encompasses the installation and configuration of AD DS, DNS settings and essential Group Policy Objects (GPOs) to establish a secure and well structured domain environment. 

# 1. Active Directory Setup 
The initial step involes installing AD DS role and promoting the server to a domain controller. This establishes the core of the Active Diretory infrastrucutre. 

# Steps Performed: 

- Install AD DS Role: Utilized Server Manager to add the Active Directory Services role.
- Promote to Domain Controller: configured the server as a new domain controller in a new forest.
- Domain Configuration: set the Fully Qualified Domain Name (FQDN) for the new domain.
- DNS Server Installation: Opted to install the DNS Server role alongside AD DS.
- Directory Services Restore Mode (DSRM) Password: defined a secure DSRM password for recovery.

# 2. DNS Setup 

# Description 

DNS configuration is critical for the functionlaity of Active Directory as it relies on DNS for domain controller location and service discovery. 

# Steps Performed 

= DNS Role Verification: Ensured the DNS Server role was installed during AD DS setup. 
- Forward Lookup Zone Creation: Created a forward lookup zone corresponding to the domain name.
- Reverse Lookup Zone Creation: Established a reverse lookup zone for IP address to name resolution.
- DNS Records Verification: Confirmed the creation of essential DNS records, inclduing SRV and A records for domain controller.
  
