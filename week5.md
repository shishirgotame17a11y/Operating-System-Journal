# Class 5: Advanced Security and Monitoring Infrastructure

## Introduction
The objective of Week 5 was to improve the security of the Ubuntu Server by integrating sophisticated security control and monitoring tools. This stage of the project expands on the work that was completed in Week 4 by focusing on enforcing access control policies, intrusion prevention, automated security updates, as well as custom security verification scripts. Additionally, all of this work was completed through remote access of the Ubuntu Workstation via SSH.

---

## Access Control with AppArmor
AppArmor was used to implement Mandatory Access Control (MAC) on the server. It restricts how applications can access system resources and helps reduce the impact of compromised services.

### Implementation
- AppArmor is installed and running on Ubuntu Server.
- Active AppArmor profiles were reviewed to verify that protection was enabled for system services.
- Profiles were maintained on a enforcing profile to prevent illegitimate action.

### Documentation and Verification
- AppArmor status was confirmed using:
  - `sudo – aa status`
- The command displays the loaded, enforcing, and complain-mode profiles, thus validating the enforcement of access control.

### Purpose
AppArmor prevents applications from accessing files or resources that go beyond the defined scope of an application’s permission.

---

## Automatic Security Updates Configuration
Automatic security updates were enabled to ensure that the server gets all critical security patches automatically.

### Implementation
- The package for unattended upgrades was installed and enabled.
- The security repositories were set up to enable automatic patch installation.

### Verification
- The configuration file was verified in order to ensure security patches were enabled:
- /etc/apt/apt.conf.d/50unattended-upgrades
- - The service status was checked to make certain updates would occur automatically.

### Purpose
This cuts down on the risks from known vulnerabilities and keeps the system current.

---

## Fail2Ban Configuration
Fail2Ban was set up for intrusion protection and protection from brute force attacks.

### Implementation
- Fail2Ban was installed in the server.
- Sshd jail/SSH protection was enabled.
- The software tracks login records and locks down IP addresses that have repeatedly failed logins.

### Verification
- Illicit activities of Fail2Ban were evaluated.
- The following commands were used:
- `sudo systemctl status fail2ban`
- `sudo fail2ban-client status`

### Purpose
“Fail2Ban” is a tool capable of automatically banning suspicious IP addresses to safeguard SSH servers against any kind.

---

## Security Baseline Verification Script
To ensure that all the security settings of Weeks 4 and 5 remain enabled, a security verification script was developed.

### Script Functionality
The script evaluates:
- SSH service status.
- FireWall (UFW) status and rules.
- AppArmor status.
- Fail2Ban service.
- Automatic updates configuration.

### Execution
- Script execution happens on the server.
- It is done remotely using SSH from the workstation.

### Conclusion
It allows a quick and repeatable check of the security posture of the system.

---

## Remote Monitoring Script
A script for monitoring was developed on the workstation to gather performance data from the server through SSH.

### Metrics Collected
- CPU usage
- Usage of memory
- Disk usage
- System availability
- Network Statistics

### Execution
- The script uses SSH to connect to the server.
- All commands are carried out remotely.
- Output is shown in the workstation terminal.

### Purpose
This allows for monitoring without having to log in to the server console.

---

## Reflection
In Week 5, the understanding and awareness pertaining to advanced concepts associated with Linux security, such as Mandatory Access Control, intrusion prevention, automation, and scripting, were enhanced. The use of scripts for validation and monitoring reflected real-world system administration techniques and emphasized the significance associated with multi-layered security mechanisms.

