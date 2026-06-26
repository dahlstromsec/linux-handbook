# Bash

Bash is the default shell on many Linux distributions and allows users to automate tasks and interact with the operating system.

---

## Variables

### Purpose

Store values for later use.

### Syntax

```bash
name="Christoffer"
echo $name
```

### Related Commands

- Environment Variables

---

## Environment Variables

### Purpose

Store configuration values available to the shell.

### Example

```bash
echo $HOME
echo $PATH
```

### Related Commands

- `printenv`

---

## Aliases

### Purpose

Create custom shortcuts for commands.

### Example

```bash
alias ll="ls -la"
```

---

## Pipes

### Purpose

Send the output of one command to another.

### Example

```bash
ps aux | grep ssh
```

### Cybersecurity Context

Often used when filtering logs and process output.

---

## Redirection

### Purpose

Redirect command output to files.

### Example

```bash
ls > files.txt
echo "test" >> notes.txt
```

---

## Command Substitution

### Purpose

Use the output of one command inside another.

### Example

```bash
echo $(pwd)
```

---

## Shell Scripts

### Purpose

Automate repetitive tasks.

### Example

```bash
#!/bin/bash
echo "Hello World"
```
