# Hypervisor-1 - Proxmox VE (KVM/QEMU)

## 1. System Configuration

| Parameter        | Value                                                |
| ---------------- | ---------------------------------------------------- |
| Hypervisor       | Proxmox VE 8.3.0 (KVM/QEMU)                          |
| Hypervisor Type  | Type-1 (Bare-metal)                                  |
| Host Node        | admin1-HP-Pro-Tower-280-G9-E-PCI-Desktop-PC          |
| Operating System | Ubuntu 24.04.3 LTS                                   |
| Kernel           | Linux 6.14.0-27-generic                              |
| vCPU             | 2                                                    |
| RAM              | ~2 GB (1968.3 MiB total)                             |
| Disk             | 20 GB                                                |
| Network          | Not captured in screenshots                          |
| Machine Type     | Standard PC (i440FX + PIIX, 1996)                    |
| Firmware         | SeaBIOS rel-1.16.3-0-ga6ed6b701f0a-prebuilt.qemu.org |

## 2. CPU Information

| Parameter        | Value                                                           |
| ---------------- | --------------------------------------------------------------- |
| CPU Model        | QEMU Virtual CPU version 2.5+                                   |
| CPU Vendor       | GenuineIntel                                                    |
| CPU Architecture | x86_64                                                          |
| CPU Cores        | 2 (1 socket x 2 cores/socket)                                   |
| CPU Threads      | 2 (1 thread/core)                                               |
| CPU Frequency    | Not shown in captured output (BogoMIPS: 4224.00)                |
| Caches           | L1d: 64 KiB (2), L1i: 64 KiB (2), L2: 8 MiB (2), L3: 16 MiB (1) |
| Virtualization   | KVM (full)                                                      |

## 3. Memory Information

| Parameter        | Value                 |
| ---------------- | --------------------- |
| Total Memory     | 1968.3 MiB (~1.9 GiB) |
| Used Memory      | 1019.4 MiB            |
| Free Memory      | 495.1 MiB             |
| Buffer/Cache     | 652.5 MiB             |
| Available Memory | 948.8 MiB             |
| Swap Total       | 2048.0 MiB            |
| Swap Used        | 0.8 MiB               |

## 4. Disk Information

| Parameter        | Value       |
| ---------------- | ----------- |
| Filesystem       | `/dev/sda2` |
| Total Disk Space | 20 GB       |
| Used Space       | 7.0 GB      |
| Available Space  | 12 GB       |
| Usage            | 38%         |

## 5. CPU Benchmark - Sysbench

| Parameter      | Value                                |
| -------------- | ------------------------------------ |
| Benchmark      | Sysbench CPU                         |
| Benchmark Tool | Sysbench                             |
| Measurement    | CPU performance                      |
| Result         | Recorded from the Sysbench execution |

## 6. Resource Utilization

| Resource        | Value                                         |
| --------------- | --------------------------------------------- |
| CPU Usage       | 0.8% user, 0.5% system, 98.5% idle, 0.2% wait |
| CPU Utilization | ~1.3% active                                  |
| Memory Usage    | 1019.4 MiB used / 1968.3 MiB total (~51.8%)   |
| Disk Usage      | 38% (root partition, from `df -h`)            |
| Network Usage   | Not captured in screenshots                   |

## 7. Result Summary

| Metric             | Observed Value           |
| ------------------ | ------------------------ |
| CPU Utilization    | ~1.3% active, 98.5% idle |
| Memory Utilization | ~51.8%                   |
| Disk Utilization   | 38% (7.0 GB / 20 GB)     |
| CPU Benchmark      | Sysbench CPU             |

## 8. Screenshots

The experimental output screenshots are available in the `screenshots` folder.

## 9. Performance Comparison

The performance of the Type-1 hypervisor (Proxmox VE) and Type-2 hypervisor (VMware Workstation) was evaluated using system resource monitoring and CPU benchmarking.

| Parameter          | Type-1 Hypervisor - Proxmox VE | Type-2 Hypervisor - VMware Workstation |
| ------------------ | ------------------------------ | -------------------------------------- |
| CPU Information    | 2 vCPU, x86_64, GenuineIntel   | 12th Gen Intel Core i5-1235U, x86_64   |
| Memory Usage       | 1019.4 MiB / 1968.3 MiB        | 1125.5 MiB / 1915.2 MiB                |
| Disk Usage         | 7.0 GB / 20 GB (38%)           | 9.8 GB / 20 GB (53%)                   |
| CPU Benchmark      | Sysbench CPU                   | Sysbench CPU, Prime 20000              |
| Events per Second  | To be recorded                 | 1290.89                                |
| Average Latency    | To be recorded                 | 0.77 ms                                |
| CPU Utilization    | ~1.3% active                   | ~3% active                             |
| Memory Utilization | ~51.8%                         | ~58.8%                                 |

The measurements provide a comparison of CPU performance, memory usage, disk usage, CPU utilization, and memory utilization between the Type-1 and Type-2 hypervisors.

## 10. Result

The Type-1 hypervisor experiment was performed using Proxmox VE 8.3.0 with KVM/QEMU. System configuration, CPU information, memory usage, disk usage, and resource utilization were measured during the experiment.

The collected measurements were compared with the corresponding Type-2 hypervisor measurements to evaluate the virtualization environments using system resource monitoring and CPU benchmarking.

## 11. Conclusion

This experiment provides practical understanding of Type-1 and Type-2 hypervisors and demonstrates how virtualization environments can be evaluated using system resource monitoring and CPU benchmarking.
