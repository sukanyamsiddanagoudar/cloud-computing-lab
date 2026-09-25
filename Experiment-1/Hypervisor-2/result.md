CC Experiment 1 — Type-2 Hypervisor Performance Benchmark

A benchmarking experiment that evaluates the CPU, memory, and disk characteristics of an Ubuntu virtual machine running on a Type-2 hypervisor (VMware Workstation), along with a CPU benchmark using Sysbench.

Table of Contents
System Configuration
CPU Information
Memory Information
Disk Information
CPU Benchmark — Sysbench
Resource Utilization
Result Summary
System Configuration
Component	Configuration
Hypervisor	VMware Workstation
Hypervisor Type	Type-2
Operating System	Ubuntu 24.04.5 LTS
vCPU	2
RAM	2 GB
Disk	20 GB
Network	NAT
CPU Information
Parameter	Value
CPU Model	12th Gen Intel(R) Core(TM) i5-1235U
CPU Architecture	x86_64
CPU Cores	2 (1 socket × 2 cores/socket)
CPU Threads	2 (1 thread per core)
CPU Frequency	Not captured (BogoMIPS: 4992.00)
Memory Information
Parameter	Value
Total Memory	1.9 GiB
Used Memory	1.1 GiB
Free Memory	128 MiB
Available Memory	796 MiB
Disk Information
Parameter	Value
Filesystem	/dev/sda2
Total Disk Space	20 GB
Used Space	9.8 GB
Available Space	8.8 GB
Usage	53%
CPU Benchmark - Sysbench

The CPU benchmark was performed using Sysbench.

Configuration
Prime limit: 20,000
Threads: 1
Official runs: 1
Results
Parameter	Value
Total Events	12,911
Total Time	10.0005 s
Events Per Second	1290.89
Minimum Latency	0.68 ms
Average Latency	0.77 ms
Maximum Latency	8.52 ms
Resource Utilization
Resource	Value
CPU Usage	1.7% user, 1.0% system, 97.0% idle
Memory Usage	1125.5 MiB used / 1915.2 MiB total (~58.8%)
Disk Usage	53% (root partition)
Network Usage	Not captured (NAT mode, no traffic measured)
Result Summary
Metric	Observed Value
CPU Benchmark	Sysbench prime calculation (limit 20000)
Execution Time	10.0005 s
Events Per Second	1290.89
Average Latency	0.77 ms
CPU Utilization	~3% active (97% idle) during test snapshot
Memory Utilization	~58.8% (1.1 GiB / 1.9 GiB)
Conclusion

This experiment measured the baseline system configuration, CPU, memory, and disk characteristics of an Ubuntu 24.04.5 LTS virtual machine running under a Type-2 hypervisor (VMware Workstation), along with a Sysbench CPU benchmark. The VM achieved approximately 1290.89 events per second under a single-threaded prime-number workload, with an average latency of 0.77 ms, while overall system CPU and memory utilization remained low during the test run.

Author Sukanya