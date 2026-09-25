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

| Parameter          | Proxmox VE     | VMware Workstation |
| ------------------ | -------------- | ------------------ |
| CPU Information    | To be recorded | Recorded           |
| Memory Usage       | To be recorded | Recorded           |
| Disk Usage         | To be recorded | Recorded           |
| CPU Benchmark      | To be recorded | Recorded           |
| Events per Second  | To be recorded | 1290.89            |
| Average Latency    | To be recorded | 0.77 ms            |
| CPU Utilization    | To be recorded | ~3% active         |
| Memory Utilization | To be recorded | ~58.8%             |

## 10. Result

The performance comparison will be completed after collecting the corresponding measurements from both Type-1 and Type-2 hypervisors.

## 11. Conclusion

This experiment provides practical understanding of Type-1 and Type-2 hypervisors and demonstrates how virtualization environments can be evaluated using system resource monitoring and CPU benchmarking.
