Prerequisites
This script is intended to be run on AWS Linux-based system.

Functions
1. top_apps: Display the Top 10 Applications by CPU Usage
This function fetches the top 10 processes sorted by CPU usage. It uses the top command and formats the output
to display the application name, process ID (PID), CPU usage, memory usage, and other relevant details.

2. display_memory: Display Memory and Swap Usage
This function shows the system's memory usage (total, used, free) and the swap usage (total, used). 
It uses the free command to gather this information and prints the results in a user-friendly format

3. display_disk: Display Disk Utilization
This function provides disk usage statistics for all mounted filesystems using the df -h command. 
It shows the filesystem, total size, used space, available space, usage percentage, and the mount point.

4. System_Load: Display System Load Averages
This function displays the system's load averages over the last 1, 5, and 15 minutes. It uses the uptime command to gather this information.

Copy the script into a file,=, Shell.sh

Make the script executable +x shell.sh

Output
[ec2-user@ip-172-31-41-246 ~]$ ./shell.sh
Top 10 Application by CPU usage:
--------------------------------
PID      USER     %CPU     %MEM     TIME+    COMMAND
1        root     0.0      1.8      0:00.99  systemd
2        root     0.0      0.0      0:00.00  kthreadd
3        root     0.0      0.0      0:00.00  rcu_gp
4        root     0.0      0.0      0:00.00  rcu_par_gp
5        root     0.0      0.0      0:00.00  slub_flushwq
6        root     0.0      0.0      0:00.00  netns
8        root     0.0      0.0      0:00.00  kworker/0:0H-events_highpri
10       root     0.0      0.0      0:00.00  mm_percpu_wq
11       root     0.0      0.0      0:00.00  rcu_tasks_kthread
12       root     0.0      0.0      0:00.00  rcu_tasks_rude_kthread

Memory Usage:
  Total Memory:  949Mi
  Used Memory:   126Mi
  Free Memory:   616Mi
  Memory Usage:  13%

Swap Usage:
  Total Swap:    0B
  Used Swap:     0B
  
Disk Utilization
==================
Filesystem           Size       Used       Avail      Use%       Mounted
devtmpfs             4.0M       0          4.0M       0%         /dev
tmpfs                475M       0          475M       0%         /dev/shm
tmpfs                190M       452K       190M       1%         /run
/dev/xvda1           8.0G       1.6G       6.4G       20%        /
tmpfs                475M       0          475M       0%         /tmp
/dev/xvda128         10M        1.3M       8.7M       13%        /boot/efi
tmpfs                95M        0          95M        0%         /run/user/1000

System Load
--------------------
Load Average : 0.00,      0.00,      0.00

