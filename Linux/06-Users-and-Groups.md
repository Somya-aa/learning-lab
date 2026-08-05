# Users and Groups

Linux is a **multi-user operating system**, allowing multiple users to access and use the same system while maintaining security and isolation.

Each user belongs to one or more groups, which help control access to files, directories, and system resources.

---

# Types of Users

Linux has three main types of users:

| User Type | Description |
|-----------|-------------|
| Root User | Has complete control over the system. |
| Regular User | Used for everyday tasks with limited permissions. |
| System User | Created by the operating system for running services and applications. |

---

# Root User

The **root user** is the system administrator with unrestricted access to all files and commands.

Home directory:

```text
/root
```

> ⚠️ **Warning:** Use the root account carefully, as incorrect commands can affect the entire system.

---

# Current User

Display the currently logged-in user:

```bash
whoami
```

Example output:

```text
somya
```

---

# Display User Information

Show your user ID (UID), group ID (GID), and group memberships:

```bash
id
```

Example output:

```text
uid=1000(somya) gid=1000(somya) groups=1000(somya),27(sudo)
```

---

# Create a New User

Create a user account:

```bash
sudo adduser john
```

or

```bash
sudo useradd john
```

> 📌 **Note:** `adduser` is more user-friendly on most Linux distributions, while `useradd` is a lower-level command.

---

# Delete a User

Delete a user:

```bash
sudo userdel john
```

Delete a user and their home directory:

```bash
sudo userdel -r john
```

---

# Change User Password

Set or change a user's password:

```bash
sudo passwd john
```

Change your own password:

```bash
passwd
```

---

# Switch Users

Switch to another user:

```bash
su john
```

Switch to the root user:

```bash
sudo su
```

Return to the previous user:

```bash
exit
```

---

# Groups

Groups allow multiple users to share the same permissions.

Display all groups:

```bash
groups
```

Example output:

```text
somya sudo developers
```

---

# Create a Group

```bash
sudo groupadd developers
```

---

# Delete a Group

```bash
sudo groupdel developers
```

---

# Add a User to a Group

```bash
sudo usermod -aG developers john
```

- `-a` → Append the user to the group.
- `-G` → Specify the group name.

---

# Remove a User from a Group

```bash
sudo gpasswd -d john developers
```

---

# Command Summary

| Command | Purpose |
|---------|---------|
| `whoami` | Display the current user |
| `id` | Show user and group information |
| `adduser` | Create a new user |
| `userdel` | Delete a user |
| `passwd` | Change a password |
| `su` | Switch users |
| `groups` | Display group memberships |
| `groupadd` | Create a group |
| `groupdel` | Delete a group |
| `usermod -aG` | Add a user to a group |
| `gpasswd -d` | Remove a user from a group |

---

# Best Practices

- Use a regular user account for daily work.
- Use `sudo` only when administrative privileges are required.
- Assign users to appropriate groups instead of giving unnecessary permissions.
- Remove unused user accounts.
- Use strong passwords for all accounts.

---

# Common Mistakes

### Logging in as Root for Daily Tasks

Avoid using the root account for routine work.

Instead, use:

```bash
sudo <command>
```

---

### Forgetting the `-a` Option

Incorrect:

```bash
sudo usermod -G developers john
```

Correct:

```bash
sudo usermod -aG developers john
```

Without `-a`, the user may be removed from existing groups.

---

### Weak Passwords

Use strong and unique passwords to improve system security.

---

# Summary

In this chapter, you learned:

- Types of Linux users.
- The role of the root user.
- How to create and delete users.
- How to manage passwords.
- How to create and manage groups.
- Best practices for user and group management.

---

## Navigation

⬅️ Previous: [File Permissions](05-File-Permissions.md)

➡️ Next: [Package Management](07-Package-Management.md)