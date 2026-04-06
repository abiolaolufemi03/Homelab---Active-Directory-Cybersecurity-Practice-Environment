# Homelab---Active-Directory-Cybersecurity-Practice-Environment
This lab simulates a small enterprise network with a dedicated Domain Controller, client machines, and a pfSense firewall separating an "Attack LAN" (Kali Linux) from the "Homelab" domain. It is designed to demonstrate real-world IT infrastructure and security skills.
# Homelab - Active Directory & Cybersecurity Practice Environment

## Project Overview

A fully functional Windows Active Directory homelab environment built in Oracle VirtualBox for hands-on practice in **System Administration**, **Active Directory management**, **Group Policy**, and **Cybersecurity fundamentals**.

This lab simulates a small enterprise network with a dedicated Domain Controller, client machines, and a pfSense firewall separating an "Attack LAN" (Kali Linux) from the "Homelab" domain. It is designed to demonstrate real-world IT infrastructure and security skills.

**Purpose**:  
To build practical experience in Windows Server administration, domain management, security configuration, and red team/blue team concepts for career development in **Cybersecurity** and **IT Systems Administration**.

## Lab Architecture

- **Hypervisor**: Oracle VirtualBox
- **Firewall/Router**: pfSense (acting as perimeter firewall)
- **Domain**: `Homelab.local`
- **Domain Controller**: Windows Server 2025 (DC-1)
- **Clients**: Windows 10/11 workstations (`labuser1`, `labuser2`)
- **Attack Machine**: Kali Linux (Attack LAN)

### Network Layout
- **WAN**: 192.168.1.249 (pfSense)
- **Homelab LAN**: 10.0.1.0/24
- **Attack LAN**: 10.0.3.0/24

## Features & Configurations Implemented

### Active Directory Setup
- Installed and configured **Active Directory Domain Services (AD DS)** on Windows Server 2025
- Created domain `Homelab.local`
- Configured DNS and DHCP services
- Successfully joined Windows client machines to the domain
- Created domain users (`labuser1`, `labuser2`)

### Security & Hardening
- Installed **Active Directory Certificate Services (AD CS)**
- Configured firewall rules in pfSense:
  - Controlled traffic between Attack LAN and Homelab
  - Allowed internet access from Homelab while blocking unnecessary traffic
  - Created custom aliases (RFC1918)
- Applied Group Policy to disable Windows Defender (for lab testing purposes)
- Configured secure remote access and basic hardening policies

### Management & Tools
- Installed and configured **Group Policy Management**
- Deployed basic security policies via GPO
- Guest Additions installed on all virtual machines for better performance
- Full domain join verification with proper credentials

## Technologies Used

- **Windows Server 2025** (Domain Controller)
- **Active Directory Domain Services**
- **Group Policy**
- **pfSense** (Firewall & Routing)
- **Kali Linux** (Attack/Testing Machine)
- **Oracle VirtualBox**
- **Windows 10/11** (Domain-joined clients)
- **DNS, DHCP, AD CS**

## Skills Demonstrated

- Windows Server installation and role configuration
- Active Directory design and administration
- Domain joining and user management
- Network segmentation and firewall rule management
- Group Policy creation and enforcement
- Basic lab security hardening
- Virtualisation and homelab architecture

## Project Status

**Completed** – March 2026s

---

**Made with ❤️ for learning and career growth in Cybersecurity & Systems Administration**
