# 🏛️ POSIX Compliance Tracking  
📌 **Tracking Guacamole/GNU’s progress toward POSIX.1-2024 compliance.**  

## 📊 Compliance Status  

| Component               | Implemented? | Notes |
|-------------------------|-------------|-------|
| **System Calls**        | ❌ No       | See [`system_calls.md`](system_calls.md) |
| **Files & Directories** | ❌ No       | File system operations |
| **Process Control**     | ❌ No       | Process creation, termination, signals |
| **Memory Management**   | ❌ No       | `mmap`, `brk`, `sbrk` |
| **Threads & IPC**       | ❌ No       | `pthread`, pipes, sockets, shared memory |
| **Signals & Timers**    | ❌ No       | `signal`, `alarm`, `setitimer` |
| **Networking**          | ❌ No       | BSD sockets support |
| **File Permissions**    | ❌ No       | `chmod`, `chown`, `umask` |
| **Device I/O**          | ❌ No       | `ioctl`, `/dev` interface |
| **Shell & Utilities**   | ✅ GNU     | Handled by GNU userland |
| **POSIX Headers**       | ❌ No       | Required headers in `include/` |
| **System Configuration**| ❌ No       | `sysconf`, `pathconf` |

---

## 📜 **POSIX Feature Breakdown**  
### **🔹 System Interfaces (`XSH`)**
| Feature                 | Implemented? | Notes |
|-------------------------|-------------|-------|
| `unistd.h`              | ❌ No       | Core system calls |
| `sys/types.h`           | ❌ No       | Common data types |
| `sys/stat.h`            | ❌ No       | File metadata |
| `fcntl.h`               | ❌ No       | File control options |
| `signal.h`              | ❌ No       | Signal handling |
| `pthread.h`             | ❌ No       | Threading support |
| `sys/mman.h`            | ❌ No       | Memory management |

### **🔹 Shell & Utilities (`XCU`)**
| Utility      | Provided? | Notes |
|-------------|-----------|-------|
| `sh`        | ✅ GNU    | Bash provided by GNU |
| `ls`        | ✅ GNU    | GNU coreutils |
| `grep`      | ✅ GNU    | GNU grep |
| `awk`       | ✅ GNU    | GNU awk |
| `sed`       | ✅ GNU    | GNU sed |

---

### **📌 How to Contribute**  
- **Update this list as features are implemented.**  
- **For system calls, check [`system_calls.md`](system_calls.md).**  

---

### **📌 Next Steps**  
✅ **Initial compliance list structured**  
➡️ **Time to expand `docs/dev/coding_guidelines.md` next!** 🚀  
