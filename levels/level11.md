# 🔐 Bandit Level 11 → 12

## 🎯 Objective
##### The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

---

## 🛠️ Concepts Used
- cat
- tr
- | (pipe)

---

## 💻 Commands Used

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
 ---
 ## 🔎 Explanation

In the challenge it was mentioned that the letters are rotated by 13 positions which means either it was rotated forward or backward. Now I tried both ways and found out it was forward i.e. **A → N** or **H → U**.

Now , to convert the text `tr`(Translate) command was used , that will swap the letters with the respective required letters.Now `'A-Za-z' 'N-ZA-Mn-za-m'` this is the format by which `tr` will translate the letters.`A → N` `Z → M` & `a → n` `z → m`.

---

In this challage I used `tr` tool for the first time, and learned that `tr` can be used not only to translate, but to delete or squeeze characters as you want.
