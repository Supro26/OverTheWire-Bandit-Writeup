# 🔐 Bandit Level 0 → 1

## 🎯 Objective
##### The goal of this level is for you to log into the game using SSH. The hostname, username, password and port are all provided in the question
##### Q. The password for the next level is stored in a file called `readme` located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

---

## 🛠️ Concepts Used
- ssh
- ls
- cat

---

## 💻 Commands Used

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
```
 ---
 ## 🔎 Explanation
At first I used `ssh bandit0@bandit.labs.overthewire.org -p 2220` to securely connect to the bandit0 server using the password **bandit0**.

Then the `ls` command is used to list all present files (One readme file was found )

And used `cat` command to print the content of `readme` in the terminal.

---

Bravo we got the pass for the next level. Too easy right? Dont worry, the more we solve tougher it will get.