# 🚀 MasteringGit

A beginner-friendly guide to understanding and mastering **Git** — a powerful version control system.

---

## Introduction

**Git** is a distributed version control system that helps developers track changes in their files and collaborate with others efficiently.  
**GitHub** is a cloud-based platform that provides a graphical interface to use Git and collaborate with others through repositories, pull requests, and more.

---

## Git Workflow Overview

```bash
Write code in files
        ↓
Add files to staging area → git add <filename> or git add .
        ↓
Commit the changes        → git commit -m "Descriptive message"
        ↓
(Optionally) Push to remote → git push origin <branch-name>
```

---

## Example Workflow

### Step 1: Create Project Folder and Initialize Git

```bash
mkdir hello-world
cd hello-world
git init
```

### Step 2: Create a File

```bash
echo Hello, World! > hello.txt
```

### Step 3: Check Status

```bash
git status
```

### Step 4: Add File to Staging Area

- Add a specific file:

```bash
git add hello.txt
```

- Add all files:

```bash
git add .
```

### Step 5: Commit the File

```bash
git commit -m "Add hello.txt with Hello World message"
```

### Step 6 (Optional): Push to GitHub

```bash
git remote add origin https://github.com/yourusername/hello-world.git
git branch -M main
git push -u origin main
```

---

## Keeping Your Local Repository in Sync

When working on a group project, it is important to keep your local repository in sync with the latest changes made by others. Here are two common ways to update your local repo with the current remote repository:

### 1. Two-step Method: Fetch and Merge

Fetch updates from the remote repository without applying them automatically:

```bash
git fetch origin
```

Then merge the changes into your current branch:

```bash
git merge origin/main
```

This approach allows you to review the changes before applying them.

---

### 2. One-step Method: Pull

You can directly fetch and merge updates with a single command:

```bash
git pull origin main
```

This is the most common and convenient way to stay up-to-date.

---

### 3. Handling Local Changes Before Updating

If you have **uncommitted changes** that conflict with remote updates, Git will prevent you from pulling. You have two options:

#### Option A: Commit Your Local Changes

```bash
git add .
git commit -m "Save my local work"
git pull origin main
```

#### Option B: Temporarily Stash Changes

```bash
git stash
git pull origin main
git stash pop
```

Using `stash` is useful when you want to update your repo but aren’t ready to commit unfinished work.

---

## 📌 Summary Table

| Task                             | Command(s)                                                 |
| -------------------------------- | ---------------------------------------------------------- |
| Initialize repo                  | `git init`                                                 |
| Check status                     | `git status`                                               |
| Add files to staging             | `git add <file>` or `git add .`                            |
| Commit changes                   | `git commit -m "message"`                                  |
| Add remote origin                | `git remote add origin <repo-url>`                         |
| Push to GitHub                   | `git push -u origin main`                                  |
| Fetch changes                    | `git fetch origin`                                         |
| Merge fetched changes            | `git merge origin/main`                                    |
| Pull updates (fetch + merge)     | `git pull origin main`                                     |
| Commit local work before pull    | `git add . && git commit -m "msg" && git pull origin main` |
| Stash changes, pull, and restore | `git stash && git pull origin main && git stash pop`       |

---
