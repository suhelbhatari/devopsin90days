# Day 01 – Linux Internals & Boot Process 🐧

## Starting Linux Again from Scratch

* Today I restarted learning Linux from scratch to build a stronger DevOps foundation.
* Strong Linux fundamentals are essential for troubleshooting servers, automation, containers, and cloud systems.

## Why Linux is Best for DevOps?

* Most cloud servers run Linux
* Powerful CLI and automation support
* Lightweight and stable for production systems
* Best ecosystem for Docker, Kubernetes, and DevOps tools
* Open-source and highly customizable

## Linux OS Architecture

```text id="h9n3xw"
+----------------------+
|    User Applications |
+----------------------+
|      User Space      |
| Shell | Libraries    |
+----------------------+
|        Kernel        |
| Process | Memory     |
| Drivers | Network    |
+----------------------+
|       Hardware       |
+----------------------+
```

## Linux Boot Process (In Depth)

### 1. BIOS / UEFI

* Initializes hardware components
* Performs POST (Power-On Self Test)
* Finds bootable device

### 2. Bootloader (GRUB)

* Loads Linux kernel into memory
* Provides OS selection menu

### 3. Linux Kernel

* Initializes CPU, memory, drivers
* Mounts root filesystem
* Starts first process

### 4. init / systemd (PID 1)

* First userspace process
* Starts system services and daemons
* Handles dependencies and startup sequence

### 5. User Space & Services

* Login screen starts
* Applications and background services become available

## Boot Process Diagram

```text id="l11q8n"
Power ON
   ↓
BIOS / UEFI
   ↓
GRUB Bootloader
   ↓
Linux Kernel
   ↓
systemd (PID 1)
   ↓
Services & User Space
   ↓
User Login
```

## Process Management

* Every running program is a process with a unique PID
* Created using `fork()` and executed using `exec()`
* Linux scheduler manages CPU allocation

## Common Process States

* **Running (R)** → Currently executing
* **Sleeping (S)** → Waiting for resource/event
* **Stopped (T)** → Paused process
* **Zombie (Z)** → Finished but waiting for cleanup

## Why systemd Matters

* Controls boot process
* Manages services and dependencies
* Handles logging and startup performance

## 5 Daily Linux Commands

```bash id="2h08qs"
ps aux
top
systemctl status nginx
journalctl -xe
kill -9 PID
```
