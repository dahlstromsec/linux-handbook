# Files & Directories

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner
> **Prerequisites:** Navigation

Working with files and directories is one of the most common tasks in Linux. Whether you're creating scripts, organizing files, copying logs, or removing temporary data, these commands form the foundation of daily Linux usage.

Understanding how to safely create, copy, move, inspect, and delete files is essential before moving on to more advanced Linux administration or cybersecurity tasks.

---

## What You'll Learn

* Creating files and directories
* Copying and moving files
* Removing files safely
* Viewing file contents
* Reading large files efficiently

---

# File & Directory Commands

---

## touch

### Purpose

Creates a new empty file or updates the modification timestamp of an existing file.

### Syntax

```bash
touch FILE
```

### Examples

```bash
touch notes.txt

touch report.md

touch script.sh
```

### Common Uses

* Create a new file.
* Prepare a script before editing.
* Update a file's timestamp.

### Cybersecurity Context

Often used when creating scripts, notes, or test files during labs and security assessments.

### Related Commands

* `cat`
* `nano`
* `mv`

---

## mkdir

### Purpose

Creates one or more directories.

### Syntax

```bash
mkdir DIRECTORY
```

### Examples

```bash
mkdir Projects

mkdir Notes

mkdir -p Labs/TryHackMe/Linux
```

### Common Uses

* Organize projects.
* Create folder structures.
* Prepare working directories.

### Cybersecurity Context

Useful for organizing investigation files, lab environments, and scripts.

### Related Commands

* `rmdir`
* `cd`

---

## rmdir

### Purpose

Removes an empty directory.

### Syntax

```bash
rmdir DIRECTORY
```

### Example

```bash
rmdir EmptyFolder
```

### Common Uses

* Remove unused empty directories.
* Clean up folder structures.

### Cybersecurity Context

Helpful when cleaning up temporary lab environments.

### Related Commands

* `rm`
* `rm -r`

---

## rm

### Purpose

Removes files from the file system.

### Syntax

```bash
rm FILE
```

### Examples

```bash
rm notes.txt

rm report.pdf
```

### Common Uses

* Delete files.
* Remove temporary files.
* Clean up directories.

### Cybersecurity Context

Be cautious when deleting files on production systems or during investigations, as removed evidence may not be recoverable.

### Related Commands

* `rm -r`

---

## rm -r

### Purpose

Recursively removes directories and their contents.

### Syntax

```bash
rm -r DIRECTORY
```

### Example

```bash
rm -r OldProject
```

### Common Uses

* Remove directories containing files.
* Delete project folders.

### Cybersecurity Context

One of the most dangerous Linux commands. Always verify the directory before running recursive deletion.

### Related Commands

* `rm`
* `rmdir`

---

## cp

### Purpose

Copies files and directories.

### Syntax

```bash
cp SOURCE DESTINATION
```

### Examples

```bash
cp notes.txt backup.txt

cp report.pdf ~/Documents

cp -r Folder BackupFolder
```

### Common Uses

* Create backups.
* Duplicate files.
* Copy directories.

### Cybersecurity Context

Useful for creating backups of log files or preserving evidence before analysis.

### Related Commands

* `mv`

---

## mv

### Purpose

Moves or renames files and directories.

### Syntax

```bash
mv SOURCE DESTINATION
```

### Examples

```bash
mv report.txt Reports/

mv old.txt new.txt
```

### Common Uses

* Rename files.
* Move files.
* Organize directories.

### Cybersecurity Context

Useful when organizing investigation artifacts or scripts.

### Related Commands

* `cp`

---

## cat

### Purpose

Displays the contents of a file.

### Syntax

```bash
cat FILE
```

### Examples

```bash
cat notes.txt

cat /etc/os-release
```

### Common Uses

* Read text files.
* Combine multiple files.
* Quickly inspect file contents.

### Cybersecurity Context

Frequently used to inspect configuration files and log files.

### Related Commands

* `less`
* `head`
* `tail`

---

## less

### Purpose

Displays file contents one page at a time.

### Syntax

```bash
less FILE
```

### Example

```bash
less /var/log/syslog
```

### Common Uses

* Read large files.
* Navigate logs efficiently.

### Cybersecurity Context

Commonly used to inspect large log files during incident response and troubleshooting.

### Related Commands

* `cat`
* `tail`

---

## head

### Purpose

Displays the first lines of a file.

### Syntax

```bash
head FILE
```

### Example

```bash
head access.log
```

### Common Uses

* Preview large files.
* Verify file contents.

### Cybersecurity Context

Useful for quickly checking the beginning of log files.

### Related Commands

* `tail`

---

## tail

### Purpose

Displays the last lines of a file.

### Syntax

```bash
tail FILE
```

### Examples

```bash
tail auth.log

tail -f auth.log
```

### Common Uses

* View recent log entries.
* Monitor files in real time.

### Cybersecurity Context

`tail -f` is widely used by administrators and SOC analysts to monitor logs as new events are written.

### Related Commands

* `head`
* `less`

---

# Common Mistakes

| Problem                | Cause                           |
| ---------------------- | ------------------------------- |
| Deleted the wrong file | Incorrect path used with `rm`   |
| `rmdir` failed         | Directory is not empty          |
| `cp` failed            | Destination path does not exist |
| `Permission denied`    | Insufficient permissions        |

---

# Summary

You should now be comfortable creating, copying, moving, viewing, and deleting files and directories. These commands are used constantly in Linux and provide the foundation for scripting, system administration, and cybersecurity tasks.

---

# Related Chapters

* Navigation
* Searching
* Permissions
* Bash
