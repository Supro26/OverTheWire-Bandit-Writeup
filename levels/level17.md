
# 🔐 Bandit Level 17 → 18

## 🎯 Objective
##### There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new


---

## 🛠️ Concepts Used
- diff

---

## 💻 Commands Used

```bash
diff passwords.new passwords.old
```
 ---
 ## 🔎 Explanation

To get the line `diff` command was used, which compares two files line by line and display the differences.

---

![alt text](/ss/17.png "Ths is a sample output")

In this output, the first line was the line from **passeords.new** which was different from the file **passwords.old** .