# 🚀 Complete Git Guide

![Git](https://img.shields.io/badge/Git-VersionControl-F05032?logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Platform-Linux-black?logo=linux)
![Status](https://img.shields.io/badge/Guide-ProductionReady-brightgreen)

---

## 📌 What is Git?

Git is a distributed version control system used to:
- Track code changes
- Collaborate with teams
- Manage branches
- Maintain history
- Deploy safely

---

# 🔧 1️⃣ Initial Setup

## Install Git (Linux)

```bash
sudo apt update
sudo apt install git
```

## Configure Identity

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Check configuration:

```bash
git config --list
```

---

# 📂 2️⃣ Create New Repository

```bash
mkdir project-name
cd project-name
git init
```

---

# 📊 3️⃣ Basic Workflow

## Check Status
```bash
git status
```

## Add Files
```bash
git add file.php
git add .
```

## Commit Changes
```bash
git commit -m "Initial commit"
```

## View History
```bash
git log --oneline
```

---

# 🌍 4️⃣ Connect to GitHub

## Add Remote Repository
```bash
git remote add origin https://github.com/username/repository.git
```

## Verify Remote
```bash
git remote -v
```

## Push Code
```bash
git branch -M main
git push -u origin main
```

After first push:
```bash
git push
```

---

# 🔁 5️⃣ Clone Repository

## HTTPS
```bash
git clone https://github.com/username/repository.git
```

## SSH (Recommended)
```bash
git clone git@github.com:username/repository.git
```

---

# 🔄 6️⃣ Pull Latest Changes

```bash
git pull origin main
```

---

# 🌿 7️⃣ Branching

## Create New Branch
```bash
git checkout -b feature-name
```

## Switch Branch
```bash
git checkout main
```

## View Branches
```bash
git branch
```

## Merge Branch
```bash
git checkout main
git merge feature-name
```

---

# ⚠️ 8️⃣ Undo Mistakes

## Unstage File
```bash
git reset file.php
```

## Undo Last Commit (Keep Changes)
```bash
git reset --soft HEAD~1
```

## Undo Last Commit (Delete Changes)
```bash
git reset --hard HEAD~1
```

---

# 📁 9️⃣ .gitignore Example

Create `.gitignore` file:

```
node_modules/
.env
vendor/
dist/
```

---

# 🧪 1️⃣0️⃣ Check Differences

```bash
git diff
```

---

# 📦 1️⃣1️⃣ Stash Changes

```bash
git stash
git stash pop
```

---

# 🗑 1️⃣2️⃣ Remove Remote

```bash
git remote remove origin
```

---

# 🏢 Production Safe Workflow

```bash
git pull origin main
git checkout -b feature-login
git add .
git commit -m "Add login feature"
git push origin feature-login
```

Create Pull Request → Merge → Deploy.

---

# 🔥 Most Used Commands Cheat Sheet

```bash
git status
git add .
git commit -m "message"
git push
git pull
git checkout -b branch-name
git merge branch-name
git log --oneline
```

---

# 🧠 Best Practices

✔ Always pull before push  
✔ Use meaningful commit messages  
✔ Never commit `.env` files  
✔ Use branches for new features  
✔ Use SSH authentication  
✔ Review code before merging  

---

🚀 Maintained by: Your Name  
