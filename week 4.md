# Week 4 – Initial System Configuration & Security Implementation

## Introduction
The aim of Week 4 was to securely install Ubuntu Server and apply basic security measures. All configurations were done over SSH from the Ubuntu Workstation, adhering to the administrative limitation. This week involved enhancing authentication security, limiting network access, and implementing proper user privilege management.

---

## 1. SSH Key-Based Authentication Configuration
The security of SSH was enhanced by implementing key-based authentication in place of relying on password authentication.

To begin with, an SSH key pair was created for the admin user. Then, the public key was uploaded to the server via the `ssh-copy-id` command. This enables secure login without password authentication.

After the copying of the key was completed successfully, the SSH access via the key was also checked for its accuracy. The process lowers the chances of having brute force attacks and offers strong authentication.

**Outcome:** The enabling and verification of SSH key-based authentication were completed successfully.

---

## 2. Setting Up a Firewall (Restricted SSH Access)
To limit SSH access, a firewall was set up using UFW (Uncomplicated Firewall).

The firewall was configured to:
- Permit SSH (port 22) only from the IP address of the Ubuntu Workstation (`192.168.56.102`).
- By default, block all other incoming connections.

The firewall was turned on after the rule was defined, and the active rules were verified by checking the firewall status.

**Outcome:** Network security was enhanced since only the workstation has SSH access to the server.

---

## 3. Management of Users and Privileges
To prevent direct root login, a non-root administrative user (`adminuser`) was created.

This user was added to the `sudo` group, enabling the safe execution of administrative commands via `sudo` rather than logging in as root.

Using a non-root admin user increases accountability and lowers the possibility of unintentional system damage.

**Outcome:** Secure privilege separation was successfully implemented.

---

## 4. Proof of SSH Access
The new administrative user was used to test SSH access from the workstation.

Confirmed successful login verified that:
- The SSH service is operational.
- Key-based authentication is functioning correctly.
- Firewall rules permit access from the appropriate IP address.

**Outcome:** Remote SSH access was confirmed and recorded.

---

## 5. Configuration File Changes (Before & After)
The SSH configuration file (`/etc/ssh/sshd_config`) was reviewed and modified to support secure settings such as:
- Disabling root login.
- Ensuring key-based authentication is enabled.

Screenshots were captured before and after the changes to show configuration differences.

**Outcome:** SSH hardening changes were properly documented.

---

## 6. Firewall Documentation
Firewall rules were reviewed using `ufw status verbose`.

The output confirmed:
- SSH is allowed only from the workstation.
- The firewall is enabled and active.

This documentation shows the complete firewall ruleset in place.

---

## 7. Remote Administration Evidence
All configuration tasks (user creation, firewall setup, and SSH configuration) were executed via SSH from the workstation and not from the server console.

This demonstrates proper remote system administration as required.

---

## Conclusion
In Week 4, fundamental concepts of Linux server security were learned, including firewall management, privilege control, and SSH hardening. By implementing these controls, the system was prepared for upcoming performance testing and provided practical experience with real-world server security procedures.
