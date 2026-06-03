# 🚀 Git CLI Master Course

<p align="center">
  <img src="https://img.shields.io/badge/Git-CLI-orange?style=for-the-badge&logo=git">
  <img src="https://img.shields.io/badge/Beginner-Friendly-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Interview-Preparation-blue?style=for-the-badge">
</p>

<h3 align="center">
Learn Git Commands with Simple Explanations, Examples, Outputs, and Visual Workflows
</h3>

---

# 📖 About This Repository

This repository is created for students, beginners, developers, and interview preparation.

Every command is explained using:

* ✅ Simple Definition
* ✅ Syntax
* ✅ Real Examples
* ✅ Sample Output
* ✅ Visual Representation
* ✅ Internal Working
* ✅ Common Mistakes
* ✅ Interview Questions

The goal is to understand Git practically instead of memorizing commands.

---

# 🎯 Course Goal

After completing this repository, you will be able to:

* Create Git repositories
* Configure Git
* Track files
* Stage changes
* Create commits
* View history
* Compare changes
* Undo mistakes safely
* Understand Git workflow clearly

---

# 🧠 What is Git?

Git is a Distributed Version Control System (DVCS).

It helps developers:

* Track source code changes
* Maintain project history
* Collaborate with teams
* Restore previous versions
* Manage software development efficiently

Created by:

**Linus Torvalds (2005)**

---

# ⚙️ Git Workflow

```text
Working Directory
        │
        ▼
    git add
        │
        ▼
   Staging Area
        │
        ▼
   git commit
        │
        ▼
 Local Repository
```

---

# 📂 Repository Structure

```text
Git-CLI-Master/

│
├── README.md
│
├── git-version.txt
├── git-config.txt
├── git-init.txt
├── git-clone.txt
│
├── git-status.txt
├── git-add.txt
├── git-commit.txt
├── git-log.txt
├── git-diff.txt
│
├── git-restore.txt
├── git-reset.txt
└── git-revert.txt
```

---

# 📚 Learning Path

```text
1. git-version
        ↓
2. git-config
        ↓
3. git-init
        ↓
4. git-clone
        ↓
5. git-status
        ↓
6. git-add
        ↓
7. git-commit
        ↓
8. git-log
        ↓
9. git-diff
        ↓
10. git-restore
        ↓
11. git-reset
        ↓
12. git-revert
```

Follow this order for the best learning experience.

---

# 🛠 Setup Commands

## git-version

Check whether Git is installed and display the current Git version.

```bash
git --version
```

Example Output:

```text
git version 2.50.1
```

---

## git-config

Configure username and email for commits.

```bash
git config --global user.name "Rohith"
git config --global user.email "rohith@example.com"
```

Verify Configuration:

```bash
git config --list
```

---

# 📦 Repository Commands

## git-init

Create a new Git repository.

```bash
git init
```

Output:

```text
Initialized empty Git repository
```

Creates a hidden `.git` folder.

---

## git-clone

Download an existing repository.

```bash
git clone repository-url
```

Example:

```bash
git clone https://github.com/user/project.git
```

Output:

```text
Cloning into 'project'...
```

---

# 🔥 Daily Workflow Commands

## git-status

Check repository status.

```bash
git status
```

Shows:

* Untracked files
* Modified files
* Staged files

---

## git-add

Move files to staging area.

```bash
git add file.txt
```

or

```bash
git add .
```

Visual:

```text
Modified File
      │
      ▼
  git add
      │
      ▼
 Staging Area
```

---

## git-commit

Create a snapshot of staged changes.

```bash
git commit -m "Initial Commit"
```

Output:

```text
[main abc123]
Initial Commit
```

Visual:

```text
Commit 1
    │
Commit 2
    │
Commit 3
```

---

## git-log

View commit history.

```bash
git log
```

Compact Version:

```bash
git log --oneline
```

Example:

```text
abc123 Initial Commit
def456 Added Login
ghi789 Bug Fixed
```

---

## git-diff

Compare file changes.

```bash
git diff
```

Shows:

```text
- Old Code
+ New Code
```

Useful before committing.

---

# 🔄 Undo Commands

## git-restore

Discard file changes.

```bash
git restore file.txt
```

Visual:

```text
Modified File
      │
git restore
      │
      ▼
Last Saved Version
```

---

## git-reset

Move HEAD and undo commits.

Soft Reset:

```bash
git reset --soft HEAD~1
```

Mixed Reset:

```bash
git reset HEAD~1
```

Hard Reset:

```bash
git reset --hard HEAD~1
```

Visual:

```text
Commit1
   │
Commit2
   │
Commit3
   ▲
 HEAD

Reset

Commit1
   │
Commit2
   ▲
 HEAD
```

---

## git-revert

Safely undo a commit.

```bash
git revert HEAD
```

Creates a new commit that reverses previous changes.

Visual:

```text
Commit1
   │
Commit2
   │
Commit3
   │
Revert Commit
```

History remains intact.

---

# 📊 Git File States

```text
Untracked
    │
git add
    ▼
Staged
    │
git commit
    ▼
Committed
```

---

# 🚀 Most Important Commands

```bash
git --version

git config --list

git init

git clone <url>

git status

git add .

git commit -m "message"

git log

git log --oneline

git diff

git restore file.txt

git reset --soft HEAD~1

git reset --hard HEAD~1

git revert HEAD
```

---

# 💡 Common Beginner Mistakes

### Mistake 1

```bash
git commit
```

Without staging files first.

Correct:

```bash
git add .
git commit -m "message"
```

---

### Mistake 2

Using:

```bash
git reset --hard
```

without understanding consequences.

This permanently removes changes.

---

### Mistake 3

Forgetting commit messages.

Bad:

```bash
git commit -m "update"
```

Good:

```bash
git commit -m "Added User Authentication Module"
```

---

# 🎓 Interview Questions

### What is Git?

A distributed version control system used to track changes in source code.

---

### What is a Repository?

A project folder managed by Git.

---

### What is the Staging Area?

A temporary area where changes are prepared before committing.

---

### Difference Between git reset and git revert?

| git reset              | git revert                 |
| ---------------------- | -------------------------- |
| Removes commit history | Creates new reverse commit |
| Can rewrite history    | Preserves history          |
| Risky                  | Safe                       |

---

### What is a Commit?

A snapshot of project changes at a particular point in time.

---

### What is HEAD?

HEAD points to the current commit.

---

### What is git diff?

Displays differences between file versions.

---

# 🏆 Final Outcome

After finishing this repository you will understand:

```text
Create Repository
        ↓
Track Files
        ↓
Stage Changes
        ↓
Create Commits
        ↓
View History
        ↓
Compare Changes
        ↓
Undo Mistakes
```

You will have a strong foundation in Git and be ready for real-world development projects and technical interviews.

---

# ⭐ Support

If this repository helps you learn Git, consider giving it a Star.

Happy Coding 🚀

# SIUUUUUUUUUUUUUUUUUU ⚽🔥
