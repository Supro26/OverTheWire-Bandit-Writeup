# 🔐 Bandit Level 2 → 3

## 🎯 Objective
##### The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory

---

## 🛠️ Concepts Used
- ls
- cat

---

## 💻 Commands Used

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat ./"--spaces in this filename--"
```
 ---
 ## 🔎 Explanation
Used `cat` and then `" "` to solve the problem of spaces, as otherwise each words will be treated as different commands.

---

And thats how we got the pass for the next level.