## General Commands

![header](/images/terminal%20commands%20cheat%20sheet.png)

---

### Table of Contents

- [**1. Navigation**](#1-navigation)
- [**2. File Operations**](#2-file-operations)
- [**3. System Information**](#3-system-information)
- [**4. Network Operations**](#4-network-operations)
- [**5. Disk Operations**](#5-disk-operations)
- [**6. Text Editing**](#6-text-editing)
- [**7. User Management**](#7-user-management)
- [**8. Permissions**](#8-permissions)
- [**9. Searching**](#9-searching)
- [**10. Miscellaneous**](#10-miscellaneous)

---

### **1. Navigation**
| Task                       | Windows         | macOS/Linux   |
| -------------------------- | --------------- | ------------- |
| List files and directories | `dir`           | `ls`          |
| Change directory           | `cd <folder>`   | `cd <folder>` |
| Go to home directory       | `cd`            | `cd ~`        |
| Go up one directory level  | `cd ..`         | `cd ..`       |
| Print current directory    | `cd` or `chdir` | `pwd`         |

### **2. File Operations**
| Task                  | Windows                       | macOS/Linux                   |
| --------------------- | ----------------------------- | ----------------------------- |
| Copy file             | `copy <source> <destination>` | `cp <source> <destination>`   |
| Move file             | `move <source> <destination>` | `mv <source> <destination>`   |
| Rename file           | `rename <oldname> <newname>`  | `mv <oldname> <newname>`      |
| Delete file           | `del <file>`                  | `rm <file>`                   |
| Delete directory      | `rmdir <folder>`              | `rm -r <folder>`              |
| Create directory      | `mkdir <folder>`              | `mkdir <folder>`              |
| Display file contents | `type <file>`                 | `cat <file>` or `less <file>` |

### **3. System Information**
| Task                      | Windows               | macOS/Linux          |
| ------------------------- | --------------------- | -------------------- |
| Display IP address        | `ipconfig`            | `ifconfig` or `ip a` |
| Display running processes | `tasklist`            | `ps aux`             |
| Kill process              | `taskkill /PID <pid>` | `kill <pid>`         |
| System information        | `systeminfo`          | `uname -a`           |

### **4. Network Operations**
| Task          | Windows                                | macOS/Linux                     |
| ------------- | -------------------------------------- | ------------------------------- |
| Ping a server | `ping <address>`                       | `ping <address>`                |
| Trace route   | `tracert <address>`                    | `traceroute <address>`          |
| Download file | Use `curl` or `wget` (3rd party tools) | `curl -O <url>` or `wget <url>` |

### **5. Disk Operations**
| Task                     | Windows  | macOS/Linux |
| ------------------------ | -------- | ----------- |
| Check disk usage         | `chkdsk` | `df -h`     |
| Display disk space usage | `dir`    | `du -sh`    |
| Format a drive           | `format` | `mkfs`      |

### **6. Text Editing**
| Task           | Windows          | macOS/Linux                  |
| -------------- | ---------------- | ---------------------------- |
| Edit text file | `notepad <file>` | `nano <file>` or `vi <file>` |

### **7. User Management**
| Task        | Windows                               | macOS/Linux               |
| ----------- | ------------------------------------- | ------------------------- |
| List users  | `net user`                            | `cat /etc/passwd`         |
| Add user    | `net user <username> <password> /add` | `sudo adduser <username>` |
| Delete user | `net user <username> /delete`         | `sudo deluser <username>` |

### **8. Permissions**
| Task                    | Windows             | macOS/Linux                  |
| ----------------------- | ------------------- | ---------------------------- |
| Change file permissions | `icacls <file>`     | `chmod <permissions> <file>` |
| Change file owner       | `takeown /f <file>` | `chown <owner> <file>`       |

### **9. Searching**
| Task                     | Windows                    | macOS/Linux               |
| ------------------------ | -------------------------- | ------------------------- |
| Search for a file        | `dir /s <filename>`        | `find / -name <filename>` |
| Search for text in files | `findstr <pattern> <file>` | `grep <pattern> <file>`   |

### **10. Miscellaneous**
| Task                  | Windows           | macOS/Linux |
| --------------------- | ----------------- | ----------- |
| Clear terminal screen | `cls`             | `clear`     |
| History of commands   | `doskey /history` | `history`   |

---

This cheat sheet covers basic commands, but each operating system has many more commands and options for more advanced tasks.
