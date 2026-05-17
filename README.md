# 🧱 Windows Active Directory Home Lab (Enterprise Simulation)

## 📌 Overview

This project simulates a small enterprise IT environment using Windows Server and Active Directory. The goal was to design, deploy, and manage a fully functional domain-based infrastructure including user management, group policy enforcement, and secure file sharing.

This lab demonstrates core IT and cybersecurity skills such as identity management, access control, DNS dependency, system administration, and troubleshooting in a Windows domain environment.

---

## 🏗️ Lab Architecture

            +----------------------+
            |   DC01 (Server)      |
            |----------------------|
            | Active Directory     |
            | DNS Server           |
            | Group Policy         |
            | File Sharing         |
            +----------+-----------+
                       |
                       | corp.local Domain
                       |
            +----------v-----------+
            |   PC01 (Client)     |
            |---------------------|
            | Windows 10/11       |
            | Domain Joined       |
            | User: CORP\jsmith   |
            +---------------------+
            
---

## 🛠️ Tools & Technologies

- Oracle VM VirtualBox  
- Windows Server 2022 Evaluation  
- Windows 10/11 Client  
- Active Directory Domain Services (AD DS)  
- DNS Server  
- Group Policy Management  
- NTFS & SMB File Sharing  
- Command Line / Windows Admin Tools  

---

## ⚙️ Project Phases Summary

### Phase 0 – Environment Setup
- Verified virtualization support and system readiness
- Organized project directory structure

### Phase 1 – Virtualization Setup
- Installed Oracle VM VirtualBox
- Configured isolated virtual lab environment

### Phase 2 – ISO Preparation
- Downloaded Windows Server 2022 Evaluation ISO
- Downloaded Windows 10/11 ISO
- Stored installation media in organized directory

### Phase 3 – Domain Controller Setup (DC01)
- Created Windows Server virtual machine
- Installed Windows Server OS
- Configured initial system environment
- Created snapshot: Fresh Install

### Phase 4 – Network Configuration
- Assigned static IP to DC01
- Configured DNS pointing to itself
- Ensured stable server networking

### Phase 5 – Active Directory & DNS Installation
- Installed AD DS and DNS roles
- Promoted server to Domain Controller
- Created domain: `corp.local`

### Phase 6 – Active Directory Structure
- Created Organizational Units (IT, HR, Computers)
- Created users: jsmith, mjones
- Created security groups: HR_Users, IT_Admins
- Assigned users to groups

### Phase 7 – Client Setup (PC01)
- Installed Windows 10/11 on client VM
- Configured network settings for domain access

### Phase 8 – Domain Join
- Joined PC01 to `corp.local` domain
- Configured DNS to point to DC01
- Logged in using domain credentials (CORP\jsmith)

### Phase 9 – Group Policy
- Created and applied Group Policy Objects
- Configured password, desktop, and control panel restrictions
- Verified policy application using gpupdate

### Phase 10 – File Sharing & Permissions
- Created shared folders:
  - C:\Shared\HR
  - C:\Shared\IT
- Applied NTFS and Share permissions
- Implemented role-based access control using security groups

### Phase 11 – Troubleshooting & Simulation
- Simulated DNS misconfiguration and restored connectivity
- Resolved account lockout via Active Directory
- Diagnosed Group Policy issues using gpresult

---

## 🧠 Key Skills Demonstrated

- Active Directory administration  
- Domain controller deployment  
- DNS configuration and dependency understanding  
- Group Policy management  
- Role-based access control (RBAC)  
- Windows file sharing and permissions  
- Troubleshooting Windows enterprise environments  
- Command-line diagnostic tools  

---

## 📸 Screenshots

Screenshots documenting each phase are available in the `/screenshots` directory.

---

## 📊 What I Learned

- How enterprise identity systems are structured using Active Directory  
- How DNS is critical for domain functionality  
- How Group Policy controls user and system behavior  
- How permissions are enforced using security groups  
- How to troubleshoot real-world Windows domain issues  

---

## 🚀 Future Improvements

- PowerShell automation for user/group creation  
- Advanced Group Policy hardening  
- SIEM/log monitoring integration  
- Multi-site domain simulation  
- Backup and recovery testing  

---

## 📌 Summary

This project demonstrates the full lifecycle of designing, deploying, and managing a Windows-based enterprise domain environment, including configuration, security enforcement, and troubleshooting.

It serves as a practical hands-on simulation of real-world IT systems administration and cybersecurity operations.
