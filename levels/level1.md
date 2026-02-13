# 🔐 Bandit Level 1 → 2

## 🎯 Objective
##### The password for the next level is stored in a file called `-` located in the home directory

---

## 🛠️ Concepts Used
- ssh
- ls
- cat

---

## 💻 Commands Used

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
cat ./-
```
 ---
 ## 🔎 Explanation
Used `ssh` in `bandit1` this time
And the `cat` command is again used to display the content of the file `-` .

---

![alt text](/ss/1.png "Ths is a sample image")

The main challange was to `cat` the `-` file, naturally we decalre [mode] for any command using the dash `-` keyword. So only using `cat -` creates confussion.

So I went to search for a solution and found out that, using `cat ./-[filename]` can slove this issue of ambiguity.