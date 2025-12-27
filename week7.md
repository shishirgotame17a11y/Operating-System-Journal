# Week 7 – Security Audit and System Review

## Overview
At the end of Week 7, a comprehensive security audit was carried out on the Ubuntu Server system to assess its general security posture. This phase of the study was designed to pinpoint vulnerabilities, review system configurations, and verify that the security controls implemented during earlier phases were effective. The study made use of industry-standard tools such as **Lynis** and **Nmap**, in addition to manual verification of SSH, access controls, and running services.

The medical staff knows him from a case of classical epilepsy with partial attacks.

---

## Scanning for Security with Lynis
An in-depth system security audit was performed using Lynis. The initial scan produced a baseline security score and highlighted several warnings and recommendations related to SSH configuration, file permissions, and overall system hardening.

By following the recommended actions, several improvements were made, including:
- Verifying firewall rule configurations  
- Further hardening of SSH settings  
- Ensuring automatic security updates were enabled  

After re-running Lynis, the system showed improved compliance and fewer warnings, indicating an overall enhancement in system security.

---

## Network Security Scanning Assessment (Nmap)
Nmap was executed from the workstation against the server over the Host-only network. The scan results indicated that only SSH (port 22) was open and accessible. All other ports were either filtered or closed.

This confirmed that firewall rules were correctly configured and that no unnecessary services were exposed to the network.

---

## SSH Security Verification
A manual review of SSH configuration was conducted to ensure secure remote access. Password-based authentication was disabled, and key-based authentication was enforced. Root login via SSH was also disabled.

Connectivity testing confirmed that SSH access was only possible from the trusted workstation IP address.

---

## Access Control Verification
AppArmor was enabled and operating in enforce mode. Active AppArmor profiles were reviewed to ensure that critical processes were properly constrained.

The AppArmor status confirmed that profiles were loaded and actively enforced, validating effective mandatory access control.

---

## Service Audit and Justification
A service audit was carried out to identify all running services on the server. Only essential services such as SSH, system logging, and network-related services were active.

No unnecessary services, such as web servers or database services, were running. This reduced the system’s attack surface and aligned with the principle of least privilege.

---

## System Configuration Review
System configurations related to firewall rules, user privileges, automated updates, and logging were reviewed. The UFW firewall was enabled with restrictive inbound rules, sudo privileges were limited to trusted users, and unattended security updates were enabled.

Overall, the system configuration was found to be secure and compliant with best practices.

---

## Remaining Risk Assessment
Despite the secure configuration, some residual risks remain. These include potential zero-day vulnerabilities and configuration changes introduced by future updates.

To mitigate these risks, regular system updates, ongoing security audits, and continuous monitoring were recommended to maintain long-term security.

---

## Conclusion
Week 7 successfully evaluated the security posture of the Ubuntu Server system. The use of automated tools alongside manual verification ensured that the system was securely configured with minimal exposure to vulnerabilities and strong access controls in place.

This phase highlighted the importance of systematic security analysis and reinforced the value of proactive security management.
