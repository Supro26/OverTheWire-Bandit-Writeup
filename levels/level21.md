# 🔐 Bandit Level 21 → 22

## 🎯 Objective
##### A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

---

## 🛠️ Concepts Used
- cron jobs
- /etc/cron.d/
- shell scripts
- file reading

---

## 💻 Commands Used

```bash
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
 ---
 ## 🔎 Explanation

Cron is a time-based job scheduler in Unix-like systems. Jobs are defined in cron tables (cron.d). This level requires us to examine what scheduled jobs are running.

First, let's look at what's in /etc/cron.d/:
```
ls /etc/cron.d/
```

We find a cronjob for bandit22. Let's examine it:
```
cat /etc/cron.d/cronjob_bandit22
```

This shows us there's a script being run: `/usr/bin/cronjob_bandit22.sh`. Let's read that:
```
cat /usr/bin/cronjob_bandit22.sh
```

This script writes a password to a file in /tmp/. The filename is randomly generated (t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv in this case).

Simply read that file to get the next password:
```
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
----

![alt text](/ss/21.png "Screenshot placeholder")

It was the firt time I heard about cron in this level, and how it works. I can tell that I learned a lot in this whole Bandit War.