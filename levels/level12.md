# 🔐 Bandit Level 12 → 13

## 🎯 Objective
##### The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name.

---

## 🛠️ Concepts Used
- gzip
- bzip2
- file
- tar
- mv

---

## 💻 Commands Used

```bash
file test1
mv test1 test2.gz
gzip -d test2.gz
file test2
mv test2 test3.bz2
bzip2 -d test3.bz2
.
.
.
tar -xvf test5
```
 ---
 ## 🔎 Explanation

This challange was a bit lengthy. The file was needed to be decompressed multiple times manually to get the actual value. Now I can't use a external tool in this env so I needed to create my own script to automate this task, but yk what? I was lazyy.

So I did it maually. But its not at all recomended to do manually in real word scenarios.

First I used `file` command to check the *type* of the file.( I will stop the process when I get the file type as *ASCII*).

Now , either the file will be a gzipped compressed or bzip2 compressed or a POSIX tar archive file.

For gzip file At first I used `mv` to change the extension of the file to **gz** , then used `gzip -d` to decompress it.

Similar steps are used for **bzip2** file type.

And for tar archive format, `tar -xvf` was used to read the archive file and look at the inner directory structure and restore them in the current device. To know more about tar format [click here.](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

---

![alt text](/ss/12.png "Ths is a sample output")
In this challage I learned about **hexdump** , what it does and how to deal with multi compressed files.

Im planning to build a tool which can automate this task. This will be one of my upcoming prject.  :]

---
March 26th,
And guess what, The project is live. A web-based Recursive File Decompressor [click here](https://github.com/Supro26/Decompressor) for the repo.
