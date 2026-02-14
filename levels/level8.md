# 🔐 Bandit Level 8 → 9

## 🎯 Objective
##### The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

---

## 🛠️ Concepts Used
- cat
- grep
- | (pipe)
- sort
- uniq

---

## 💻 Commands Used

```bash
wc data.txt
cat data.txt | sort | uniq -c | sort -n | grep -w "1" millionth
```
 ---
 ## 🔎 Explanation

Now this challange was fun. I had to find out the only line that occured once.

First I used `sort` to sort the lines by there total character size, so that every repeating lines come together

Then piping `|` it to `uniq -c` which removes all the duplicate lines and adds a count in front of each unique line

Again piping `|` it to `sort -n` which sorts the output in respect to the numner(count) [this one was unnecessary as I did a `grep` later on]

And again piping `|` it to `grep -w "1"` so that it onlu returns the line with '**1**' as an exact keyword.

---
![alt text](/ss/8.png "Ths is a sample output")

And just like that, I found the password for the next level.
