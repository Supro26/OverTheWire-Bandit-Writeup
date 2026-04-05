# 🔐 Bandit Level 20 → 21

## 🎯 Objective
##### There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

---

## 🛠️ Concepts Used
- netcat (nc)
- localhost connections
- client-server communication

---

## 💻 Commands Used

```bash
ls -la
./suconnect
nc -l -p 12345 -q 1 < /etc/bandit_pass/bandit20
# In another terminal:
./suconnect 12345
```
 ---
 ## 🔎 Explanation

This level requires a two-step process. The `suconnect` binary acts as a client - it connects to a specified port on localhost, reads a password, and if correct, returns the next password.

We need to:
1. Set up a netcat listener (server) that will provide the password when the client connects
2. Run the suconnect binary to connect to our listener

First, create a netcat listener on any available port (e.g., 12345):
```
nc -l -p 12345 -q 1 < /etc/bandit_pass/bandit20
```

This listens on port 12345 and sends the content of bandit20's password when a connection is made.

Then, in another terminal (or backgrounded), run:
```
./suconnect 12345
```

The suconnect binary connects to localhost:12345, receives the password we sent, validates it, and then outputs the password for the next level.

---

![alt text](/ss/20.png "Screenshot placeholder")
