# Git Best Practices

Writing good code is important, but using Git effectively is equally important. Following best practices helps keep repositories organized, improves collaboration, and makes projects easier to maintain.

---

# Write Meaningful Commit Messages

A commit message should clearly describe the purpose of the changes.

Good examples:

```text
Add user authentication
Fix navigation bar alignment
Update project documentation
```

Avoid vague messages like:

```text
Update
Fix
Changes
Done
```

---

# Commit Small, Logical Changes

Each commit should represent a single logical change.

Instead of combining multiple unrelated changes into one commit, separate them into smaller commits.

Benefits include:

- Easier debugging
- Clear project history
- Simpler code reviews

---

# Use Branches for New Work

Create a new branch for every feature, bug fix, or experiment instead of working directly on the `main` branch.

Example:

```bash
git switch -c feature-login
```

---

# Pull Before You Push

Before pushing your changes, make sure your local repository is up to date.

```bash
git pull origin main
```

This helps reduce merge conflicts.

---

# Review Changes Before Committing

Always check what has changed before creating a commit.

```bash
git status
git diff
```

Reviewing changes helps catch mistakes early.

---

# Ignore Unnecessary Files

Do not commit generated files, temporary files, or sensitive information.

Use a `.gitignore` file to exclude files such as:

```text
__pycache__/
node_modules/
.env
.vscode/
```

---

# Never Commit Sensitive Information

Avoid committing:

- Passwords
- API keys
- Access tokens
- Private certificates

Store sensitive information in environment variables or secure secret management tools.

---

# Keep the Main Branch Stable

The `main` branch should always contain stable and working code.

Test your changes before merging them into `main`.

---

# Sync with the Remote Repository

Regularly fetch or pull changes from the remote repository.

```bash
git fetch
git pull
```

Keeping your repository synchronized reduces conflicts and keeps you up to date.

---

# Delete Merged Branches

Once a branch has been successfully merged, delete it to keep your repository organized.

Delete a local branch:

```bash
git branch -d feature-login
```

Delete a remote branch:

```bash
git push origin --delete feature-login
```

---

# Best Practices Checklist

- Write meaningful commit messages.
- Make small and focused commits.
- Use feature branches.
- Pull before pushing.
- Review changes before committing.
- Use `.gitignore`.
- Never commit sensitive information.
- Keep the `main` branch stable.
- Stay synchronized with the remote repository.
- Delete merged branches.

---

# Summary

In this chapter, you learned how to:

- Organize your Git workflow.
- Write better commit messages.
- Keep repositories clean.
- Collaborate more effectively.
- Follow industry-standard Git practices.

---

# Congratulations 🎉

You have completed the Git section of the **Learning Lab** repository.

You now understand:

- Git fundamentals
- Installation and configuration
- Repository basics
- Branching
- Merging
- Remote repositories
- GitHub workflow
- Common Git commands
- Git best practices

The next section will cover **Linux**, where you'll learn essential terminal commands, file management, permissions, shell scripting, and more.