
# Linux Lab 1

This repository contains the solutions for Lab 1 of the Linux Basics course.

## 📚 Contents

- `lab1.md`: Step-by-step answers to Linux terminal and system usage tasks.
- Covers:
  - File and directory manipulation
  - Shell navigation
  - `vi` editor usage
  - Manual pages and command help

---

## ✅ Lab 1 - Solutions

### 1. Install Ubuntu [Dual-boot, VM, Multipass]  
Ubuntu was installed on a virtual machine using Hyper-V.

---

### 2. Difference between `cat` and `more` command  
- `cat` shows the file content all at once.  
- `more` shows the file content in parts (page-by-page).

---

### 3. Difference between `rm` and `rmdir` (using `man`)  
- `rmdir` removes empty directories.  
- `rm` removes files and directories (with `-r` for recursive).

---

### 4. Directory Hierarchy Tasks  

**a. Remove `dir11` in one step. What did you notice? How did you overcome it?**  
- `rmdir` didn’t work because `dir11` wasn’t empty.  
- Used `rm -r dir11` to remove it recursively.

**b. Remove `dir12` using `rmdir -p`. What happened?**  
- It removed `dir12` and its parent directories if they were empty.

**c. Absolute and relative path for file `mycv` (assuming output of `pwd` is `/home/user`)**  
- Absolute path: `/home/user/mycv`  
- Relative path: `./mycv`

---

### 5. Copy `/etc/passwd` to your home directory with the name `mypasswd`  
```bash
cp /etc/passwd mypasswd
```

---

### 6. Rename the file to `oldpasswd`  
```bash
mv mypasswd oldpasswd
```

---

### 7. Four ways to go to your home directory from `/usr/bin`  
- `cd ~`  
- `cd /home`  
- `cd`  
- `cd $HOME`

---

### 8. List Linux commands in `/usr/bin` that start with "w"  
```bash
ls /usr/bin | grep '^w'
```

---

### 9. Display the first 4 lines of `/etc/passwd`  
```bash
head -n 4 /etc/passwd
```

---

### 10. Display the last 7 lines of `/etc/passwd`  
```bash
tail -n 7 /etc/passwd
```

---

### 11. Display the man pages of the `passwd` command and file sequentially  
⚠️ Original command was incorrect. Use:  
```bash
man passwd
```

---

### 12. Display the man page of the `passwd` command (not the file)  
```bash
man passwd
```

---

### 13. List all commands that mention "passwd" in their man page  
```bash
man -k passwd
```

---

### 14. Write your CV using `vi` in a file called `mycv`  
```bash
sudo vi mycv
```
- Press `i` to enter insert mode  
- Write your content (name, age, school, college, experience, etc.)  
- Press `Esc`, then type `:wq` to save and quit

---

### 15. Edit `mycv` file using `vi`

- **Move down one line:** `j`  
- **Move up one line:** `k`  
- **Search for word "age":** `/age`  
- **Jump to line 5:** `5G`  
- **Delete current and line 5:** `dd` (on each line)  
- **Go to end of line and enter insert mode:** `A`

---

### 16. List available shells in your system  
```bash
cat /etc/shells
```

---

## 🛠️ Tools Used

- Ubuntu (via VM on Hyper-V)
- Terminal / Bash shell
- vi editor

---

## 📎 Author

- Name: *Your Name Here*
- Course: Linux Basics
- Date: April 2025
