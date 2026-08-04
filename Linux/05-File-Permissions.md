# File Permissions

Linux uses a permission system to control who can read, write, or execute files and directories. Every file and directory has an associated owner, group, and set of permissions.

Understanding file permissions is essential for securing files and managing access in a multi-user environment.

---

# Understanding File Permissions

Display file permissions using:

```bash
ls -l
```

Example output:

```text
-rwxr-xr-- 1 somya users 2048 Aug 4 18:30 script.sh
```

Permission breakdown:

```text
-rwxr-xr--
│││ │ │
│││ │ └── Others
│││ └──── Group
│└────── Owner
└──────── File Type
```

---

# File Types

| Symbol | File Type |
|---------|-----------|
| `-` | Regular file |
| `d` | Directory |
| `l` | Symbolic link |
| `c` | Character device |
| `b` | Block device |

---

# Permission Types

| Symbol | Permission | Value |
|---------|------------|------:|
| `r` | Read | 4 |
| `w` | Write | 2 |
| `x` | Execute | 1 |
| `-` | No Permission | 0 |

---

# Permission Categories

Linux divides permissions into three categories:

| Category | Description |
|----------|-------------|
| Owner (u) | User who owns the file |
| Group (g) | Users belonging to the same group |
| Others (o) | All other users |

---

# Change Permissions

Use the `chmod` command to modify permissions.

Example:

```bash
chmod u+x script.sh
```

Add execute permission for the owner.

Remove write permission:

```bash
chmod u-w script.sh
```

Grant read permission to others:

```bash
chmod o+r script.sh
```

---

# Numeric Permission Method

Permissions can also be represented using numbers.

| Number | Permission |
|--------:|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 0 | --- |

Example:

```bash
chmod 755 script.sh
```

Meaning:

```text
Owner : rwx (7)
Group : r-x (5)
Others: r-x (5)
```

Another example:

```bash
chmod 644 notes.txt
```

Meaning:

```text
Owner : rw-
Group : r--
Others: r--
```

---

# Change File Ownership

Use the `chown` command to change the file owner.

```bash
sudo chown alice notes.txt
```

Change owner and group:

```bash
sudo chown alice:developers notes.txt
```

---

# Change Group Ownership

Use the `chgrp` command.

```bash
sudo chgrp developers notes.txt
```

---

# View File Ownership

```bash
ls -l
```

Example output:

```text
-rw-r--r-- 1 somya developers 1024 Aug 4 notes.txt
```

---

# Command Summary

| Command | Purpose |
|---------|---------|
| `ls -l` | View file permissions |
| `chmod` | Change file permissions |
| `chown` | Change file owner |
| `chgrp` | Change group ownership |

---

# Best Practices

- Follow the principle of least privilege.
- Grant execute permission only when required.
- Avoid using `777` unless absolutely necessary.
- Regularly review file permissions.
- Use `sudo` carefully when changing ownership.

---

# Common Mistakes

### Using `chmod 777`

```bash
chmod 777 file.txt
```

> ⚠️ **Warning:** This grants full permissions to everyone and can create security risks.

---

### Forgetting Execute Permission

Scripts require execute permission before they can run.

```bash
chmod +x script.sh
```

---

### Changing Ownership Without `sudo`

Changing ownership usually requires administrative privileges.

```bash
sudo chown username file.txt
```

---

# Summary

In this chapter, you learned:

- How Linux file permissions work.
- File types and permission symbols.
- Permission categories.
- Symbolic and numeric permission methods.
- How to change permissions and ownership.
- Best practices for managing file security.

---

## Navigation

⬅️ Previous: [File and Directory Management](04-File-and-Directory-Management.md)

➡️ Next: [Users and Groups](06-Users-and-Groups.md)