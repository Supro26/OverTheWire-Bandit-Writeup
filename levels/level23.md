# 🔐 Bandit Level 23 → 24

## 🎯 Objective
##### A program is running automatically at regular intervals from cron. This level requires you to create your own first shell script. The program is in /var/spool/bandit24/ (note: location may vary - check the cron script).

---

## 🛠️ Concepts Used
- shell scripting
- cron jobs
- creating and executing scripts
- file permissions

---

## 💻 Commands Used

```bash
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
mkdir -p /tmp/your_directory
cat > /tmp/your_directory/script.sh << 'EOF'
#!/bin/bash
cp /etc/bandit_pass/bandit24 /tmp/your_directory/password
EOF
chmod +x /tmp/your_directory/script.sh
cp /tmp/your_directory/script.sh /var/spool/bandit24/
# Wait for cron to execute, then:
cat /tmp/your_directory/password
```
 ---
 ## 🔎 Explanation

This level requires us to create our own shell script that will be executed by cron. Let's first examine what the cron job is doing:

```
ls /etc/cron.d/
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh
```

The script runs every minute and executes any script in the bandit24 spool directory. It looks for scripts owned by the current user (bandit23), runs them, and then deletes them.

To solve this:
1. Create a temporary directory to store our output
2. Write a shell script that copies the password to our directory
3. Copy the script to the spool directory
4. Wait for cron to execute it (up to 60 seconds)
5. Read the password from our output directory

The script should look like:
```bash
#!/bin/bash
cp /etc/bandit_pass/bandit24 /tmp/your_directory/password
```

This demonstrates the basics of shell scripting and how cron jobs work - important skills for both system administration and security.

---

![alt text](/ss/23.png "Screenshot placeholder")
