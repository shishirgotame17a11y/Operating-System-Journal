# Week 1: System Planning and Distribution Selection

## Overview
The objective for Week 1 was to design and implement a initial client server system platform using Oracle VirtualBox. For week one, the emphasis was on identifying appropriate Linux distributions and understanding system architectures, virtual networking, and system properties using the command line interface. Setting up a system for week one provides a platform for system security settings and system performance tuning.

## System Architecture Overview
The environment comprises two virtual machines running on a Windows host machine utilizing the VirtualBox technology by Oracle. Ubuntu Server 24.04 LTS and Ubuntu Desktop 24.04 LTS installations comprise the environment. The two virtual machines connect via a Host-only connection that enables secure internal communications. The server can be controlled by remote login over an SSH connection established by the workstation.

## Distribution Selection Reasoning
A decision to use Ubuntu Server 24.04 LTS was based on it being lightweight, stable, as well as qualified to receive security updates for a long time. The system is popular for deployment on servers to be secure. Ubuntu Desktop 24.04 LTS was chosen for use on the workstation due to its GUI making it easy to administer, monitor, and document.

## Determining Workstation Configuration
The workstation is equipped with Ubuntu Desktop, making it convenient for working with the server. The GUI makes tasks like SSH connectivity, server monitoring, and taking screenshots easy. This is ideal for use as an administration and test workstation.

## Computer Network Architecture
A Host-only adapter connection in VirtualBox enabled the server and workstation to communicate with each other while protecting the network environment from the outside world.

## Network Details
- **Subnet:** 192.168.56.0/24  
- **Server IP Address:** 192.168.56.103  
- **Workstation IP Address:** 192.168.56.102  

## Command-Line Verification
System configuration and specifications were checked using various command line tools that are provided under the Linux operating system. The command lines used include:

- `uname -a` for checking system kernels  
- `free -h` for checking system memory  
- `df -h` for checking system disks  
- `ip addr` for checking IP addresses  
- `lsb_release -a` for checking system distributions  

## SSH Verification
The remote access of the server was also checked from the workstation through SSH. Successful connection ensured the network settings and SSH service were working well.

## Reflection
Week 1 aided in the understanding of virtualisation, Linux distributions, basic networking, and remote administration. This current setup offers an excellent foundation on which to focus on the implementation of security and performance in the next week.
