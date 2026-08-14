# Linux Best Practices

Linux provides many powerful commands and tools. Following good practices makes the system safer, easier to manage, and easier to troubleshoot.

---

# Use the Correct Permissions

Give users only the permissions they actually need.

Check permissions:

```bash
ls -l
```

Change permissions when necessary:

```bash
chmod 644 file.txt
```

Avoid unnecessary full permissions:

```bash
chmod 777 file.txt
```

`777` gives read, write, and execute permissions to everyone and should generally be avoided.

---

# Be Careful with sudo

`sudo` gives commands administrative privileges.

Example:

```bash
sudo apt update
```

Use `sudo` only when it is actually required.

Avoid running unknown commands with `sudo`, especially commands copied from untrusted sources.

---

# Keep the System Updated

Regular updates help keep the system secure and provide bug fixes.

Ubuntu/Debian:

```bash
sudo apt update
sudo apt upgrade
```

Keeping packages updated helps improve system security and stability.

---

# Understand Commands Before Running Them

Before executing an unfamiliar command, understand what it does.

For example:

```bash
rm file.txt
```

deletes a file.

Be especially careful with commands that can delete many files:

```bash
rm -rf directory
```

Always check the path before executing destructive commands.

---

# Use Absolute and Relative Paths Carefully

An absolute path starts from the root directory:

```text
/home/user/Documents/file.txt
```

A relative path starts from the current directory:

```text
Documents/file.txt
```

Check your current location:

```bash
pwd
```

---

# Use Meaningful File and Directory Names

Good names make projects easier to understand.

Example:

```text
project/
├── src/
├── docs/
├── scripts/
└── README.md
```

Avoid confusing names such as:

```text
folder1/
test2/
abc/
```

when working on larger projects.

---

# Keep Your Home Directory Organized

Avoid storing everything directly inside your home directory.

A better structure is:

```text
Home/
├── Documents/
├── Downloads/
├── Projects/
├── Scripts/
└── Learning/
```

This makes files easier to find and manage.

---

# Use Command History

View command history:

```bash
history
```

Search through history:

```bash
history | grep git
```

You can also use:

```text
Ctrl + R
```

to search previous commands interactively.

---

# Use Manual Pages

Linux provides documentation for many commands through `man`.

Example:

```bash
man ls
```

Other examples:

```bash
man chmod
man grep
man find
```

To leave the manual page, press:

```text
q
```

---

# Use --help

Many commands provide a quick help option.

Example:

```bash
ls --help
```

Other examples:

```bash
cp --help
grep --help
chmod --help
```

---

# Use Tab Completion

The `Tab` key can automatically complete commands, file names, and directories.

For example:

```bash
cd Doc
```

Press `Tab` and Bash may complete it to:

```bash
cd Documents/
```

Tab completion reduces typing and prevents spelling mistakes.

---

# Use Pipes Effectively

Pipes allow the output of one command to become the input of another.

Example:

```bash
ls | grep ".txt"
```

Another example:

```bash
ps aux | grep python
```

Pipes are one of the most powerful features of the Linux command line.

---

# Use Redirection Carefully

Write output to a file:

```bash
ls > files.txt
```

Append output:

```bash
date >> log.txt
```

Redirect errors:

```bash
command 2> error.txt
```

Redirect both output and errors:

```bash
command > output.txt 2>&1
```

Be careful with `>` because it can overwrite existing file contents.

---

# Backup Important Data

Important files should not exist in only one location.

Useful backup options include:

- External storage
- Cloud storage
- Another system
- Git repositories for source code

For example:

```bash
git add .
git commit -m "Backup project changes"
```

Regular backups can help prevent data loss.

---

# Use Git for Projects

For programming projects, Git provides version control.

Check the repository status:

```bash
git status
```

Save changes:

```bash
git add .
git commit -m "Update project"
```

Push changes to a remote repository:

```bash
git push
```

Git allows you to track changes and recover previous versions of your project.

---

# Monitor System Resources

Check memory:

```bash
free -h
```

Check disk usage:

```bash
df -h
```

Check directory size:

```bash
du -sh directory/
```

Monitor processes:

```bash
top
```

These commands can help identify resource problems.

---

# Check Running Processes

List running processes:

```bash
ps
```

Show more detailed information:

```bash
ps aux
```

Search for a process:

```bash
ps aux | grep python
```

If a process needs to be stopped, first identify its PID:

```bash
ps aux
```

Then:

```bash
kill PID
```

Use process-killing commands carefully.

---

# Manage Disk Space

Check available disk space:

```bash
df -h
```

Find the size of directories:

```bash
du -sh *
```

Large files and unnecessary packages can consume disk space quickly.

Regularly checking disk usage can prevent unexpected storage problems.

---

# Use Shell Scripts Carefully

Before running a script, inspect its contents.

View a script:

```bash
cat script.sh
```

Check syntax:

```bash
bash -n script.sh
```

Run it in debug mode:

```bash
bash -x script.sh
```

Avoid running scripts from unknown sources without understanding what they do.

---

# Keep Scripts Readable

Use meaningful variable names:

```bash
username="Somya"
```

instead of:

```bash
x="Somya"
```

Add comments where necessary:

```bash
# Create a backup of the project
cp -r project project-backup
```

Readable scripts are easier to debug and maintain.

---

# Use Logs for Troubleshooting

Logs can help identify errors and system problems.

Some Linux logs can be found under:

```text
/var/log/
```

List log files:

```bash
ls /var/log/
```

For example:

```bash
cat /var/log/syslog
```

The exact logs available depend on the Linux distribution and configuration.

---

# Check Network Connectivity

Useful commands for troubleshooting network problems include:

```bash
ping google.com
```

Check network interfaces:

```bash
ip addr
```

Check routes:

```bash
ip route
```

These commands can help determine whether the system has network connectivity.

---

# Avoid Unnecessary Services

Running unnecessary services can consume resources and increase security risks.

On systems using `systemd`, check services with:

```bash
systemctl
```

Check the status of a service:

```bash
systemctl status service-name
```

Only disable services when you understand what they are used for.

---

# Protect Sensitive Information

Do not store passwords, API keys, or other secrets directly inside scripts or public repositories.

Avoid:

```bash
API_KEY="my-secret-key"
```

inside a GitHub repository.

Instead, use environment variables or appropriate secret-management tools.

Also avoid accidentally committing files containing credentials.

---

# Clean Up Carefully

Remove unnecessary files when you are sure they are no longer needed.

Remove a file:

```bash
rm file.txt
```

Remove an empty directory:

```bash
rmdir directory
```

Before deleting anything, verify the file or directory path.

---

# Common Mistakes

## Running Commands Without Understanding Them

Do not blindly copy commands from the internet.

Understand what the command does before executing it.

## Using chmod 777 Unnecessarily

Avoid:

```bash
chmod 777 file
```

Use the minimum permissions required.

## Using sudo Everywhere

Not every command requires administrative privileges.

Use `sudo` only when necessary.

## Overwriting Files Accidentally

Be careful with:

```bash
>
```

because it can replace existing content.

## Deleting the Wrong Files

Always verify the path before using:

```bash
rm
```

especially with recursive deletion.

---

# Useful Safety Checklist

Before running an important command, ask:

- Am I in the correct directory?
- What exactly will this command do?
- Will it modify or delete files?
- Do I really need `sudo`?
- Is the command from a trusted source?
- Do I have a backup if something goes wrong?

---

# Linux Productivity Tips

| Shortcut | Purpose |
|----------|---------|
| `Ctrl + C` | Stop the current command |
| `Ctrl + L` | Clear the terminal |
| `Ctrl + R` | Search command history |
| `Ctrl + D` | Exit the shell |
| `Tab` | Autocomplete |
| `↑` / `↓` | Navigate command history |

---

# Best Practices Summary

Good Linux practices include:

1. Use the minimum permissions required.
2. Be careful when using `sudo`.
3. Keep the system updated.
4. Understand commands before executing them.
5. Keep files and directories organized.
6. Use Git for source-code version control.
7. Back up important data.
8. Monitor disk and system resources.
9. Protect passwords and API keys.
10. Test scripts before running them.
11. Keep scripts readable.
12. Be careful with commands that delete or overwrite data.

---

# What I Learned

Through this Linux section, I learned how to:

- Navigate the Linux file system.
- Create, copy, move, rename, and delete files.
- Manage directories.
- Work with permissions.
- Manage users and groups.
- Install and manage packages.
- Work with processes.
- Use networking commands.
- Use pipes and redirection.
- Write Bash scripts.
- Automate tasks.
- Troubleshoot common Linux problems.
- Follow safer Linux practices.

---

# Linux Section Complete

This chapter completes the Linux section of my learning journey.

## Chapters Covered

```text
01 - Introduction to Linux
02 - Linux File System
03 - Basic Linux Commands
04 - File and Directory Management
05 - File Permissions
06 - Users and Groups
07 - Package Management
08 - Shell and Bash
09 - Process Management
10 - Networking Commands
11 - Redirection and Pipes
12 - Bash Scripting
13 - Linux Best Practices
```

---

## Navigation

⬅️ Previous: [Bash Scripting](12-Bash-Scripting.md)

➡️ Next: Coming Soon
