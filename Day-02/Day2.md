# Day 02 – Linux Folder Structure 📂

## Why Folder Structure Matters?

* Linux organizes everything as files and directories.
* Understanding folders helps in troubleshooting, configuration, logging, and server management.

---

# Symbolic Links (Less Significant)

| Directory            | Description                         |
| -------------------- | ----------------------------------- |
| `/sbin -> /usr/sbin` | Administrative system binaries      |
| `/bin -> /usr/bin`   | Essential user commands             |
| `/lib -> /usr/lib`   | Shared libraries and kernel modules |

---

# Important System Directories

| Directory | Description                           |
| --------- | ------------------------------------- |
| `/boot`   | Files required for booting Linux      |
| `/usr`    | Applications, binaries, libraries     |
| `/var`    | Logs, cache, frequently changing data |
| `/etc`    | System configuration files            |

---

# User & Application Directories

| Directory | Description                   |
| --------- | ----------------------------- |
| `/home`   | User home directories         |
| `/opt`    | Optional third-party software |
| `/srv`    | Service-related data          |
| `/root`   | Home directory of root user   |

---

# Temporary & Virtual Directories

| Directory | Description                     |
| --------- | ------------------------------- |
| `/tmp`    | Temporary files                 |
| `/run`    | Runtime process data            |
| `/proc`   | Process and system information  |
| `/sys`    | Hardware and kernel information |
| `/dev`    | Device files                    |

---

# Mount Points

| Directory | Description              |
| --------- | ------------------------ |
| `/mnt`    | Temporary mount location |
| `/media`  | USB/CD mount point       |
| `/data`   | Custom mounted storage   |

---

# Useful Commands

```bash id="o4d8ku"
pwd          # Show current directory
ls -la       # List files and permissions
cd           # Change directory
tree         # View folder structure
df -h        # Disk usage information
```

## Key Learning

* `/etc` is critical for configuration management.
* `/var/log` is heavily used for troubleshooting.
* `/proc` and `/sys` provide live system information.
* Linux filesystem knowledge is essential for DevOps and system administration.
