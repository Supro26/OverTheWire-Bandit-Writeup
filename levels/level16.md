
# 🔐 Bandit Level 16 → 17

## 🎯 Objective
##### The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.


---

## 🛠️ Concepts Used
- nmap
- openssl

---

## 💻 Commands Used

```bash
nmap -p 31000-32000 localhost 
nmap -p [ports_found] -sV -t10
openssl s_client -connect localhost:31790
```
 ---
 ## 🔎 Explanation

In this challenge `nmap` was used to look up for open ports in the range 31000 to 32000 on localhost. Now we need to know which ports provide SSL service, but if we scan every ports in range 31000-32000 it will take a long time , So I splitted the task by first finding the open ports, then finding the service versions for those specific ports.

There were 2 ports with SSL but only one of them will provide the required output. After connecting with both the ports with `openssl`, **31790** was the port we were looking for.

Entering the password of this level , I got a 'RSA Private Key' as a return. I saved it, changed permissions and used it to enter the lext level.(similar to [level 13](/levels/level3.md)).

---



