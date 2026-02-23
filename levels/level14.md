# 🔐 Bandit Level 14 → 15

## 🎯 Objective
##### The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

---

## 🛠️ Concepts Used
- nc
- cat

---

## 💻 Commands Used

```bash
cat /etc/bandit_pass/bandit14
nc localhost 30000
```
 ---
 ## 🔎 Explanation

As it was mentioned in the previous challenge , the password for bandit14 was stored in `/etc/bandit_pass/bandit14` , and can only be read by user bandit14. So I `cat` the file and got the password. Now `nc` was used to connet to the port 30000 in the localhost. Now when we enter the password for bandit14 in it, we got another password as output.

---

![alt text](/ss/14.png "Ths is a sample output")

`nc` is a very powerfull tool used to connect or listen to ports and create a TCP or UDP connection between two device. check out [here](https://commandlinux.com/man-page/man1/nc1/) to learn more about `nc`


