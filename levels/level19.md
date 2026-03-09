# 🔐 Bandit Level 19 → 20

## 🎯 Objective
##### The password for the next level is stored in a file in the home directory. Use the setuid binary in the home directory to get the password for bandit20.

---

## 🛠️ Concepts Used
- setuid binaries
- file permissions
- executing binaries with elevated privileges

---

## 💻 Commands Used

```bash
ls -la
./bandit20-do
./bandit20-do cat /etc/bandit_pass/bandit20
```
 ---
 ## 🔎 Explanation

In this level, there's a setuid binary called `bandit20-do` in the home directory. Setuid binaries are special executables that run with the privileges of the file owner (in this case, bandit20) rather than the current user.

First, we list the files to see what we're working with. Then we run `./bandit20-do` without arguments to see how it works - it typically shows usage information.

The key insight is that this binary allows us to execute commands as the user bandit20. We can use it to read the password file directly:
```
./bandit20-do cat /etc/bandit_pass/bandit20
```

This executes `cat /etc/bandit_pass/bandit20` with bandit20's privileges, giving us access to the next password.

---

![alt text](/ss/19.png "Screenshot placeholder")
