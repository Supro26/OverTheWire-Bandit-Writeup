# 🔐 Bandit Level 7 → 8

## 🎯 Objective
##### The password for the next level is stored in the file data.txt next to the word millionth

---

## 🛠️ Concepts Used
- cat
- wc
- grep
- | (pipe)

---

## 💻 Commands Used

```bash
wc data.txt
cat data.txt | grep -i millionth
```
 ---
 ## 🔎 Explanation

Never `cat` A file Without using `wc` first.I Repeat, NEVER DO THAT. 

So, `wc` helps to count the number of words a file cotains. After that using `grep` I found out the line contaning '**millionth**' and thats how it doesn't print the whole text but only the line with the word '**millionth**'.

---

And just like that, I found the password for the next level.
