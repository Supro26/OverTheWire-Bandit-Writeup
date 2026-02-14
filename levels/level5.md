# 🔐 Bandit Level 5 → 6

## 🎯 Objective
##### The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

 - human-readable
 - 1033 bytes in size
 - not executable



---

## 🛠️ Concepts Used
- cd
- cat
- find

---

## 💻 Commands Used

```bash
cd /inhere
ls
find . -readable -size 1033c -not -executable
```
 ---
 ## 🔎 Explanation
Using `cd` to change the directory to **/inhere** 

Now the **inhere** folder contains a lot of other folders, that contains folders inside that folder. Boom, good luck finding the file manually. But I have tools, so I used `find` to search throuth all the directorys in the current directory whose porperties are as mentiond in the Question.

`-readable` mode tells that the file should be human readlabe

`-size 1033c` tells that the file size should be 1033 bytes

`-not -executable` tells that the fild should not be executable

---

![alt text](/ss/5.png "Ths is a sample output")

All the criterieas matches with the **./maybehere07/.file2** 

This level taught me how to `find` to find a specific file with some specific creiterias.



