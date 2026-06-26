# Processes

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner
> **Prerequisites:** Users

Every program running on a Linux system is a process. Understanding how to view, monitor, and stop processes is an essential skill for troubleshooting, system administration, and cybersecurity.

---

## What You'll Learn

* Viewing running processes
* Monitoring system resources
* Terminating processes
* Identifying resource usage

---

# Process Commands

---

## ps

### Purpose

Displays information about running processes.

### Syntax

```bash
ps [OPTIONS]
```

### Examples

```bash
ps

ps aux

ps -ef
```

### Common Uses

* View running processes.
* Find a process ID (PID).
* Troubleshoot applications.

### Cybersecurity Context

Useful during investigations to identify suspicious or unexpected processes.

### Related Commands

* `top`
* `htop`
* `kill`

---

## top

### Purpose

Displays a live view of running processes and system resource usage.

### Syntax

```bash
top
```

### Common Uses

* Monitor CPU usage.
* Monitor memory usage.
* Identify resource-intensive processes.

### Cybersecurity Context

Useful for detecting unusual CPU or memory consumption that may indicate malware or compromised services.

### Related Commands

* `htop`
* `ps`

---

## htop

### Purpose

Provides an interactive and user-friendly process viewer.

### Syntax

```bash
htop
```

### Common Uses

* Monitor processes.
* Sort by CPU or memory usage.
* Terminate processes interactively.

### Cybersecurity Context

Makes it easier to identify suspicious processes during incident response.

### Related Commands

* `top`

---

## kill

### Purpose

Terminates a process using its Process ID (PID).

### Syntax

```bash
kill PID
```

### Examples

```bash
kill 1234

kill -9 1234
```

### Common Uses

* Stop unresponsive applications.
* Terminate unwanted processes.

### Cybersecurity Context

Useful when stopping malicious or compromised processes during investigations.

### Related Commands

* `killall`

---

## killall

### Purpose

Terminates processes by name.

### Syntax

```bash
killall PROCESS_NAME
```

### Examples

```bash
killall firefox

killall python3
```

### Common Uses

* Stop multiple instances of an application.
* Quickly terminate a known process.

### Cybersecurity Context

Helpful when stopping unwanted services or scripts by process name.

### Related Commands

* `kill`

---

# Common Mistakes

| Problem                 | Cause                                       |
| ----------------------- | ------------------------------------------- |
| Process won't terminate | Incorrect PID or insufficient permissions   |
| `kill` has no effect    | Process ignores the signal or requires `-9` |
| `htop` not found        | Package not installed                       |

---

# Summary

You should now understand how to view, monitor, and terminate processes in Linux. These commands are frequently used when troubleshooting systems and investigating suspicious activity.

---

# Related Chapters

* Users
* Networking
* Security
