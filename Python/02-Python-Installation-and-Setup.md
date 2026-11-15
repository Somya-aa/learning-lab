# Chapter 2: Python Installation and Setup

## 1. Introduction

Before writing Python programs, we need to install Python and configure a development environment.

Python programs can be written using a simple text editor, an IDE, or a code editor such as Visual Studio Code.

In this chapter, we will learn how to install Python, verify the installation, configure VS Code, and execute Python programs.

## 2. Installing Python

Follow these steps to install Python:

1. Visit the official Python website.
2. Open the Downloads section.
3. Download the latest stable version for your operating system.
4. Run the installer.
5. On Windows, select **Add Python to PATH**.
6. Click Install Now and complete the installation.

Official website: https://www.python.org/downloads/

## 3. Verify Python Installation

After installation, open Command Prompt or the VS Code terminal.

Check the installed Python version:

```bash
python --version
```

You can also try:

```bash
python -V
```

On some Windows systems, use:

```bash
py --version
```

If Python is installed correctly, the terminal displays its installed version.

## 4. Python Interpreter

A Python interpreter is a program that executes Python code.

It allows us to run Python instructions directly or execute programs saved in `.py` files.

Python provides an interactive mode called the **Python Shell** or **REPL**.

REPL stands for:

- Read
- Evaluate
- Print
- Loop

To open the Python interactive shell, enter:

```bash
python
```

Example:

```python
>>> 10 + 20
30

>>> print("Hello Python")
Hello Python
```

To exit the interactive shell:

```python
exit()
```

## 5. Installing Visual Studio Code

Visual Studio Code is a popular code editor used for Python development.

Installation steps:

1. Visit https://code.visualstudio.com/
2. Download Visual Studio Code.
3. Run the installer.
4. Complete the installation.
5. Open VS Code.

## 6. Setting Up Python in VS Code

Follow these steps:

1. Open Visual Studio Code.
2. Open the Extensions section.
3. Search for **Python**.
4. Install the official Python extension published by Microsoft.
5. Open your project folder.
6. Create a new file named `hello.py`.
7. Write your Python code.
8. Select the installed Python interpreter using the command palette.

To open the command palette, press:

```text
Ctrl + Shift + P
```

Search for:

```text
Python: Select Interpreter
```

Select the Python installation you want to use.

## 7. Running a Python Program

Create a file named `hello.py`.

Write the following code:

```python
print("Hello, World!")
print("Welcome to Python Programming")
```

Run the program using the terminal:

```bash
python hello.py
```

**Output:**

```text
Hello, World!
Welcome to Python Programming
```

You can also use the Run button provided by the Python extension in VS Code.

## 8. Understanding pip

`pip` is the standard package installer for Python.

It is used to install and manage external Python packages.

Check the pip version:

```bash
python -m pip --version
```

Install a package:

```bash
python -m pip install requests
```

View installed packages:

```bash
python -m pip list
```

Upgrade pip:

```bash
python -m pip install --upgrade pip
```

## 9. Virtual Environments

A virtual environment creates an isolated Python environment for a project.

It helps manage dependencies separately and prevents conflicts between different projects.

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Activate it on Linux or macOS:

```bash
source venv/bin/activate
```

Deactivate the environment:

```bash
deactivate
```

**Best Practice:** Use a separate virtual environment for each Python project.

## 10. Common Installation Problems

| Problem | Possible Solution |
|---|---|
| Python command not recognized | Check whether Python is added to PATH |
| Wrong Python version | Select the correct interpreter |
| pip command not working | Try `python -m pip` |
| Module not found | Install the required package |
| VS Code cannot find Python | Select the installed interpreter |
| Permission error | Check folder permissions and environment settings |

## 11. Important Commands

| Command | Purpose |
|---|---|
| `python --version` | Check Python version |
| `python` | Open Python interactive shell |
| `python filename.py` | Execute a Python file |
| `python -m pip --version` | Check pip version |
| `python -m pip install package` | Install a package |
| `python -m pip list` | Display installed packages |
| `python -m venv venv` | Create a virtual environment |
| `deactivate` | Exit a virtual environment |

## 12. What I Learned

After completing this chapter, I understand:

- How to download and install Python.
- How to verify the Python installation.
- What a Python interpreter and REPL are.
- How to configure Python in VS Code.
- How to create and execute Python files.
- How to use pip to install packages.
- How to create and manage virtual environments.
- How to identify common installation problems.

## Summary

Setting up Python correctly is the first practical step toward Python development. With Python, VS Code, pip, and virtual environments configured, we can create, execute, and manage Python projects efficiently.

---

### Navigation

⬅️ Previous: [Introduction to Python](01-Introduction-to-Python.md)

➡️ Next: [Python Syntax and Variables](03-Python-Syntax-and-Variables.md)