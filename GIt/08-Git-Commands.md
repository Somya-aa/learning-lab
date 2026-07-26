# Git Commands

Git provides a variety of commands to help you manage repositories, track changes, collaborate with others, and maintain project history.

This chapter serves as a quick reference for the most commonly used Git commands.

---

# Repository Commands

| Command | Description |
|---------|-------------|
| `git init` | Initialize a new Git repository. |
| `git clone <url>` | Clone an existing repository. |
| `git status` | Show the current repository status. |

---

# Configuration Commands

| Command | Description |
|---------|-------------|
| `git config --global user.name "Your Name"` | Set your Git username. |
| `git config --global user.email "you@example.com"` | Set your Git email. |
| `git config --list` | Display all Git configurations. |

---

# Staging Commands

| Command | Description |
|---------|-------------|
| `git add <file>` | Stage a specific file. |
| `git add .` | Stage all modified and new files. |
| `git restore --staged <file>` | Remove a file from the staging area. |

---

# Commit Commands

| Command | Description |
|---------|-------------|
| `git commit -m "message"` | Create a new commit with a message. |
| `git commit --amend` | Modify the most recent commit. |
| `git log` | View commit history. |
| `git log --oneline` | View a condensed commit history. |

---

# Branch Commands

| Command | Description |
|---------|-------------|
| `git branch` | List local branches. |
| `git branch <name>` | Create a new branch. |
| `git switch <branch>` | Switch to another branch. |
| `git switch -c <branch>` | Create and switch to a new branch. |
| `git branch -d <branch>` | Delete a merged branch. |

---

# Merge Commands

| Command | Description |
|---------|-------------|
| `git merge <branch>` | Merge a branch into the current branch. |

---

# Remote Repository Commands

| Command | Description |
|---------|-------------|
| `git remote -v` | View configured remote repositories. |
| `git remote add origin <url>` | Add a remote repository. |
| `git push origin <branch>` | Push commits to a remote repository. |
| `git pull origin <branch>` | Pull and merge changes from a remote repository. |
| `git fetch` | Download changes without merging them. |

---

# Undo Commands

| Command | Description |
|---------|-------------|
| `git restore <file>` | Discard changes in a file. |
| `git restore --staged <file>` | Unstage a file. |
| `git reset HEAD~1` | Undo the last commit while keeping changes locally. |

---

# Useful Commands

| Command | Description |
|---------|-------------|
| `git diff` | Show changes between versions. |
| `git show` | Display details of a specific commit. |
| `git stash` | Temporarily save uncommitted changes. |
| `git stash pop` | Restore the most recently stashed changes. |
| `git tag` | List all tags. |

---

# Best Practices

- Use meaningful commit messages.
- Check `git status` before committing.
- Pull the latest changes before pushing.
- Keep commits focused on a single task.
- Use branches for new features and bug fixes.

---

# Summary

In this chapter, you learned:

- Repository commands.
- Configuration commands.
- Staging commands.
- Commit commands.
- Branch commands.
- Merge commands.
- Remote repository commands.
- Useful Git commands.

---

## Next Chapter

➡️ **09 – Best Practices**