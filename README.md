name: Linux System Monitoring & Log Rotation Automation
description: >

  A practical Linux project that automates system health monitoring and log rotation
  using Bash scripts and Cron jobs. Designed for beginners to practice Linux scripting,
  file permissions, system monitoring, and automation — demonstrating skills relevant
  to real-world Linux and DevOps environments.

project_overview:

  system_health_script:
    name: system-health.sh
    description: >
    
      Monitors CPU, memory, disk usage, checks system uptime and active users,
      logs alerts to /var/log/syshealth-alerts.log if thresholds are exceeded,
      scheduled via cron to run every 1 minute.
  rotate_logs_script:
    name: rotate-logs.sh
    description: >
      Compresses old log files with timestamps, archives logs in /var/log/myapp/,
      scheduled via cron to run daily at midnight.

skills_demonstrated:

  - Linux commands and filesystem navigation
  - Bash scripting and automation
  - File permissions and ownership
  - Cron job scheduling
  - System monitoring and log management
  - Practical understanding of DevOps tasks

cron_jobs_setup:

  system_health: "*/1 * * * * /usr/local/bin/system-health.sh"
  rotate_logs: "0 0 * * * /usr/local/bin/rotate-logs.sh"

how_to_use:

  steps:
    - Copy scripts to the system path:
      - sudo cp system-health.sh /usr/local/bin/
      - sudo cp rotate-logs.sh /usr/local/bin/
    - Make scripts executable:
      - sudo chmod +x /usr/local/bin/system-health.sh
      - sudo chmod +x /usr/local/bin/rotate-logs.sh
    - Add the cron jobs using: crontab -e
    - Test manually:
      - sudo /usr/local/bin/system-health.sh
      - sudo /usr/local/bin/rotate-logs.sh

logs_verification:

  system_alerts: cat /var/log/syshealth-alerts.log
  archived_logs: ls -l /var/log/myapp/

author:

  name: Priyanka Dhage
  roles: Linux Beginner | DevOps Enthusiast | Automation & Scripting
