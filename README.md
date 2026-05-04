# learnGit

A beginner-friendly guide to learning Git.

---

## What is Git?

Git is a distributed version control system that tracks changes in source code, enables collaboration, and maintains a full history of every modification.

---

## Initial Setup

Configure your identity before your first commit:

```bash
git config --global user.name  "Your Name"
git config --global user.email "you@example.com"
```

---

## Core Concepts

| Concept       | Description                                                    |
|---------------|----------------------------------------------------------------|
| Repository    | A directory tracked by Git (contains a `.git` folder)          |
| Commit        | A snapshot of your changes saved in the history               |
| Branch        | An independent line of development                             |
| Remote        | A version of the repository hosted elsewhere (e.g., GitHub)   |
| Staging area  | Where you prepare changes before committing them              |

---

## Essential Commands

### Starting a repository

```bash
git init                  # Create a new local repository
git clone <url>           # Clone an existing remote repository
```

### Checking status and history

```bash
git status                # Show the working tree status
git log                   # Show commit history
git log --oneline         # Compact one-line-per-commit history
git diff                  # Show unstaged changes
```

### Staging and committing

```bash
git add <file>            # Stage a specific file
git add .                 # Stage all changes in the current directory
git commit -m "message"   # Commit staged changes with a message
```

### Branching and merging

```bash
git branch                # List branches
git branch <name>         # Create a new branch
git checkout <name>       # Switch to a branch
git checkout -b <name>    # Create and switch to a new branch
git merge <name>          # Merge a branch into the current branch
git branch -d <name>      # Delete a branch
```

### Working with remotes

```bash
git remote -v             # List remote connections
git remote add origin <url>   # Add a remote named "origin"
git fetch                 # Download changes without merging
git pull                  # Fetch and merge changes from the remote
git push origin <branch>  # Push local branch to the remote
```

### Undoing changes

```bash
git restore <file>        # Discard unstaged changes in a file
git reset HEAD <file>     # Unstage a file (keep changes)
git revert <commit>       # Create a new commit that undoes a previous one
```

---

## Typical Workflow

```
1. git clone <url>          – Get a copy of the repository
2. git checkout -b feature  – Create a feature branch
3. # … make changes …
4. git add .                – Stage your changes
5. git commit -m "Add …"    – Commit your changes
6. git push origin feature  – Push to the remote
7. Open a Pull Request on GitHub and request a review
8. git checkout main && git pull   – Update your local main after merge
```

---

## Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [Pro Git Book (free)](https://git-scm.com/book/en/v2)
- [GitHub Learning Lab](https://skills.github.com/)
