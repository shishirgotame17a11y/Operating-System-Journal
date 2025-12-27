# Phase 6 – Performance Evaluation and Analysis

## Introduction
The target for Week 6 was to conduct performance testing for Ubuntu Server and examine its behavior with varied levels of workload. The target for Week 3 was to select applications to be used for testing CPU performance, memory performance, disk I/O performance, network performance, system latency, and services with varied workload levels. All these tasks were completed from the Ubuntu Workstation using SSH, in line with administrative constraints.

---

## 1. Testing Methodology
Performance testing was conducted systematically to achieve consistent and reliable results.

### Baseline Performance Testing
Baseline testing was carried out with low system loads in order to understand normal system behavior.

### Application Load Testing
Each application was run separately to target a specific system resource:
- CPU stress using `stress-ng`
- Memory stress testing using `stress-ng`
- Disk I/O benchmarking using `fio`
- Network testing using `iperf3`
- Service testing using `Apache2`

### Performance Analysis
The results from baseline testing and load testing were compared to identify system limitations.

### Optimization Testing
System optimizations were applied and tests were run again to evaluate performance improvements. At least two system optimizations were implemented.

---

## 2. Performance Metrics Monitored
The following system metrics were monitored during testing:
- **CPU usage:** `top`, `uptime`
- **Memory utilization:** `free -h`
- **Disk I/O performance:** `df -h`, `iostat`
- **Network performance:** `iperf3`
- **System latency:** `ping`
- **Service times and availability:** Apache access and response tests

---

## 3. Results of Performance Testing

### Performance Data Table

| Application            | CPU Usage  | Memory Usage | Disk I/O   | Network     | Notes                           |
|------------------------|------------|--------------|------------|-------------|---------------------------------|
| Baseline               | Low        | Low          | Low        | Low         | System idle                     |
| Stress-ng (CPU)        | Very High  | Low          | Low        | Low         | CPU saturation observed         |
| Stress-ng (Memory)     | Medium     | Very High    | Low        | Low         | Swap activity observed          |
| fio                    | Medium     | Low          | Very High  | Low         | Disk I/O bottleneck             |
| iperf3                 | Low        | Low          | Low        | Very High   | High throughput                 |
| Apache2                | Medium     | Medium       | Low        | Medium      | Increased response time under load |

---

## 4. Network Performance Analysis
Network performance was analyzed using `ping` and `iperf3`.

- **Latency:** Measured using ICMP ping between the workstation and the server.
- **Throughput:** Tested using `iperf3` in client-server mode.

In Host-only mode, latency and throughput were stable, making the environment suitable for internal testing.

---

## 5. Optimization and Improvements
Two system optimizations were implemented:

### Optimisation 1: Background Services
Unused services were disabled to free system resources and reduce CPU and memory overhead.

### Optimisation 2: Disk I/O Scheduling Enhancement
Disk I/O behavior improved after optimization, resulting in reduced I/O wait times during `fio` testing.

After optimization, performance tests showed reduced latency and improved responsiveness.

---

## 6. Testing Evidence
Evidence of performance testing included screenshots of terminal output showing:
- Test execution
- Baseline monitoring
- Application load execution

---

## Reflection
In Week 6, hands-on experience was gained in analyzing operating system performance under real-world workloads. By comparing baseline performance with stressed conditions, system bottlenecks and the effects of performance optimizations were better understood. At this stage, performance testing proved essential for making informed judgments about system performance.
