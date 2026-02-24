
# 🔐 Bandit Level 18 → 19

## 🎯 Objective
##### The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.


---

## 🛠️ Concepts Used
- ssh

---

## 💻 Commands Used

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```
 ---
 ## 🔎 Explanation

As the question says, `.bashrc` file was modified so that whenever someone try to log in with SSH it will log them out instantly. 

Now, the task is easy, we need to `cat` the file **readme** in the home directory.But I can't get access to their shell.

So a better choice is to use a Remote Command Execution via SSH. We give the command we want to execute along with the ssh command i.e. `cat readme`. What it does is that, It connects → executes the command → prints output → disconnects.

---

![alt text](/ss/18.png "Ths is a sample output")

And theres our password.