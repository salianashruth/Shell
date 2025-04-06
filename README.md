Prerequisites
This script is intended to be run on AWS Linux-based system.

Functions
1. top_apps: Display the Top 10 Applications by CPU Usage
This function fetches the top 10 processes sorted by CPU usage. It uses the top command and formats the output
to display the application name, process ID (PID), CPU usage, memory usage, and other relevant details.

display_memory: Display Memory and Swap Usage
This function shows the system's memory usage (total, used, free) and the swap usage (total, used). 
It uses the free command to gather this information and prints the results in a user-friendly format

display_disk: Display Disk Utilization
This function provides disk usage statistics for all mounted filesystems using the df -h command. 
It shows the filesystem, total size, used space, available space, usage percentage, and the mount point.

System_Load: Display System Load Averages
This function displays the system's load averages over the last 1, 5, and 15 minutes. It uses the uptime command to gather this information.

Copy the script into a file,=, Shell.sh
Make the script executable +x shell.sh
