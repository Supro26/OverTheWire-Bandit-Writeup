# 🔐 Bandit Level 6 → 7

## 🎯 Objective
##### The password for the next level is stored somewhere on the server and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

---

## 🛠️ Concepts Used
- cat
- find

---

## 💻 Commands Used

```bash
ls
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```
 ---
 ## 🔎 Explanation

Exactly like the previous level I used `find` with some conditions to find out the file location.

But There was an issue, The output was really big as there were lots of directorys that the user dont have acces of. So it was printing a lot of errors in there. To filter then I found out there is a trick. I can redirect all the error calls in a garbage bin using `2>/dev/null`

---

![alt text](/ss/6.png "Ths is a sample output")

that `2` represents stderr which is redirected to the location `/dev/null`

This redirecting errors to filter the output is a new skill that I learned from this level. 
