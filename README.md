# MasteringGit

> A beginner-friendly guide to understanding and mastering Git — a powerful version control system.

---

## 📘 Introduction

**Git** is a distributed version control system that helps developers track changes in their files and collaborate with others efficiently.  
**GitHub** is a cloud-based platform that provides a graphical interface to use Git and collaborate with others through repositories, pull requests, and more.

---

## 🔁 Git Workflow Overview

```bash
Write code in files
        ↓
Add files to staging area → `git add <filename>` or `git add .`
        ↓
Commit the changes        → `git commit -m "Descriptive message"`
        ↓
(Optionally) Push to remote → `git push origin <branch-name>`

```

---

## Example

# Step 1: Create project folder and initialize Git

```bash
mkdir hello-world
cd hello-world
git init
```

# Step 2: Create a file

```bash
echo Hello, World! > hello.txt
```

# Step 3: Check status

```bash
git status
```

# Step 4: Add file to staging area

```bash
git add hello.txt
```

# Step 5: Commit the file

```bash
git commit -m "Add hello.txt with Hello World message"
```

# Step 6 (Optional): Push to GitHub

```bash
git remote add origin https://github.com/yourusername/hello-world.git
git branch -M main
git push -u origin main
```
