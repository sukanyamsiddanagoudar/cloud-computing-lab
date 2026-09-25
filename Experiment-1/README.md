# Experiment 1 — Performance Analysis of Type-1 and Type-2 Hypervisors

## 1. Aim

To analyze and compare the performance of virtual machines running on Type-1 and Type-2 hypervisors using CPU, memory, disk, and CPU benchmark measurements.

## 2. Objectives

* Understand the working of Type-1 and Type-2 hypervisors.
* Deploy a virtual machine using Proxmox VE.
* Deploy a virtual machine using VMware Workstation.
* Compare the system resources available to the virtual machines.
* Perform CPU benchmarking using Sysbench.
* Observe CPU, memory, disk, and network utilization.
* Analyze the performance characteristics of both hypervisor types.

## 3. Hypervisors Used

| Hypervisor         | Type   |
| ------------------ | ------ |
| Proxmox VE         | Type-1 |
| VMware Workstation | Type-2 |

## 4. Experimental Configuration

Both virtual machines are configured with similar resources for comparison.

| Parameter        | Configuration |
| ---------------- | ------------- |
| Operating System | Ubuntu        |
| vCPU             | 2             |
| RAM              | 2 GB          |
| Disk             | 20 GB         |
| Proxmox Network  | vmbr0         |
| VMware Network   | NAT           |

## 5. Performance Parameters

The following parameters are considered during the experiment:

* CPU information
* Memory usage
* Disk usage
* CPU benchmark performance
* CPU utilization
* Memory utilization
* Network configuration

## 6. CPU Benchmark

Sysbench is used to perform the CPU benchmark.

```bash
sysbench cpu --cpu-max-prime=20000 run
```

The following benchmark parameters are recorded:

* Total events
* Total execution time
* Events per second
* Minimum latency
* Average latency
* Maximum latency

## 7. Hypervisor-1 — Proxmox VE

Proxmox VE is used as the Type-1 hypervisor.

The screenshots and experimental results will be added after the Proxmox experiment is completed.

### Evidence

```text
Hypervisor-1/
├── screenshots/
└── result.md
```

## 8. Hypervisor-2 — VMware Workstation

VMware Workstation is used as the Type-2 hypervisor.

The actual system information, resource utilization, and Sysbench CPU benchmark results are documented in:

```text
Hypervisor-2/result.md
```

The corresponding experimental screenshots are stored in:

```text
Hypervisor-2/screenshots/
```

## 9. Comparison

After both experiments are completed, the measured values will be compared based on:
## Performance Comparison

After both experiments are completed, the measured values will be compared based on:

| Parameter | Proxmox VE | VMware Workstation |
|---|---|---|
| CPU Information | To be recorded | Recorded |
| Memory Usage | To be recorded | Recorded |
| Disk Usage | To be recorded | Recorded |
| CPU Benchmark | To be recorded | Recorded |
| Events per Second | To be recorded | 1290.89 |
| Average Latency | To be recorded | 0.77 ms |
| CPU Utilization | To be recorded | ~3% active |
| Memory Utilization | To be recorded | ~58.8% |
## 10. Result

The performance of the Type-1 hypervisor (Proxmox VE) and Type-2 hypervisor (VMware Workstation) was evaluated using system resource monitoring and CPU benchmarking.

| Parameter          | Type-1 Hypervisor - Proxmox VE | Type-2 Hypervisor - VMware Workstation |
| ------------------ | ------------------------------ | -------------------------------------- |
| CPU Information    | 2 vCPU, x86_64, GenuineIntel   | 12th Gen Intel Core i5-1235U, x86_64   |
| Memory Usage       | 1019.4 MiB / 1968.3 MiB        | 1125.5 MiB / 1915.2 MiB                |
| Disk Usage         | 7.0 GB / 20 GB (38%)           | 9.8 GB / 20 GB (53%)                   |
| CPU Benchmark      | Sysbench CPU                   | Sysbench CPU, Prime 20000              |
| Events per Second  | To be filled from Sysbench     | 1290.89                                |
| Average Latency    | To be filled from Sysbench     | 0.77 ms                                |
| CPU Utilization    | ~1.3% active                   | ~3% active                             |
| Memory Utilization | ~51.8%                         | ~58.8%                                 |

The measurements provide a comparison of CPU performance, memory usage, disk usage, CPU utilization, and memory utilization between the Type-1 and Type-2 hypervisors.
## 11. Conclusion

This experiment provides practical understanding of Type-1 and Type-2 hypervisors and demonstrates how virtualization environments can be evaluated using system resource monitoring and CPU benchmarking.


## 12. Docker — Python Web Application

A simple Python Flask web application was containerized and executed using Docker.

### Docker Components

| Component | Description |
|-----------|-------------|
| Application | Python Flask |
| Docker Image | my-python-app |
| Container | my-python-container |
| Port | 5000 |

### Docker Workflow

```text
Flask Application
       ↓
   Dockerfile
       ↓
  Docker Image
  my-python-app
       ↓
Docker Container
my-python-container
       ↓
http://localhost:5000
Result:
The Flask application was successfully containerized and run using Docker. The application was accessed through http://localhost:5000, and container operations such as logs, stop, start, and removal were successfully performed.