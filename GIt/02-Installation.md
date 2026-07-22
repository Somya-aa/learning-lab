# Git Installation

Before you can start tracking changes and managing repositories, Git must be installed on your system.

Git is available for **Windows**, **Linux**, and **macOS**.

---

# System Requirements

Git is lightweight and supports most modern operating systems.

- Windows 10 or later
- Linux (Ubuntu, Fedora, Arch, Debian, etc.)
- macOS 10.13 or later

---

# Installing Git on Windows

1. Visit the official Git website:

   https://git-scm.com/downloads

2. Download the latest version for Windows.

3. Run the installer.

4. During installation, the default options are suitable for most users.

5. Complete the installation.

---

# Installing Git on Linux

### Ubuntu / Debian

```bash
sudo apt update
sudo apt install git
```

### Fedora

```bash
sudo dnf install git
```

### Arch Linux

```bash
sudo pacman -S git
```

---

# Installing Git on macOS

If you have Homebrew installed:

```bash
brew install git
```

Or install Xcode Command Line Tools:

```bash
xcode-select --install
```

---

# Verify the Installation

After installation, open your terminal (or Git Bash on Windows) and run:

```bash
git --version
```

Example output:

```text
git version 2.50.1
```

If a version number appears, Git has been installed successfully.

---

# Configure Git

Before making your first commit, configure your identity.

Set your username:

```bash
git config --global user.name "Your Name"
```

Set your email:

```bash
git config --global user.email "you@example.com"
```

These details are attached to every commit you create.

---

# Check Your Configuration

To display your current Git configuration:

```bash
git config --list
```

Example output:

```text
user.name=John Doe
user.email=john@example.com
```

---

# Default Branch Name (Optional)

To make Git use `main` as the default branch for new repositories:

```bash
git config --global init.defaultBranch main
```

---

# Where Does Git Store Its Configuration?

Git stores configuration in three levels:

| Level | Scope |
|--------|-------|
| System | Applies to all users on the computer |
| Global | Applies only to your user account |
| Local | Applies only to the current repository |

You can view the configuration for each level:

```bash
git config --system --list
git config --global --list
git config --local --list
```

---

# Useful Commands

| Command | Purpose |
|---------|---------|
| `git --version` | Check the installed Git version |
| `git config --global user.name` | Set your username |
| `git config --global user.email` | Set your email |
| `git config --list` | View Git configuration |

---

# Common Issues

### `'git' is not recognized as an internal or external command`

Git is either not installed or not added to your system's PATH.

---

### Incorrect username or email

Update your configuration using:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

# Best Practices

- Download Git only from the official website.
- Configure your username and email before creating repositories.
- Verify the installation after setup.
- Keep Git updated to access the latest features and security fixes.

---

# Summary

In this chapter, you learned:

- How to install Git on Windows, Linux, and macOS.
- How to verify the installation.
- How to configure your username and email.
- How to view your Git configuration.
- The different configuration levels in Git.

Now your system is ready to create and manage Git repositories.

---