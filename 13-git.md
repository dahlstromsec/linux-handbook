# Git

> **Estimated Reading Time:** 15–20 minutes
> **Difficulty:** Beginner–Intermediate
> **Prerequisites:** Bash

Git is a distributed version control system used to track changes in files and collaborate on projects. It allows you to save snapshots of your work, revert changes, and synchronize projects with remote repositories such as GitHub.

Learning Git is an essential skill for developers, system administrators, and cybersecurity professionals who manage scripts, documentation, and automation projects.

---

## What You'll Learn

* Creating Git repositories
* Cloning existing repositories
* Tracking file changes
* Creating commits
* Working with branches
* Synchronizing with GitHub

---

# Basic Git Workflow

Most Git projects follow the same workflow:

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
        │
        ▼
git push
        │
        ▼
GitHub Repository
```

---

# Git Commands

---

## git clone

### Purpose

Downloads an existing Git repository from a remote server.

### Syntax

```bash
git clone REPOSITORY_URL
```

### Example

```bash
git clone https://github.com/example/linux-notes.git
```

### Common Uses

* Download projects.
* Contribute to open-source repositories.
* Clone personal repositories onto another computer.

### Cybersecurity Context

Commonly used to obtain security tools, lab material, and open-source projects from GitHub.

### Related Commands

* `git pull`

---

## git init

### Purpose

Creates a new Git repository in the current directory.

### Syntax

```bash
git init
```

### Example

```bash
mkdir linux-notes

cd linux-notes

git init
```

### Common Uses

* Start a new project.
* Begin version tracking.

### Cybersecurity Context

Useful when creating repositories for scripts, notes, automation, or documentation.

### Related Commands

* `git add`

---

## git add

### Purpose

Stages changes before creating a commit.

### Syntax

```bash
git add FILE
```

### Examples

```bash
git add README.md

git add .

git add *.md
```

### Common Uses

* Stage new files.
* Stage modified files.
* Prepare commits.

### Cybersecurity Context

Allows you to carefully review and stage only the intended changes before committing.

### Related Commands

* `git commit`

---

## git commit

### Purpose

Creates a snapshot of all staged changes.

### Syntax

```bash
git commit -m "Commit message"
```

### Example

```bash
git commit -m "Add Linux networking notes"
```

### Common Uses

* Save project progress.
* Document changes.
* Create project history.

### Cybersecurity Context

Meaningful commit messages make it easier to audit changes and track modifications over time.

### Related Commands

* `git add`

---

## git push

### Purpose

Uploads local commits to a remote repository.

### Syntax

```bash
git push
```

### Example

```bash
git push origin main
```

### Common Uses

* Upload completed work.
* Backup projects.
* Share repositories.

### Cybersecurity Context

Frequently used to synchronize documentation, scripts, and projects with GitHub.

### Related Commands

* `git pull`

---

## git pull

### Purpose

Downloads and integrates changes from a remote repository.

### Syntax

```bash
git pull
```

### Example

```bash
git pull origin main
```

### Common Uses

* Update local repositories.
* Synchronize projects.

### Cybersecurity Context

Important when collaborating on repositories with multiple contributors.

### Related Commands

* `git push`

---

## git branch

### Purpose

Lists, creates, or deletes branches.

### Syntax

```bash
git branch
```

### Examples

```bash
git branch

git branch feature-notes
```

### Common Uses

* View existing branches.
* Create feature branches.

### Cybersecurity Context

Branches allow experimentation without affecting the main project.

### Related Commands

* `git switch`
* `git checkout`

---

## git checkout

### Purpose

Switches branches or restores files.

### Syntax

```bash
git checkout BRANCH
```

### Example

```bash
git checkout main
```

### Common Uses

* Switch branches.
* Restore files.
* View previous versions.

### Cybersecurity Context

Useful when reviewing historical project versions or restoring previous configurations.

### Related Commands

* `git switch`

---

## git switch

### Purpose

Switches between existing Git branches.

### Syntax

```bash
git switch BRANCH
```

### Example

```bash
git switch feature-notes
```

### Common Uses

* Change active branch.
* Continue feature development.

### Cybersecurity Context

Allows different features or documentation updates to be developed independently.

### Related Commands

* `git checkout`

---

## git merge

### Purpose

Combines changes from one branch into another.

### Syntax

```bash
git merge BRANCH
```

### Example

```bash
git merge feature-notes
```

### Common Uses

* Merge completed work.
* Integrate feature branches.

### Cybersecurity Context

Allows reviewed changes to be incorporated into the primary project while preserving development history.

### Related Commands

* `git branch`
* `git switch`

---

# Common Mistakes

| Problem                    | Cause                                    |
| -------------------------- | ---------------------------------------- |
| Nothing to commit          | Files were not staged using `git add`    |
| Repository not initialized | `git init` has not been run              |
| Push rejected              | Remote repository contains newer commits |
| Detached HEAD              | Checked out a commit instead of a branch |

---

# Summary

You should now understand the basic Git workflow, including creating repositories, tracking changes, creating commits, working with branches, and synchronizing projects with GitHub. These commands form the foundation of version control and will be used throughout your development and cybersecurity journey.

---

# Related Chapters

* Bash
* Files & Directories
* Security
* Package Management
