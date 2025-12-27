# Project Overview

The objective of Week 3 was to identify appropriate applications that represent different workload types for performance testing. These applications will be used subsequently for analysis purposes related to the behaviour of the operating system with varied workloads including CPU saturation, Memory, Disk I/O Operations, Network Activity, and Server Workloads.

## Application Selection Matrix

### 1. CPU-Intensive Application – stress-ng
stress-ng was chosen as the tool for stressing the CPU to high load levels. It provides the ability to validate CPU performance against heavy loads.

### 2. RAM-Intensive Application – stress-ng
stress-ng was also chosen to stress the system's memory by allocating considerable amounts of RAM. This facilitates the analysis and detection of potential swapping.

### 3. I/O-Intensive Application – fio
fio was selected to test disk reads and writes. This tool is effective in analyzing disk I/O performance, throughput, and latency.

### 4. Network Intensive Application – iperf3
iperf3 has been used to evaluate the throughput and delay of the network from the workstation to the server. The tool is helpful when analyzing the performance of the network when it is under stress.

### 5. Server Application – Apache2
Apache2 was chosen as the server application because it is a real-world web server. That is, this package enables the computation of service time, CPU time, and memory space while handling requests from the client.

## Installation Documentation (SSH-Based)

All applications were installed over SSH from the Ubuntu Workstation because of the administrative constraint. All were installed on the Ubuntu Server.

## Installation Commands

The following commands were used:

```bash
sudo apt update
sudo apt install -y stress-ng
sudo apt install -y fio
sudo apt install -y iperf3
sudo apt install -y apache2
