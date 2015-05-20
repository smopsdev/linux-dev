Linux Performance Tuning
=========================

#####1. Approach
On a very high level, following are the four subsystems that needs to be monitored.

  * CPU - four critical performance metrics for CPU — context switch, run queue, cpu utilization, and load average.
  * Memory - 
     1. Virtual memory = Swap space available on the disk + Physical memory. The virtual memory contains both user space and kernel space.
     2. Using either 32-bit or 64-bit system makes a big difference in determining how much memory a process can utilize. On a 32-bit system a process can only access a maximum of 4GB virtual memory. On a 64-bit system there is no such limitation.
    3. The unused RAM will be used as file system cache by the kernel.
    4. The Linux system will swap when it needs more memory. i.e when it needs more memory than the physical memory. When it swaps, it writes the least used memory pages from the physical memory to the swap space on the disk.
    5. Lot of swapping can cause performance issues, as the disk is much slower than the physical memory, and it takes time to swap the memory pages from RAM to disk.

  * I/O - I/O wait is the amount of time CPU is waiting for I/O. If a consistent high i/o wait is recorded in a system, it indicates a problem in the disk subsystem. The following aspects of IO should be monitored; reads/second, and writes/second. This is measured in blocks. i.e number of blocks read/write per second. These are also referred as bi and bo (block in and block out).
    tps indicates total transactions per seconds, which is sum of rtps (read transactions per second) and wtps (write transactions per seconds).

  * Network - For network interfaces, the following metrics are more relevant total number of packets (and bytes) received/sent through the interface, number of packets dropped. Also a good understanding of the TCP protocol.
  

#####2. Tuning Parameters
#####3. Metrics
#####4. Cookbook
#####5. Resources
