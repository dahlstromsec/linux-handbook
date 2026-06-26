# Package Management

Package managers install, update, search for, and remove software.

---

## apt update

### Purpose

Updates the local package index.

### Syntax

```bash
sudo apt update
```

### Common Uses

- Refresh package information before installing or upgrading software.

### Cybersecurity Context

Always update package lists before applying security updates.

### Related Commands

- `apt upgrade`
- `apt install`

---

## apt upgrade

### Purpose

Upgrades installed packages to newer versions.

### Syntax

```bash
sudo apt upgrade
```

### Common Uses

- Install security patches.
- Keep the system up to date.

### Cybersecurity Context

Regular updates reduce exposure to known vulnerabilities.

### Related Commands

- `apt update`

---

## apt install

### Purpose

Installs software packages.

### Syntax

```bash
sudo apt install PACKAGE
```

### Example

```bash
sudo apt install nmap
```

### Related Commands

- `apt remove`

---

## apt remove

### Purpose

Removes an installed package.

### Syntax

```bash
sudo apt remove PACKAGE
```

### Related Commands

- `apt install`

---

## apt search

### Purpose

Searches for available packages.

### Syntax

```bash
apt search KEYWORD
```

### Related Commands

- `apt install`
