# Bash Scripting

Bash scripting allows us to automate tasks by combining Linux commands, variables, conditions, loops, and functions into a single script.

A Bash script is a text file containing commands that are executed by the Bash shell.

---

## What is Bash Scripting?

Bash is both:

- A command-line shell.
- A scripting language.

Instead of entering commands one by one, we can put them inside a script and execute them together.

Example:

```bash
#!/bin/bash

echo "Hello"
echo "Welcome to Linux"
```

---

## Creating a Bash Script

Create a file with the `.sh` extension:

```bash
touch script.sh
```

Open the file and add:

```bash
#!/bin/bash

echo "Hello, Linux!"
```

The first line is called the **shebang**. It tells Linux which interpreter should be used to execute the script.

---

## Running a Bash Script

First, give the script execute permission:

```bash
chmod +x script.sh
```

Run the script:

```bash
./script.sh
```

You can also execute it directly using Bash:

```bash
bash script.sh
```

---

## Variables

Variables are used to store values.

```bash
name="Linux"
age=20

echo "Name: $name"
echo "Age: $age"
```

Output:

```text
Name: Linux
Age: 20
```

> **Note:** Do not use spaces around `=` when assigning a variable.

Correct:

```bash
name="Linux"
```

Incorrect:

```bash
name = "Linux"
```

---

## User Input

The `read` command allows a script to accept input from the user.

```bash
#!/bin/bash

echo "Enter your name:"
read name

echo "Hello, $name!"
```

You can also use `read -p`:

```bash
read -p "Enter your name: " name
echo "Hello, $name!"
```

---

## Command-Line Arguments

A script can receive arguments when it is executed.

Example:

```bash
#!/bin/bash

echo "Hello, $1"
```

Run:

```bash
./script.sh Somya
```

Output:

```text
Hello, Somya
```

Common special variables:

| Variable | Meaning |
|----------|---------|
| `$0` | Script name |
| `$1` | First argument |
| `$2` | Second argument |
| `$#` | Number of arguments |
| `$@` | All arguments |
| `$?` | Exit status of previous command |

Example:

```bash
echo "Script: $0"
echo "First argument: $1"
echo "Second argument: $2"
```

---

## Environment Variables

Linux provides environment variables containing information about the current environment.

Some useful variables are:

```bash
echo $HOME
echo $USER
echo $PWD
```

You can create an environment variable using:

```bash
export PROJECT="Learning-Lab"
```

Check it:

```bash
echo $PROJECT
```

---

## Command Substitution

Command substitution allows the output of a command to be used inside another command.

```bash
current_dir=$(pwd)

echo "Current directory: $current_dir"
```

Another example:

```bash
today=$(date)

echo "Today is: $today"
```

---

## Conditional Statements

Conditional statements allow a script to make decisions.

Basic structure:

```bash
if [ condition ]; then
    command
else
    command
fi
```

Example:

```bash
age=20

if [ "$age" -ge 18 ]; then
    echo "Adult"
else
    echo "Minor"
fi
```

---

## if, elif and else

Multiple conditions can be checked using `elif`.

```bash
marks=75

if [ "$marks" -ge 90 ]; then
    echo "Grade A"
elif [ "$marks" -ge 60 ]; then
    echo "Grade B"
elif [ "$marks" -ge 40 ]; then
    echo "Grade C"
else
    echo "Fail"
fi
```

---

## Comparison Operators

### Numeric Comparisons

| Operator | Meaning |
|----------|---------|
| `-eq` | Equal |
| `-ne` | Not equal |
| `-gt` | Greater than |
| `-lt` | Less than |
| `-ge` | Greater than or equal |
| `-le` | Less than or equal |

Example:

```bash
num=10

if [ "$num" -gt 5 ]; then
    echo "Number is greater than 5"
fi
```

### String Comparisons

| Operator | Meaning |
|----------|---------|
| `=` | Equal |
| `!=` | Not equal |
| `-z` | Empty string |
| `-n` | Non-empty string |

Example:

```bash
name="Linux"

if [ "$name" = "Linux" ]; then
    echo "Correct"
fi
```

---

## File Tests

Bash can check whether files and directories exist.

Check for a file:

```bash
if [ -f "notes.txt" ]; then
    echo "File exists"
fi
```

Check for a directory:

```bash
if [ -d "Documents" ]; then
    echo "Directory exists"
fi
```

Common file tests:

| Operator | Meaning |
|----------|---------|
| `-f` | Regular file exists |
| `-d` | Directory exists |
| `-e` | Path exists |
| `-r` | File is readable |
| `-w` | File is writable |
| `-x` | File is executable |

---

## Case Statement

The `case` statement is useful when a variable can have multiple possible values.

```bash
choice="start"

case "$choice" in
    start)
        echo "Starting..."
        ;;
    stop)
        echo "Stopping..."
        ;;
    restart)
        echo "Restarting..."
        ;;
    *)
        echo "Unknown option"
        ;;
esac
```

The `*` acts as the default case.

---

## For Loop

A `for` loop repeats commands for each item in a list.

```bash
for name in Linux Git Python
do
    echo "$name"
done
```

Output:

```text
Linux
Git
Python
```

Another example:

```bash
for number in 1 2 3 4 5
do
    echo "Number: $number"
done
```

---

## While Loop

A `while` loop continues running while a condition is true.

```bash
count=1

while [ "$count" -le 5 ]
do
    echo "$count"
    count=$((count + 1))
done
```

Output:

```text
1
2
3
4
5
```

---

## Functions

Functions allow us to create reusable blocks of code.

```bash
greet() {
    echo "Hello, Linux!"
}

greet
```

Functions can also accept arguments:

```bash
greet() {
    echo "Hello, $1!"
}

greet Somya
```

Output:

```text
Hello, Somya!
```

Functions make larger scripts easier to organize and maintain.

---

## Arithmetic

Bash supports basic arithmetic using `$(( ))`.

```bash
a=10
b=5

sum=$((a + b))

echo "Sum = $sum"
```

Output:

```text
Sum = 15
```

Common arithmetic operators:

| Operator | Operation |
|----------|-----------|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Modulus |

Example:

```bash
num=10

result=$((num * 2))

echo "$result"
```

---

## Exit Status

Every command returns an exit status.

A successful command normally returns:

```text
0
```

You can check the exit status of the previous command using:

```bash
echo $?
```

Example:

```bash
ls
echo $?
```

If `ls` succeeds, the output will normally be:

```text
0
```

A non-zero value generally indicates that an error occurred.

---

## Redirection and Pipes in Scripts

The redirection and pipe operators learned earlier can also be used inside Bash scripts.

Save output:

```bash
ls > files.txt
```

Append output:

```bash
date >> log.txt
```

Use a pipe:

```bash
ps aux | grep python
```

This makes it possible to combine multiple commands inside a script.

---

## Comments

Comments are ignored by Bash and are useful for explaining code.

Use `#`:

```bash
# Display the current username

whoami
```

You can also use comments to describe sections:

```bash
# Check whether the directory exists

if [ -d "Documents" ]; then
    echo "Directory found"
fi
```

---

## Practical Example

The following script combines variables, user input, conditions, and arithmetic.

```bash
#!/bin/bash

read -p "Enter your name: " name
read -p "Enter your age: " age

if [ "$age" -ge 18 ]; then
    echo "Hello, $name!"
    echo "You are an adult."
else
    echo "Hello, $name!"
    echo "You are a minor."
fi
```

This script:

1. Takes the user's name.
2. Takes the user's age.
3. Checks the age.
4. Displays the appropriate message.

---

## Debugging Bash Scripts

Bash provides options that help with debugging.

Run a script in debug mode:

```bash
bash -x script.sh
```

Bash will display commands as they are executed.

Check the syntax without executing the script:

```bash
bash -n script.sh
```

These commands are useful when troubleshooting scripts.

---

## Best Practices

- Start scripts with a proper shebang.
- Use meaningful variable names.
- Quote variables when appropriate.
- Add comments to explain complex sections.
- Keep scripts organized using functions.
- Test scripts before using them on important files.
- Avoid using `sudo` unless necessary.
- Check commands and file paths carefully.
- Use `bash -n` to check syntax.
- Use `bash -x` when debugging.

---

## Common Mistakes

### Spaces Around `=`

Incorrect:

```bash
name = "Linux"
```

Correct:

```bash
name="Linux"
```

### Forgetting Execute Permission

Before using:

```bash
./script.sh
```

make sure the script is executable:

```bash
chmod +x script.sh
```

### Forgetting Quotes

Prefer:

```bash
echo "$name"
```

instead of:

```bash
echo $name
```

Quoting variables helps avoid unexpected behavior when values contain spaces or special characters.

---

## Command Summary

| Command / Syntax | Purpose |
|------------------|---------|
| `#!/bin/bash` | Specify Bash interpreter |
| `chmod +x` | Make a script executable |
| `read` | Read user input |
| `if` | Conditional execution |
| `case` | Handle multiple choices |
| `for` | Repeat commands |
| `while` | Repeat while a condition is true |
| `function()` | Define reusable code |
| `$1`, `$2` | Script arguments |
| `$@` | All script arguments |
| `$?` | Previous command's exit status |
| `$(( ))` | Perform arithmetic |
| `bash -n` | Check script syntax |
| `bash -x` | Debug a script |

---

## Summary

In this chapter, you learned:

- What Bash scripting is.
- How to create and execute Bash scripts.
- How to use variables and user input.
- How to use command-line arguments.
- How environment variables work.
- How to use conditional statements.
- How to use `case` statements.
- How to use `for` and `while` loops.
- How to create functions.
- How to perform arithmetic.
- How to check exit status.
- How to use pipes and redirection in scripts.
- How to debug Bash scripts.

---

## Navigation

⬅️ Previous: [Redirection and Pipes](11-Redirection-and-Pipes.md)

➡️ Next: [Linux Best Practices](13-Linux-Best-Practices.md)
