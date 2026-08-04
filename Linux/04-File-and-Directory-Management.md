# File and Directory Management

Linux provides a variety of commands to create, copy, move, rename, and delete files and directories. Understanding these commands is essential for managing the Linux file system efficiently.

---

# Create a Directory

Use the `mkdir` command to create a new directory.

```bash
mkdir projects
```

Create multiple directories at once:

```bash
mkdir project1 project2 project3
```

Create nested directories:

```bash
mkdir -p development/python/project
```

---

# Create a File

Use the `touch` command to create an empty file.

```bash
touch notes.txt
```

Create multiple files:

```bash
touch file1.txt file2.txt file3.txt
```

---

# Copy Files

Use the `cp` command to copy files.

```bash
cp notes.txt backup.txt
```

Copy a file to another directory:

```bash
cp notes.txt Documents/
```

---

# Copy Directories

To copy an entire directory, use the `-r` (recursive) option.

```bash
cp -r project backup-project
```

---

# Move or Rename Files

Use the `mv` command to move or rename files.

Rename a file:

```bash
mv notes.txt linux-notes.txt
```

Move a file:

```bash
mv linux-notes.txt Documents/
```

---

# Rename a Directory

```bash
mv old-folder new-folder
```

---

# Delete Files

Use the `rm` command to remove files.

```bash
rm notes.txt
```

Delete multiple files:

```bash
rm file1.txt file2.txt
```

---

# Delete Directories

Delete an empty directory:

```bash
rmdir empty-folder
```

Delete a directory and all its contents:

```bash
rm -r project
```

Force delete without confirmation:

```bash
rm -rf project
```

> ⚠️ **Warning:** The `rm -rf` command permanently deletes files and directories. Use it carefully, as deleted data cannot be recovered easily.

---

# View File Contents

Display the contents of a file:

```bash
cat notes.txt
```

View a file page by page:

```bash
less notes.txt
```

Display the first 10 lines:

```bash
head notes.txt
```

Display the last 10 lines:

```bash
tail notes.txt
```

---

# Count File Information

Use the `wc` command to count lines, words, and characters.

```bash
wc notes.txt
```

Example output:

```text
15 120 850 notes.txt
```

---

# Search for Files

Use the `find` command to locate files.

```bash
find . -name "notes.txt"
```

Search for directories:

```bash
find . -type d -name "project"
```

---

# Command Summary

| Command | Purpose |
|---------|---------|
| `mkdir` | Create directories |
| `touch` | Create empty files |
| `cp` | Copy files |
| `cp -r` | Copy directories |
| `mv` | Move or rename files/directories |
| `rm` | Delete files |
| `rm -r` | Delete directories |
| `rmdir` | Delete empty directories |
| `cat` | Display file contents |
| `less` | View large files |
| `head` | Display the beginning of a file |
| `tail` | Display the end of a file |
| `wc` | Count lines, words, and characters |
| `find` | Search for files and directories |

---

# Best Practices

- Verify the file or directory before deleting it.
- Use descriptive file and folder names.
- Prefer `cp` instead of `mv` when you need a backup.
- Use `rm -rf` only when absolutely necessary.
- Organize related files into dedicated directories.

---

# Common Mistakes

### Using `rm -rf` Without Verification

Always check the directory before deleting it.

```bash
pwd
ls
```

---

### Forgetting the `-r` Option

Directories cannot be copied without the recursive option.

```bash
cp -r project backup-project
```

---

### Renaming the Wrong File

Verify the file name before using the `mv` command.

```bash
ls
```

---

# Summary

In this chapter, you learned:

- How to create files and directories.
- How to copy, move, and rename files.
- How to delete files and directories.
- How to view file contents.
- How to search for files.
- Best practices for managing files in Linux.

---

## Navigation

⬅️ Previous: [Basic Commands](03-Basic-Commands.md)

➡️ Next: [File Permissions](05-File-Permissions.md)