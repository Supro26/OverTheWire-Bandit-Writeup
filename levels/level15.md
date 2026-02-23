# 🔐 Bandit Level 15 → 16

## 🎯 Objective
##### The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

###### Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.


---

## 🛠️ Concepts Used
- openssl

---

## 💻 Commands Used

```bash
openssl s_client -connect localhost:30001
```
 ---
 ## 🔎 Explanation

`openssl` is used to connet to port **30001** on localhost using a ssl encrypted connection.

And after that we entered the password of the current level and got the next password as return.

---



