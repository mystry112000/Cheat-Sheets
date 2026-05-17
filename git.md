# 🐙 Git Cheat Sheet

> Git saves different versions of your code so you can go back in time, try new things without breaking anything, and share your work with others.

---

## 📦 Setup

```bash
# Set your name and email (do this once)
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# Check your settings
git config --list
```

---

## 📁 Starting a Project

```bash
# Start tracking an existing folder
git init

# Download an existing project from GitHub
git clone https://github.com/user/repo.git
```

---

## 💾 Saving Changes (The Basic Workflow)

```bash
# Step 1: Check what changed
git status

# Step 2: See the actual changes in files
git diff

# Step 3: Prepare files to be saved (stage them)
git add filename.js          # Stage one file
git add .                    # Stage ALL changed files
git add *.js                 # Stage all .js files

# Step 4: Save the changes with a message
git commit -m "What I changed and why"
```

> 🔄 **Do this cycle every time you make changes:** edit → `git add` → `git commit`

---

## 🌿 Branches (Working on different things at once)

```bash
# See all branches (* = current branch)
git branch

# Create a new branch
git branch new-feature

# Switch to a branch
git checkout new-feature
# Or do both at once (create + switch)
git checkout -b new-feature

# Merge a branch into your current branch
git checkout main            # First switch to main
git merge new-feature        # Then merge new-feature into main

# Delete a branch (after merging)
git branch -d new-feature
```

---

## ☁️ GitHub (Uploading & Downloading)

```bash
# Connect your folder to a GitHub repo
git remote add origin https://github.com/your/repo.git

# Upload your code to GitHub
git push origin main

# First time push (sets upstream)
git push -u origin main

# Download latest changes from GitHub
git pull origin main
```

---

## ⏪ Undoing Things

```bash
# Unstage a file (keep changes but remove from staging)
git reset filename.js

# Discard changes in a file (go back to last saved version)
git checkout -- filename.js

# Undo the last commit (keep changes in staging)
git reset --soft HEAD~1

# Undo the last commit (discard changes completely)
git reset --hard HEAD~1
```

---

## 👀 Checking History

```bash
# See commit history
git log

# See compact history (one line per commit)
git log --oneline

# See history as a graph
git log --oneline --graph --all
```

---

## 🚨 Common Problems & Fixes

| Problem | Fix |
|---------|-----|
| Wrong message in last commit | `git commit --amend -m "New message"` |
| Forgot to add a file to last commit | `git add file.js` then `git commit --amend --no-edit` |
| Need to undo everything since last commit | `git reset --hard HEAD` |
| Already pushed but need to undo | `git revert HEAD` (safe way) |

---

## 💡 Pro Tips

- **Commit often** — small commits with clear messages are better than one big messy commit
- **Write good messages:** "Fix login bug" not "stuff" or "."
- **Branch for every new feature** — keeps main branch clean
- **Pull before you push** — avoids conflicts
- When stuck, type `git status` — it tells you what to do next
