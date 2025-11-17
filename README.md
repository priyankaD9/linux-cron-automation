# Linux Cron Job Automation Project

A hands-on Linux project demonstrating **system monitoring** and **log rotation automation** using Bash scripts and Cron jobs.  
Ideal for beginners to showcase scripting, automation, and Linux/DevOps skills.

---

## Project Overview

This project contains two scripts:

### 1. `system-health.sh`
- Monitors **CPU, memory, and disk usage**  
- Checks **system uptime** and **active users**  
- Logs alerts to `/var/log/syshealth-alerts.log` if thresholds are exceeded  
- Scheduled via cron to run **every 1 minute**

### 2. `rotate-logs.sh`
- Compresses old log files with **timestamps**  
- Archives logs in `/var/log/myapp/`  
- Scheduled via cron to run **daily at midnight**

---

## Skills Demonstrated

- Linux commands and filesystem navigation  
- Bash scripting and automation  
- File permissions and ownership  
- Cron job scheduling  
- System monitoring and log management

---

## Cron Jobs Setup

```bash
# Run system-health.sh every 1 minute
*/1 * * * * /usr/local/bin/system-health.sh

# Run rotate-logs.sh daily at midnight
0 0 * * * /usr/local/bin/rotate-logs.sh
