# 🛠️ Guacamole/GNU Coding Guidelines  

📌 **Standardized coding practices for kernel development.**  

---

## 📝 **1. General Coding Style**  

✅ **Follow the GNU Coding Standards**  
- Use **K&R-style braces**, but with GNU indentation.  
- Use **spaces instead of tabs** (4 spaces per indentation level).  
- Keep **lines under 80 characters** when possible.  
- Use **snake_case** for variable names (`kernel_buffer`).  
- Use **PascalCase** for struct and type names (`TaskStruct`).  
- **Avoid magic numbers**; use `#define` or `const` values instead.  
- Use **descriptive comments** for complex logic.  

```c
/* ✅ Good */
#define MAX_TASKS 128  // Maximum number of tasks

/* ❌ Bad */
int max = 128;
```

---

## 📌 **2. File Organization**  

✅ **Follow a clear file structure:**  

```
.
├── src/           # Kernel source code
│   ├── arch/      # Architecture-specific code
│   ├── drivers/   # Device drivers
│   ├── fs/        # Filesystem support
│   ├── mm/        # Memory management
│   ├── sched/     # Scheduler
│   └── sys/       # System calls
├── include/       # Header files
├── docs/          # Documentation
├── tests/         # Unit tests & integration tests
```

Each source file should have a **header with license information and purpose**:  

```c
/*
 * my_file.c - Example Kernel Module
 * Part of Guacamole/GNU Kernel
 * (C) 2025 TacosAreGoodForProgrammers, Licensed under GPLv3
 */
```

---

## 🏷️ **3. Naming Conventions**  

- **Functions**: `module_function_name()`
- **Variables**: `snake_case`
- **Constants**: `ALL_CAPS`
- **Structs/Types**: `PascalCase`

Example:  

```c
struct TaskStruct {
    int task_id;
    char task_name[32];
};
```

---

## 🔄 **4. Commit & Git Guidelines**  

✅ **Commit Messages Format**  
- Use present tense (`Fix bug`, not `Fixed bug`).  
- Keep the first line under 50 characters.  
- Separate detailed explanations with a blank line.  

✅ **Example:**  

```
[MM] Implement basic page allocator

Added a simple first-fit page allocator in mm/page_alloc.c.
TODO: Implement buddy system for better fragmentation handling.
```

✅ **Branch Naming:**  

- **`feature/xyz`** for new features  
- **`bugfix/xyz`** for bug fixes  
- **`doc/xyz`** for documentation changes  

---

## ⚠️ **5. Error Handling**  

✅ **Use POSIX error codes (`errno`)**  
- Return `-EINVAL` for invalid arguments.  
- Return `-ENOMEM` for memory allocation failures.  

```c
if (!ptr) {
    return -ENOMEM;
}
```

---

## 🚀 **6. Performance Considerations**  

✅ **Avoid unnecessary heap allocations.**  
✅ **Use inline functions for small, frequently called operations.**  
✅ **Minimize global variables to avoid race conditions.**  

---

## 📜 **7. Licensing & Headers**  

✅ **All code must include a GPLv3 header.**  
✅ **Use SPDX license identifiers in every file:**  

```c
// SPDX-License-Identifier: GPL-3.0-or-later
```

---

## ✨ **8. How to Contribute**  

1. **Follow these guidelines** when writing code.  
2. **Ensure your code builds and passes tests** before pushing.  
3. **Submit a pull request** with a detailed description.  
4. **Be nice and review others' PRs!** 
**If you contribute to a file, add your name and what you worked on in [CONTRIBUTORS.md](../../CONTRIBUTORS.md) before submitting a PR.**  


---

## ✅ **Final Notes**  
- Keep code **clean, readable, and maintainable**.  
- Follow **POSIX compliance** wherever possible.  
- **If unsure, ask in discussions or open an issue.**  

---

🚀 **Happy hacking, and welcome to the Guacamole/GNU project!**  
