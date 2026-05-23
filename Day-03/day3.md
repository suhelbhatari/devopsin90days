# Day 03 – User Management in Linux 👤

## Why User Management Matters?

| Topic                  | Explanation                            |
| ---------------------- | -------------------------------------- |
| Security               | Controls user access to the system     |
| Multi-User Environment | Multiple users can work simultaneously |
| System Integrity       | Prevents unauthorized changes          |

---

# Important User Management Files

| File           | Purpose                     |
| -------------- | --------------------------- |
| `/etc/passwd`  | Stores user account details |
| `/etc/shadow`  | Stores encrypted passwords  |
| `/etc/group`   | Stores group information    |
| `/etc/gshadow` | Secure group details        |

---

# Creating Users

| Command                         | Description                              |
| ------------------------------- | ---------------------------------------- |
| `useradd username`              | Create user without home directory       |
| `useradd -m username`           | Create user with home directory          |
| `useradd -s /bin/bash username` | Create user with Bash shell              |
| `adduser username`              | Interactive user creation (Debian-based) |

---

# Managing Passwords

| Command                | Purpose                |
| ---------------------- | ---------------------- |
| `passwd username`      | Set or change password |
| `chage -M 90 username` | Set password expiry    |
| `passwd -l username`   | Lock user account      |
| `passwd -u username`   | Unlock user account    |

---

# Modifying Users

| Command                            | Description           |
| ---------------------------------- | --------------------- |
| `usermod -l new old`               | Change username       |
| `usermod -d /new/home -m username` | Change home directory |
| `usermod -s /bin/zsh username`     | Change default shell  |

---

# Deleting Users

| Command               | Description                     |
| --------------------- | ------------------------------- |
| `userdel username`    | Delete user only                |
| `userdel -r username` | Delete user with home directory |

---

# Group Management

| Command                          | Purpose              |
| -------------------------------- | -------------------- |
| `groupadd groupname`             | Create new group     |
| `usermod -aG groupname username` | Add user to group    |
| `groups username`                | View user groups     |
| `usermod -g group username`      | Change primary group |

---

# Sudo Access & Privilege Escalation

| Command                      | Purpose                         |
| ---------------------------- | ------------------------------- |
| `usermod -aG sudo username`  | Add user to sudo group (Debian) |
| `usermod -aG wheel username` | Add user to wheel group (RHEL)  |
| `visudo`                     | Edit sudoers file securely      |

### Example sudoers Entry

```bash id="l1m4q9"
username ALL=(ALL) NOPASSWD: /path/to/command
```

---

# Useful Daily Commands

| Command           | Purpose                |
| ----------------- | ---------------------- |
| `whoami`          | Show current user      |
| `id`              | Display UID and groups |
| `sudo -l`         | Check sudo permissions |
| `groups`          | Show group memberships |
| `cat /etc/passwd` | View user accounts     |

---

# Key Learning

| Topic          | Learning                                        |
| -------------- | ----------------------------------------------- |
| User Accounts  | Essential for secure system access              |
| Groups         | Simplify permission management                  |
| Sudo           | Provides controlled administrative access       |
| Linux Security | Strong user management improves system security |
