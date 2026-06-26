# Bash

> **Estimated Reading Time:** 15–20 minutes
> **Difficulty:** Beginner–Intermediate
> **Prerequisites:** Navigation, Files & Directories

Bash (Bourne Again Shell) is the default command-line shell on many Linux distributions. It allows you to execute commands, automate repetitive tasks, manipulate files, and combine commands into powerful workflows.

Learning Bash is essential for Linux administration, scripting, and cybersecurity.

---

## What You'll Learn

* Variables
* Environment Variables
* Aliases
* Pipes
* Redirection
* Command Substitution
* Basic Shell Scripts

---

# Bash Fundamentals

---

## Variables

### Purpose

Variables store data that can be reused throughout a command or script.

### Syntax

```bash
variable="value"
```

### Examples

```bash
filename="report.txt"

echo $filename
```

```bash
directory="/var/log"

ls $directory
```

### Common Uses

* Store filenames.
* Store directory paths.
* Simplify scripts.
* Reuse values.

### Cybersecurity Context

Variables are commonly used in Bash scripts that automate log analysis, backups, and security checks.

### Related Commands

* Environment Variables

---

## Environment Variables

### Purpose

Environment variables store information that is available throughout the current shell session.

### Examples

```bash
echo $HOME

echo $PATH

echo $USER

printenv
```

### Common Uses

* Display system information.
* Configure applications.
* Locate executables.

### Cybersecurity Context

Understanding variables such as `PATH` helps identify where executables are loaded from and can assist when investigating suspicious binaries.

### Related Commands

* `printenv`

---

## Aliases

### Purpose

Creates custom shortcuts for frequently used commands.

### Syntax

```bash
alias name="command"
```

### Example

```bash
alias ll="ls -lah"
```

### Common Uses

* Reduce typing.
* Customize the shell.
* Improve productivity.

### Cybersecurity Context

Aliases are often used to speed up repetitive administrative and security tasks.

### Related Commands

* `unalias`

---

## Pipes (`|`)

### Purpose

Passes the output of one command directly to another.

### Examples

```bash
ps aux | grep ssh
```

```bash
cat access.log | grep "Failed password"
```

```bash
ls -la | less
```

### Common Uses

* Filter command output.
* Chain multiple commands.
* Process log files.

### Cybersecurity Context

Pipes are heavily used by SOC analysts when searching logs, filtering processes, and analyzing command output.

### Related Commands

* `grep`
* `sort`
* `uniq`

---

## Redirection

### Purpose

Redirects command output or input.

### Examples

Overwrite a file:

```bash
ls > files.txt
```

Append to a file:

```bash
echo "Log entry" >> notes.txt
```

Read input from a file:

```bash
sort < users.txt
```

### Common Uses

* Save command output.
* Create log files.
* Build scripts.

### Cybersecurity Context

Useful when collecting evidence, exporting logs, or saving command output for later analysis.

### Related Commands

* Pipes

---

## Command Substitution

### Purpose

Uses the output of one command inside another command.

### Syntax

```bash
$(command)
```

### Examples

```bash
echo $(pwd)
```

```bash
mkdir $(date +%F)
```

### Common Uses

* Build dynamic commands.
* Automate scripts.
* Reuse command output.

### Cybersecurity Context

Frequently used in automation scripts to dynamically generate filenames, timestamps, or paths.

### Related Commands

* Variables

---

## Basic Shell Scripts

### Purpose

Automates repetitive tasks by executing multiple commands from a single file.

### Example

```bash
#!/bin/bash

echo "System Information"

hostname

whoami

pwd
```

Run the script:

```bash
chmod +x script.sh

./script.sh
```

### Common Uses

* System administration.
* Backups.
* Log collection.
* Automation.

### Cybersecurity Context

Shell scripts are widely used to automate security checks, collect logs, perform backups, and assist during incident response.

### Related Commands

* `chmod`
* `bash`

---

# Common Mistakes

| Problem              | Cause                                      |
| -------------------- | ------------------------------------------ |
| Variable is empty    | Forgot the `$` when reading it             |
| Script won't execute | Missing execute permission (`chmod +x`)    |
| `command not found`  | Incorrect PATH or command spelling         |
| Alias doesn't work   | Alias wasn't loaded into the current shell |

---

# Summary

You should now understand the Bash features that are used most frequently when working with Linux systems. These fundamentals form the basis of automation, scripting, and many cybersecurity workflows.

---

# Related Chapters

* Navigation
* Processes
* Git
* Security
