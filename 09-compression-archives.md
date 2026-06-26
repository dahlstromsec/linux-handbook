# Compression & Archives

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner
> **Prerequisites:** Files & Directories

Compression reduces file size, while archives combine multiple files into a single package. These commands are commonly used for backups, file transfers, and log collection.

---

## What You'll Learn

* Creating archives
* Compressing files
* Extracting archives
* Working with ZIP and TAR files

---

# Archive Commands

---

## tar

### Purpose

Creates and extracts archive files.

### Syntax

```bash
tar [OPTIONS] ARCHIVE FILES
```

### Examples

```bash
tar -cvf backup.tar Documents/

tar -xvf backup.tar
```

### Common Uses

* Create backups.
* Archive project folders.
* Package multiple files together.

### Cybersecurity Context

Frequently used to archive logs or evidence before transferring them to another system.

### Related Commands

* `gzip`
* `zip`

---

## gzip

### Purpose

Compresses a file using the Gzip format.

### Syntax

```bash
gzip FILE
```

### Example

```bash
gzip access.log
```

### Common Uses

* Compress log files.
* Reduce storage usage.

### Cybersecurity Context

Large log files are commonly compressed before long-term storage or transfer.

### Related Commands

* `gunzip`
* `tar`

---

## gunzip

### Purpose

Decompresses Gzip-compressed files.

### Syntax

```bash
gunzip FILE.gz
```

### Example

```bash
gunzip access.log.gz
```

### Common Uses

* Restore compressed logs.
* Extract archived files.

### Cybersecurity Context

Useful when reviewing archived logs during investigations.

### Related Commands

* `gzip`

---

## zip

### Purpose

Creates ZIP archives.

### Syntax

```bash
zip ARCHIVE FILE
```

### Example

```bash
zip backup.zip report.pdf
```

### Common Uses

* Package files for sharing.
* Create compressed backups.

### Cybersecurity Context

Often used to package investigation reports or exported data before transferring them securely.

### Related Commands

* `unzip`

---

## unzip

### Purpose

Extracts ZIP archives.

### Syntax

```bash
unzip ARCHIVE.zip
```

### Example

```bash
unzip backup.zip
```

### Common Uses

* Extract downloaded archives.
* Restore compressed backups.

### Cybersecurity Context

Always verify the source of downloaded ZIP archives before extracting them, as they may contain malicious files.

### Related Commands

* `zip`

---

# Common Mistakes

| Problem               | Cause                             |
| --------------------- | --------------------------------- |
| Archive won't extract | Incorrect archive format          |
| File already exists   | Existing files may be overwritten |
| Permission denied     | Insufficient permissions          |

---

# Summary

You should now understand how to create archives, compress files, and extract common archive formats used on Linux systems.

---

# Related Chapters

* Files & Directories
* Storage & Filesystems
* Security
