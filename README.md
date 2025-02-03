# Active Directory Homelab Project

## Overview
This project focuses on setting up a homelab environment to simulate an **Active Directory** (AD) infrastructure with security monitoring, penetration testing, and incident detection. The homelab includes various **Windows and Linux VMs**, **Splunk**, **Sysmon**, and **Atomic Red Team** for testing attack scenarios.

## Lab Environment
The following virtual machines (VMs) were used:

- **Windows 10** – Target PC (Client)
- **Windows Server 2022** – Domain Controller (DC)
- **Ubuntu Server** – Splunk Server
- **Kali Linux** – Attack machine

## Objectives
1. **Set up a virtualized lab network** using VirtualBox.
2. **Configure Active Directory (AD)** on Windows Server 2022.
3. **Join a Windows 10 machine** to the domain.
4. **Install and configure Splunk** on Ubuntu to collect logs from Windows devices.
5. **Deploy Sysmon and Splunk Universal Forwarder (SUF)** for event logging.
6. **Use Kali Linux to simulate attacks** and detect security events in Splunk.
7. **Implement Atomic Red Team (ART)** to generate and analyze adversary behaviors.

---

## Steps & Configuration

### 1. **Setting up Virtual Machines**
- Installed **Windows Server 2022**, **Windows 10**, **Ubuntu Server**, and **Kali Linux**.
- Configured **NAT Network** in VirtualBox for inter-VM communication.

### 2. **Active Directory Setup**
- Installed **Active Directory Domain Services (AD DS)** on Windows Server.
- Created an **Organizational Unit (OU) `_USERS`** and added **50 users** via PowerShell.

### 3. **Configuring Splunk**
- Installed Splunk **Enterprise** on Ubuntu.
- Configured **Splunk Forwarders** on Windows machines to send logs to Splunk.

### 4. **Deploying Sysmon for Advanced Logging**
- Installed **Sysmon** and applied **Olaf’s Sysmon Configuration**.
- Set up Splunk **inputs.conf** to capture:
  - Security Logs
  - System Logs
  - Sysmon Logs

### 5. **Simulating Attacks & Monitoring**
- Used **Crowbar** on Kali Linux for **RDP brute-force attacks**.
- Ran **Atomic Red Team (ART) tests** to simulate:
  - Privilege Escalation
  - Account Creation
  - PowerShell Execution
- Verified **telemetry in Splunk** for attack detection.

---

## Key Learnings
- **Windows Server Administration:** Managing AD, users, and policies.
- **Security Monitoring:** Using **Splunk + Sysmon** to detect attacks.
- **Red Teaming & Defense:** Understanding **MITRE ATT&CK techniques**.
- **Networking & Virtualization:** Setting up **NAT Networks** and **firewall rules**.

---

## Future Improvements
- Implement **Group Policy Objects (GPOs)** for security hardening.
- Integrate **Elastic Stack (ELK)** for alternative logging.
- Deploy **Microsoft Defender ATP** for endpoint security.

---

## Resources
- [Splunk Docs](https://docs.splunk.com/)
- [MITRE ATT&CK](https://attack.mitre.org/)
- [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
- [Sysmon Configuration](https://github.com/olafhartong/sysmon-modular)

---

## Author
👤 **[Atikor Ibodeng]**  
🔗 **GitHub:** [GitHub Profile](https://github.com/rokita28)

