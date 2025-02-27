# Guacamole/GNU System Calls  
📌 **Tracking POSIX compliance & custom system calls**  

## 📊 System Call Implementation Status  

| Name         | Implemented? | Notes |
|-------------|-------------|-------|
| `fork`      | ❌ No       | Process creation |
| `execve`    | ❌ No       | Execute a program |
| `exit`      | ❌ No       | Terminate a process |
| `waitpid`   | ❌ No       | Wait for a process to change state |
| `kill`      | ❌ No       | Send signals to processes |
| `open`      | ❌ No       | Open a file |
| `close`     | ❌ No       | Close a file descriptor |
| `read`      | ❌ No       | Read from a file descriptor |
| `write`     | ❌ No       | Write to a file descriptor |
| `mmap`      | ❌ No       | Map files into memory |
| `munmap`    | ❌ No       | Unmap memory regions |
| `ioctl`     | ❌ No       | Device control operations |
| `getpid`    | ❌ No       | Get process ID |
| `getppid`   | ❌ No       | Get parent process ID |
| `brk`       | ❌ No       | Adjust heap memory |
| `sbrk`      | ❌ No       | Manage heap growth |
| `chdir`     | ❌ No       | Change working directory |
| `getcwd`    | ❌ No       | Get current working directory |
| `stat`      | ❌ No       | Get file metadata |
| `fstat`     | ❌ No       | Get file metadata by descriptor |
| `dup`       | ❌ No       | Duplicate a file descriptor |
| `dup2`      | ❌ No       | Duplicate a file descriptor to a specific FD |
| `pipe`      | ❌ No       | Create an interprocess pipe |
| `socket`    | ❌ No       | Create a network socket |
| `connect`   | ❌ No       | Connect to a socket |
| `bind`      | ❌ No       | Bind a socket to an address |
| `listen`    | ❌ No       | Mark a socket as passive |
| `accept`    | ❌ No       | Accept a connection on a socket |
| `send`      | ❌ No       | Send data on a socket |
| `recv`      | ❌ No       | Receive data on a socket |
| `shutdown`  | ❌ No       | Shut down socket communication |
| `reboot`    | ❌ No       | Reboot the system |
| `mount`     | ❌ No       | Mount a filesystem |
| `umount`    | ❌ No       | Unmount a filesystem |

---

## 🔧 **Custom System Calls (Guacamole-Specific)**
| Name         | Implemented? | Notes |
|-------------|-------------|-------|
| `guac_debug` | ❌ No       | Custom debug logging |
| `guac_lkm`   | ❌ No       | Load/unload kernel modules |

---

### **📌 How to Contribute**  
- **Add new system calls** to this list when planned.  
- **Mark them ✅ when implemented** (or add notes if partially done).  

---