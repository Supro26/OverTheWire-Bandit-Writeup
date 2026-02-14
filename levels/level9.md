# 🔐 Bandit Level 9 → 10

## 🎯 Objective
##### The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

---

## 🛠️ Concepts Used
- strings
- grep
- | (pipe)

---

## 💻 Commands Used

```bash
file data.txt
strings data.txt | grep -E '={2,}'
```
 ---
 ## 🔎 Explanation

Using `file` I got to know its a binary file. So the `strings` command is then used to show only the humal readable strings out of a binary file.

Now as the question says that the password is preceded with several "=" cahracters. So its better to use `grep` to filter out only the lines with more than one "**=**" char 


---
![alt text](/ss/9.png "Ths is a sample output")

Weww we got another password for the next level.
