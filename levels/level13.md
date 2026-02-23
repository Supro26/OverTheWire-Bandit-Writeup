# 🔐 Bandit Level 13 → 14

## 🎯 Objective
##### The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.

---

## 🛠️ Concepts Used
- ssh
- chmod
- cat

---

## 💻 Commands Used

```bash
cat sshkey.private
exit
chmod 600 key.private
ssh bandit14@bandits.labs.overthewire.org -p 2220 -i key.private
```
 ---
 ## 🔎 Explanation

In the home directory there is a **sshkey.private** file that holds the ssh key for the next level. So I simply copied the content in the clipboard and pasted in my local device. 

Now when I tried to use it, I got a warning saying "UNPROTECTED PRIVATE KEY FILE !". And then I realized that iI need to change the permissions for the file as its a sensitive file should not be accessed by everyone. So `chmod 600 key.private` was used to change the permission to only read and write access to the owner.

Then the problem was solved and I was in the bandit14.

---

It was this level when I got to know that you can ssh into without using password and instaed using a **private ssh key** . And what error it might show if the private key file is not assigned with proper permissions.


