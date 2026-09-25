Hypervisor-1 — Proxmox VE (KVM/QEMU)

1\. System Configuration

Parameter	Value

Hypervisor	Proxmox VE 8.3.0 (KVM/QEMU)

Hypervisor Type	Type-1 (Bare-metal)

Host Node	admin1-HP-Pro-Tower-280-G9-E-PCI-Desktop-PC

Guest VM	VM 108 — "project1"

Operating System	Ubuntu 24.04.3 LTS

Kernel	Linux 6.14.0-27-generic

vCPU	2

RAM	\~2 GB (1968.3 MiB total)

Disk	20 GB

Network	Not captured in screenshots

Machine Type	Standard PC (i440FX + PIIX, 1996)

Firmware	SeaBIOS rel-1.16.3-0-ga6ed6b701f0a-prebuilt.qemu.org

2\. CPU Information

Parameter	Value

CPU Model	QEMU Virtual CPU version 2.5+

CPU Vendor	GenuineIntel

CPU Architecture	x86\_64

CPU Cores	2 (1 socket × 2 cores/socket)

CPU Threads	2 (1 thread/core)

CPU Frequency	Not shown in captured output (BogoMIPS: 4224.00)

Caches	L1d: 64 KiB (2), L1i: 64 KiB (2), L2: 8 MiB (2), L3: 16 MiB (1)

Virtualization	KVM (full)

3\. Memory Information



(from top, project1 VM)



Parameter	Value

Total Memory	1968.3 MiB (\~1.9 GiB)

Used Memory	1019.4 MiB

Free Memory	495.1 MiB

Buffer/Cache	652.5 MiB

Available Memory	948.8 MiB

Swap Total	2048.0 MiB

Swap Used	0.8 MiB

4\. Disk Information



(from df -h)



Parameter	Value

Filesystem	/dev/sda2

Total Disk Space	20 GB

Used Space	7.0 GB

Available Space	12 GB

Usage	38%

5\. CPU Benchmark — Sysbench

Parameter	Value

Benchmark	Sysbench CPU

Status	Not available — installation failed

Reason	apt install sysbench failed with repository authentication errors (Clearsigned file isn't valid, got 'NOSPLIT') and E: Unable to locate package sysbench

Result	No benchmark data captured for this hypervisor



Note: The repository signing error typically indicates a host clock/time-sync issue in the guest VM. Re-running sudo apt update after fixing the system clock (e.g. sudo timedatectl set-ntp true) and retrying the install is recommended to capture sysbench results.



6\. Resource Utilization



(from top)



Resource	Value

CPU Usage	0.8% user, 0.5% system, 98.5% idle, 0.2% wait

Memory Usage	1019.4 MiB used / 1968.3 MiB total (\~51.8%)

Disk Usage	38% (root partition, from df -h)

Network Usage	Not captured in screenshots

7\. Result Summary

Metric	Observed Value

CPU Benchmark	Not available (sysbench installation failed — repository authentication error)

Execution Time	N/A

Events Per Second	N/A

Average Latency	N/A

CPU Utilization	\~1.3% active, 98.5% idle (snapshot)

Memory Utilization	\~51.8% (1019.4 MiB / 1968.3 MiB)

Disk Utilization	38% (7.0 GB / 20 GB)

8\. Screenshots



The experimental output screenshots are available in the screenshots folder:



12-task\_manager.png — Proxmox VE dashboard, VM 108 (project1) task history

13-ubantu\_screen.png — Guest console, hostnamectl command entry

14-hostman.png — hostnamectl output (OS, kernel, hardware model)

15-cpuanalysis.png — lscpu output (part 1)

16-cpu.png — Supplementary VM (CC-Experiment1-Type1) free -h output

17-diskAnalysis.png — lscpu vulnerabilities section + df -h output

18-cpu\_and\_memory.png — top output (CPU/memory utilization)

19-memory\_and\_space.png — Supplementary VM (CC-Experiment1-Type1) free -h output

20-sysbench.png — Failed sysbench installation attemptAdditional note



Screenshots 16-cpu.png and 19-memory\_and\_space.png are from a different guest VM, captured with free -h:



Parameter	Value

Total Memory	1.9 GiB

Used Memory	764 MiB

Free Memory	128 MiB

Shared Memory	86 MiB

Buffer/Cache	1.0 GiB

Available Memory	964 MiB

Swap	0B (total/used/free)



These are included for completeness but are not part of the primary "project1" (VM 108) measurements used in Sections 1–7 above.

