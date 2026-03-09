# 🔐 Bandit Level 22 → 23

## 🎯 Objective
##### Similar to the previous level, a program is running automatically at regular intervals from cron. Look in /etc/cron.d/ for the configuration and see what command is being executed. This time, the password for the next level is in the script itself!

---

## 🛠️ Concepts Used
- cron jobs
- /etc/cron.d/
- md5sum
- string processing

---

## 💻 Commands Used

```bash
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
cat /tmp/<md5-hash>
```
 ---
 ## 🔎 Explanation

This level is similar to the previous one - we need to examine cron jobs. Let's start by looking at the cron configuration:

```
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit23
```

Now let's examine the script that's being run:
```
cat /usr/bin/cronjob_bandit23.sh
```

This script is more interesting than the previous one! It takes the username (bandit23), passes it through md5sum, and uses that hash to construct a filename in /tmp/.

The key is to figure out what filename the script will generate:
1. Get the md5 hash of the string "I am user bandit23":
   ```
   echo I am user bandit23 | md5sum | cut -d ' ' -f 1
   ```
2. Use that hash to read the password file:
   ```
   cat /tmp/<the-hash>
   ```

This demonstrates how cron jobs can expose sensitive data if they store passwords in predictable locations.

---

![alt text](/ss/22.png "Screenshot placeholder")
