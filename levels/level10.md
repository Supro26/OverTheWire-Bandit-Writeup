# 🔐 Bandit Level 10 → 11

## 🎯 Objective
##### The password for the next level is stored in the file data.txt, which contains base64 encoded data.

---

## 🛠️ Concepts Used
- cat
- base64
- | (pipe)

---

## 💻 Commands Used

```bash
cat data.txt | base64 -d
```
 ---
 ## 🔎 Explanation

As the question says, the file is containig a base64 format encoded data. So I `cat` the **data.txt** file and piped it `|` with `base64 -d` to decode it in normal human readable form.

---

And thats how we got another password for the next level.
