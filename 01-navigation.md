# Navigation

Navigation commands are used to move around the Linux file system and determine your current working location.

Understanding these commands is essential before working with files, directories, or system administration tasks.

---

## pwd

### Purpose

Displays the absolute path of the current working directory.

### Syntax

```bash
pwd
```

### Example

```bash
pwd
```

Output

```text
/home/christoffer/Documents
```

### Common Uses

- Verify your current location.
- Confirm where commands will execute.
- Avoid working in the wrong directory.

### Cybersecurity Context

Before searching log files, editing configuration files, or running scripts, it is good practice to verify your current working directory.

### Related Commands

- `ls`
- `cd`

---

## ls

### Purpose

Lists files and directories in the current working directory.

### Syntax

```bash
ls
```

### Example

```bash
ls
```

Output

```text
Documents  Downloads  Pictures  Music
```

### Common Uses

- View directory contents.
- Confirm files exist.
- Inspect a directory quickly.

### Cybersecurity Context

Frequently used when navigating Linux systems during investigations and incident response.

### Related Commands

- `pwd`
- `cd`
- `find`

---

## ls -l

### Purpose

Displays files and directories in long listing format.

### Syntax

```bash
ls -l
```

### Example

```bash
ls -l
```

Output

```text
drwxr-xr-x 2 christoffer users 4096 Jul 30 12:15 Documents
-rw-r--r-- 1 christoffer users 842 Jul 29 20:48 notes.txt
```

### Common Uses

- View permissions.
- View ownership.
- View file size and modification time.

### Cybersecurity Context

Useful for inspecting permissions and ownership during investigations.

### Related Commands

- `chmod`
- `chown`
- `stat`
