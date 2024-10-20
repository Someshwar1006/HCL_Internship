This log file provides a detailed timeline of the tasks completed during my internship at HCL Technologies, focused on real-time Linux kernel development. The internship, spanning from May 31, 2024, to August 8, 2024, involved transforming a standard Linux kernel into a real-time (RT) kernel by applying patches, optimizing memory allocation, and improving overall system performance.

Throughout the internship, I worked extensively with C programming, Linux commands, and kernel debugging tools to enhance the kernel's stability and efficiency. To ensure the system maintained stability after each kernel modification, I ran a series of tests using the Linux Testing Project (LTP), an industry-standard tool used for system validation.

Below is a week-by-week breakdown of the tasks performed during this internship.

WEEK 1, 2 (31 May - 13 June 2024)
----------------------------------
[TASK] Basics of C programming.
       - Focused on learning syntax, control structures, and standard libraries in C.
       - Implemented basic programs for memory management, file handling, and I/O operations.
       - Gained familiarity with pointers, data structures, and dynamic memory allocation techniques.

WEEK 3 (14 June - 20 June 2024)
-------------------------------
[TASK] Creation of GitHub repository.
       - Set up a GitHub repository to track project progress and manage code.
       - Committed initial C programs and kernel documentation for version control.
       - Used Git commands such as `git init`, `git add`, `git commit`, and `git push`.

WEEK 4 (21 June - 27 June 2024)
-------------------------------
[TASK] Linux installation.
       - Installed and configured Arch Linux for kernel development.
       - Ensured compatibility with the system hardware and loaded the necessary kernel modules.
       - Configured bootloader (GRUB) to manage multiple kernel versions during the internship.
       - **LTP Stability Check:** 
         1. Ran Linux Testing Project (LTP) tests to validate the system after installation.
         2. Ensured that the installed kernel passed essential stability tests.
         3. Documented results to confirm that the system is ready for further kernel updates.

WEEK 5 (28 June - 4 July 2024)
------------------------------
[TASK] Kernel update for stability.
       - Updated the kernel to the latest stable version.
       - Compiled the updated kernel from source using `make` and `make install`.
       - Tested kernel stability by running stress tests and monitoring system logs (`dmesg`).
       - **LTP Stability Check:**
         1. Submitted the updated kernel to LTP to perform extensive stability testing.
         2. Reviewed LTP test results for potential kernel crashes or stability issues.

WEEK 6 (5 July - 11 July 2024)
------------------------------
[TASK] Applied PREEMPT_RT patch for real-time capabilities.
       - Downloaded and applied the PREEMPT_RT patch to enable real-time performance.
       - Configured the kernel with `make menuconfig` to enable real-time preemption.
       - Compiled and installed the patched kernel, then rebooted to verify real-time performance.
       - **LTP Stability Check:**
         1. Ran LTP tests to ensure that the PREEMPT_RT-patched kernel maintained system stability.
         2. Confirmed that the real-time performance tests passed with no critical errors.

WEEK 7 (12 July - 18 July 2024)
-------------------------------
[TASK] Journaling, write-back, and write-through techniques.
       - Explored filesystem journaling for data integrity, focusing on performance impact.
       - **Disabling Journaling:**
         1. Opened `/etc/fstab` with root privileges (`sudo nano /etc/fstab`).
         2. Located the entry for the relevant partition.
         3. Removed the `data=journal` option to disable journaling.
         4. Saved the changes and rebooted the system for them to take effect.
       - **Disabling Write-Back Cache:**
         1. Edited the `sysctl.conf` file with root privileges (`sudo nano /etc/sysctl.conf`).
         2. Added `vm.dirty_background_ratio = 0` to disable write-back caching.
         3. Saved the file and applied changes using `sudo sysctl -p`.
       - **Disabling Write-Through Cache:**
         1. Edited `sysctl.conf` with root privileges.
         2. Added `fs.file-max = 1024` to disable write-through caching.
         3. Saved the file and applied changes using `sudo sysctl -p`.
       - **LTP Stability Check:**
         1. Submitted the modified filesystem and cache configuration to LTP for stability checks.
         2. Verified that no data integrity or performance issues arose from disabling journaling or caching.

WEEK 8 (19 July - 25 July 2024)
-------------------------------
[TASK] Kernel debugging.
       - Enabled kernel debugging features during kernel configuration (`make menuconfig`).
       - Used `gdb` and `kgdb` to debug kernel crashes and memory allocation errors.
       - Debugged issues in kernel modules, identified performance bottlenecks, and applied fixes.
       - **LTP Stability Check:**
         1. Conducted LTP tests post-debugging to validate kernel stability.
         2. Ensured that fixes resolved the crashes and no new errors were introduced.

WEEK 9 (26 July - 1 August 2024)
-------------------------------
[TASK] Dynamic memory allocation.
       - Implemented and tested memory allocation strategies (slab allocator, buddy system).
       - Modified kernel code to optimize memory usage for real-time operations.
       - Verified correct usage of memory pools, caches, and efficient memory freeing.
       - **LTP Stability Check:**
         1. Submitted the kernel with memory allocation changes to LTP for testing.
         2. Validated that dynamic memory allocation strategies did not cause memory leaks or kernel crashes.

WEEK 10 (2 August - 8 August 2024)
----------------------------------
[TASK] Final review.
       - Reviewed all kernel modifications, including the applied real-time patches and optimizations.
       - Conducted stress tests, performance evaluations, and ensured kernel stability.
       - **LTP Final Stability Check:**
         1. Performed a final round of LTP testing to ensure overall system stability.
         2. Generated and reviewed test reports to confirm the kernel is stable and ready for deployment.
       - Prepared the final project report, documented all findings, and submitted it for evaluation.
