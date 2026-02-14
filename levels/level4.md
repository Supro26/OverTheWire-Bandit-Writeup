# 🔐 Bandit Level 4 → 5

## 🎯 Objective
##### The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.


---

## 🛠️ Concepts Used
- cd
- ls
- cat
- file

---

## 💻 Commands Used

```bash
cd /inhere
ls
file ./-file00 ./-file01 ./-file02 ./-file03 ./-file04 ./-file05 ./-file06 ./-file07 ./-file08 ./-file09
```
 ---
 ## 🔎 Explanation
Using `cd` to change the directory to **/inhere** 

There were lots of files in that directory, containing binary data. so if I cat all the files one by one, it would be a mess X-X . So using `file` command was a better option. `file` tells the info about the data content of a file. if the data type is an **ASCII text** , thats our target.

---

![alt text](/ss/4.png "Ths is a sample output")

**-file07** contains the pass for the next level.I was planning to automate the file names entry, cuz if there were too many files, It won't be possible to type them manually. For that either use a tool or write a bash script, but I was lazy to type out sooo  : )



