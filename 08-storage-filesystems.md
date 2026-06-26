# Storage & Filesystems

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner
> **Prerequisites:** Files & Directories

Linux stores data on block devices such as hard drives, SSDs, and USB devices. These commands help you inspect disk usage, identify storage devices, and mount or unmount filesystems.

---

## What You'll Learn

* Viewing disk usage
* Measuring directory size
* Mounting filesystems
* Unmounting storage devices
* Viewing connected disks

---

# Storage Commands

---

## df -h

### Purpose

Displays disk space usage for mounted filesystems in a human-readable format.

### Syntax

```bash
df -h
```

### Example

```bash
df -h
```

### Common Uses

* Check available disk space.
* Identify nearly full drives.
* Verify mounted filesystems.

### Cybersecurity Context

Useful when investigating systems that have stopped logging due to a full disk or when checking available storage before collecting forensic evidence.

### Related Commands

* `du`
* `lsblk`

---

## du -sh

### Purpose

Displays the total size of a directory.

### Syntax

```bash
du -sh DIRECTORY
```

### Examples

```bash
du -sh ~/Downloads

du -sh /var/log
```

### Common Uses

* Find large directories.
* Monitor storage usage.
* Identify unnecessary files.

### Cybersecurity Context

Useful when identifying large log directories or unexpected data growth caused by malware or excessive logging.

### Related Commands

* `df -h`

---

## mount

### Purpose

Mounts a filesystem, making it accessible through the Linux directory structure.

### Syntax

```bash
mount DEVICE DIRECTORY
```

### Example

```bash
sudo mount /dev/sdb1 /mnt
```

### Common Uses

* Mount USB drives.
* Access additional disks.
* Mount ISO images.

### Cybersecurity Context

Frequently used when mounting forensic images or removable media during investigations.

### Related Commands

* `umount`

---

## umount

### Purpose

Safely unmounts a mounted filesystem.

### Syntax

```bash
umount DIRECTORY
```

### Example

```bash
sudo umount /mnt
```

### Common Uses

* Safely remove USB devices.
* Disconnect mounted drives.

### Cybersecurity Context

Always unmount storage devices before disconnecting them to prevent data corruption.

### Related Commands

* `mount`

---

## lsblk

### Purpose

Lists available block devices such as hard drives, SSDs, and USB devices.

### Syntax

```bash
lsblk
```

### Example

```bash
lsblk
```

### Common Uses

* View connected storage devices.
* Identify partitions.
* Verify newly connected disks.

### Cybersecurity Context

Useful when identifying removable media, external drives, or forensic disks connected to a system.

### Related Commands

* `df -h`
* `mount`

---

# Common Mistakes

| Problem                   | Cause                              |
| ------------------------- | ---------------------------------- |
| `No space left on device` | Disk is full                       |
| `umount: target is busy`  | Files are still being used         |
| Device not found          | Incorrect device name              |
| Permission denied         | Administrative privileges required |

---

# Summary

You should now understand how to inspect storage devices, monitor disk usage, and safely mount or unmount filesystems.

---

# Related Chapters

* Files & Directories
* Processes
* Security
