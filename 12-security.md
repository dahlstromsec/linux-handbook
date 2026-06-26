# Security Commands

These commands are commonly used when verifying files, investigating systems, and checking integrity.

---

## history

### Purpose

Displays previously executed commands.

### Syntax

```bash
history
```

### Cybersecurity Context

Useful during incident response and auditing.

### Related Commands

- `grep`

---

## passwd

### Purpose

Changes a user's password.

### Syntax

```bash
passwd
```

### Related Commands

- `sudo`

---

## sha256sum

### Purpose

Calculates a SHA-256 hash.

### Syntax

```bash
sha256sum FILE
```

### Cybersecurity Context

Used to verify file integrity and compare hashes.

### Related Commands

- `md5sum`

---

## md5sum

### Purpose

Calculates an MD5 hash.

### Syntax

```bash
md5sum FILE
```

### Cybersecurity Context

Still useful for comparisons, though SHA-256 is preferred for integrity verification.

### Related Commands

- `sha256sum`

---

## file

### Purpose

Identifies a file's type.

### Syntax

```bash
file FILE
```

### Cybersecurity Context

Useful when investigating unknown files.

### Related Commands

- `stat`

---

## stat

### Purpose

Displays detailed file metadata.

### Syntax

```bash
stat FILE
```

### Related Commands

- `ls -l`
