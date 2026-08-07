# Package Management

Package management is the process of installing, updating, removing, and managing software on a Linux system.

Instead of downloading applications from websites, Linux uses **package managers** to handle software installation along with its required dependencies.

---

# What is a Package Manager?

A **package manager** is a tool that automates:

- Installing software
- Updating software
- Removing software
- Managing software dependencies
- Searching for available packages

Package managers help keep the operating system organized and secure.

---

# Common Package Managers

| Package Manager | Linux Distribution |
|-----------------|--------------------|
| `apt` | Ubuntu, Debian |
| `dnf` | Fedora |
| `yum` | CentOS, RHEL (Older Versions) |
| `pacman` | Arch Linux |
| `zypper` | openSUSE |

---

# Update Package Information

Before installing new software, update the package list.

Ubuntu/Debian:

```bash
sudo apt update
```

Fedora:

```bash
sudo dnf check-update
```

Arch Linux:

```bash
sudo pacman -Sy
```

---

# Upgrade Installed Packages

Upgrade all installed software.

Ubuntu/Debian:

```bash
sudo apt upgrade
```

Fedora:

```bash
sudo dnf upgrade
```

Arch Linux:

```bash
sudo pacman -Syu
```

---

# Install a Package

Ubuntu/Debian:

```bash
sudo apt install git
```

Fedora:

```bash
sudo dnf install git
```

Arch Linux:

```bash
sudo pacman -S git
```

---

# Remove a Package

Ubuntu/Debian:

```bash
sudo apt remove git
```

Fedora:

```bash
sudo dnf remove git
```

Arch Linux:

```bash
sudo pacman -R git
```

---

# Search for a Package

Ubuntu/Debian:

```bash
apt search git
```

Fedora:

```bash
dnf search git
```

Arch Linux:

```bash
pacman -Ss git
```

---

# Display Installed Packages

Ubuntu/Debian:

```bash
apt list --installed
```

Fedora:

```bash
dnf list installed
```

Arch Linux:

```bash
pacman -Q
```

---

# Remove Unused Dependencies

Ubuntu/Debian:

```bash
sudo apt autoremove
```

Fedora:

```bash
sudo dnf autoremove
```

---

# Clean Package Cache

Ubuntu/Debian:

```bash
sudo apt clean
```

Fedora:

```bash
sudo dnf clean all
```

Arch Linux:

```bash
sudo pacman -Sc
```

---

# Command Summary

| Command | Purpose |
|---------|---------|
| `apt update` | Update package list |
| `apt upgrade` | Upgrade installed packages |
| `apt install` | Install a package |
| `apt remove` | Remove a package |
| `apt search` | Search for a package |
| `apt list --installed` | List installed packages |
| `apt autoremove` | Remove unused dependencies |
| `apt clean` | Clear package cache |

---

# Best Practices

- Always update the package list before installing software.
- Install software from official repositories whenever possible.
- Remove unused packages regularly.
- Keep your system updated for security and stability.
- Read package descriptions before installing unfamiliar software.

---

# Common Mistakes

### Installing Packages Without Updating

Always update the package list first.

```bash
sudo apt update
```

---

### Removing Important System Packages

Review packages before removing them.

```bash
apt show <package-name>
```

---

### Forgetting to Upgrade the System

Regular updates help improve performance and security.

```bash
sudo apt upgrade
```

---

# Summary

In this chapter, you learned:

- What a package manager is.
- Common Linux package managers.
- How to install, update, search, and remove packages.
- How to clean package caches.
- Best practices for package management.

---

## Navigation

⬅️ Previous: [Users and Groups](06-Users-and-Groups.md)

➡️ Next: [Shell and Bash](08-Shell-and-Bash.md)