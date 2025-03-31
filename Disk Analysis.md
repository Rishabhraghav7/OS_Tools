# `du` vs `dust` in Linux

## **`du` (Disk Usage)**
- **Command:** `du [options] [directory/file]`
- **Purpose:** Shows disk usage of files and directories.
- **Basic Usage:**  
  ```bash
  du -sh /home/user
  ```
  - `-s` → Summarize total size  
  - `-h` → Human-readable format  

- **Common Options:**  
  ```bash
  du -ah  # Show sizes of all files and directories
  du -c   # Show total size
  du -d 1 /path  # Limit depth to level 1
  du --max-depth=2 /path  # Limit depth to level 2
  du -k /path  # Output in kilobytes
  du -m /path  # Output in megabytes
  du -b /path  # Output in bytes
  du -x /path  # Stay within one file system
  du -t 100M /path  # Show only files larger than 100MB
  du --exclude="*.log" /path  # Exclude certain files
  ```

- **Performance Optimization:**  
  ```bash
  du -sh /path 2>/dev/null  # Suppress permission errors
  du -sh * | sort -hr  # Sort by size
  ```

- **Use Cases:**
  - Checking which directories are taking up space.
  - Summarizing disk usage for analysis.

---

## **`dust` (du + Rust)**
- **Command:** `dust [options] [directory]`
- **Purpose:** A faster, modern `du` alternative.
- **Installation:**  
  ```bash
  sudo pacman -S dust  # Arch
  sudo apt install dust  # Debian/Ubuntu
  ```

- **Basic Usage:**  
  ```bash
  dust /home/user
  ```
  - Auto-sorts by size.
  - Uses colorized output.
  - Displays in a tree format.

- **Performance:**  
  - **Faster** than `du` (multi-threaded Rust-based).
  - **Better UI** (graphical representation of disk usage).

- **Comparison (`du` vs `dust`):**

  | Feature     | `du`  | `dust` |
  |------------|------|------|
  | Speed      | Slower | Faster (multi-threaded) |
  | Readability | Plain text | Colorized, tree-based |
  | Sorting    | Manual (`sort -hr`) | Automatic |
  | Pre-installed | Yes | No (needs installation) |

- **Use Cases:**
  - Quickly analyzing large directories.
  - More user-friendly and intuitive output.

---
## **When to Use What?**
- **Need pre-installed, basic disk usage check?** → Use `du`
- **Want faster, more readable output?** → Use `dust`