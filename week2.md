# Week 2 – Security Planning and Testing Methodology

## 1. Performance Testing Plan

### Remote Monitoring Method
All the monitoring and testing will be done remotely from the Ubuntu Workstation using SSH. By using SSH, it is possible to control the server from a distance without having physical or console access to the machine. The standard monitoring tools available in Linux operating systems will be applied in the process so that the performance of the system can be checked without having to install any additional software.

### Testing Approach
Performance testing shall be done in steps:

- Firstly, the data will be taken with the system in the idle state.  
- Next, workloads will now be used to test CPU, memory, disk, and network resource use.  
- The results will be used for comparison purposes to identify the limits of performance.  
- Any improvements will be tested again to check their impact.  

The key performance criteria that should be monitored are the use of the CPU, memory space, disk I/O, and network response times.

---

## 2. Security Configuration Checklist

This checklist provides the planned settings for the server.

### SSH Hardening
i. The ability to log in via the “root” username over SSH will be disabled.  
ii. SSH key-based authentication will be utilized.  
iii. Password login functionality will be disabled.  
iv. SSH will be allowed only from workstation IP.  

### Firewall Configuration
i. The UFW firewall will be enabled.  
ii. Allowed SSH connections will take place from one IP address that will be trusted.  
iii. All other incoming connections would be blocked by default.  

### Mandatory Access Control
i. App Armor will be enabled.  
ii. Profiles with activities will have their services verified.  

### Automatic Updates
i. Security updates will be enabled automatically.  
ii. The system will get critical security patches automatically.  

### User Privilege Management
- An administrative user non-root will be created.  
- Access to sudo will be restricted to authorized persons only.  

### Network Security
i. It will be a Host only Network.  
ii. External network access will be limited.  
iii. Network traffic will be monitored during the tests.  

---

## 3. Threat Model

### Risk 1: SSH Brute-Force Attacks
SSH passwords can be guessed by attackers.

**Mitigations**
i. Disable password authentication.  
ii. Use SSH keys.  
iii. Limit SSH access based on IP address.  

### Risk 2: Unauthorized Privilege Escalation
User processes may attempt to gain root access without permission.

**Mitigations**
i. Replace root login with sudo.  
ii. Restrict Administrative Privileges.  
iii. Monitor system logs.  

### Risk 3: Network Attacks
The server may be vulnerable to unauthorized access from other networks.

**Mitigations**
i. Use a Host-only network.  
ii. Use a deny by default firewall rule.  
iii. Allow only required services.  
