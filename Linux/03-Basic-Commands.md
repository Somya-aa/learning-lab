# Basic Commands

Linux provides a powerful Command Line Interface (CLI) that allows users to interact with the operating system efficiently. Learning basic commands is essential for navigating the file system and managing files and directories.

---

# Display the Current Directory

The `pwd` (Print Working Directory) command displays the full path of your current directory.

```bash
pwd
```

Example output:

```text
/home/somya/Documents
```

---

# List Files and Directories

The `ls` command lists the contents of a directory.

```bash
ls
```

Example output:

```text
Documents  Downloads  Pictures  Videos
```

---

# List Detailed Information

```bash
ls -l
```

Displays:

- File permissions
- Owner
- File size
- Last modified date

---

# Show Hidden Files

```bash
ls -a
```

Example output:

```text
.  ..  .bashrc  Documents  Downloads
```

Hidden files begin with a (`.`).

---

# Change Directory

Use the `cd` command to move between directories.

```bash
cd Documents
```

Go to the home directory:

```bash
cd ~
```

Go to the parent directory:

```bash
cd ..
```

Go to the root directory:

```bash
cd /
```

---

# Clear the Terminal

```bash
clear
```

Shortcut:

```text
Ctrl + L
```

---

# Display Command History

```bash
history
```

Example output:

```text
1  pwd
2  ls
3  cd Documents
4  mkdir projects
```

---

# Display Calendar

```bash
cal
```

Display a specific year:

```bash
cal 2026
```

---

# Display Date and Time

```bash
date
```

Example output:

```text
Mon Aug 3 18:30:25 IST 2026
```

---

# Display Logged-in User

```bash
whoami
```

Example output:

```text
somya
```

---

# Display System Information

```bash
uname
```

Display detailed information:

```bash
uname -a
```

---

# Display Linux Distribution Information

```bash
cat /etc/os-release
```

---

# Command Summary

| Command | Purpose |
|---------|---------|
| `pwd` | Display current directory |
| `ls` | List directory contents |
| `ls -l` | Detailed directory listing |
| `ls -a` | Show hidden files |
| `cd` | Change directory |
| `clear` | Clear terminal screen |
| `history` | Show command history |
| `cal` | Display calendar |
| `date` | Show current date and time |
| `whoami` | Display current username |
| `uname` | Display system information |

---

# Best Practices

- Use `pwd` whenever you're unsure of your current location.
- Prefer `ls -l` when you need detailed file information.
- Learn keyboard shortcuts like `Ctrl + L` to improve productivity.
- Use `history` to review previously executed commands.

---

# Common Mistakes

### Running Commands in the Wrong Directory

Always verify your current directory before making changes.

```bash
pwd
```

---

### Forgetting Hidden Files

Remember that `ls` does not display hidden files.

Use:

```bash
ls -a
```

---

### Confusing `cd /` and `cd ~`

- `cd /` takes you to the root directory.
- `cd ~` takes you to your home directory.

---

# Summary

In this chapter, you learned:

- How to navigate directories.
- How to list files and folders.
- How to display system information.
- How to view command history.
- Some of the most frequently used Linux commands.

---

## Navigation

⬅️ Previous: [Linux File System](02-Linux-File-System.md)

➡️ Next: [File and Directory Management](04-File-and-Directory-Management.md)