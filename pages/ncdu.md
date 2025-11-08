# 🧰 Disk Analysis Tools Cheat Sheet (Linux)

A complete guide for analyzing and managing disk usage with:
- `ncdu` (interactive analyzer)
- `du` (disk usage)
- `df` (disk free space)
- `lsblk` (block devices)

---

## 🧮 ncdu – NCurses Disk Usage

A terminal-based disk usage analyzer with interactive navigation.

### 📦 Installation

| OS | Command |
|----|----------|
| Debian/Ubuntu | `sudo apt install ncdu` |
| Fedora | `sudo dnf install ncdu` |
| Arch Linux | `sudo pacman -S ncdu` |
| macOS | `brew install ncdu` |

---

### 🚀 Usage

| Command | Description |
|----------|-------------|
| `ncdu` | Scan current directory |
| `ncdu /path/to/dir` | Scan a specific directory |
| `sudo ncdu /` | Scan entire filesystem |
| `ncdu -x /` | Stay on one filesystem |
| `ncdu -r` | Read-only mode (no delete) |
| `ncdu -q` | Quiet mode (less verbose) |

---

### 🧭 Navigation

| Key | Action |
|-----|---------|
| ↑ / ↓ | Move selection up/down |
| ← | Go up (parent directory) |
| → / Enter | Enter selected directory |
| `n` | Sort by name |
| `s` | Sort by size |
| `C` | Sort by item count |
| `a` | Toggle apparent/disk usage |
| `d` | Delete selected file/folder |
| `g` | Toggle graph view |
| `r` | Refresh directory |
| `q` | Quit ncdu |

---

### ⚙️ Options

| Option | Description |
|--------|-------------|
| `-x` | Stay on one filesystem |
| `-r` | Read-only (no deletes) |
| `--exclude PATTERN` | Exclude pattern |
| `--exclude-from FILE` | Read excludes from file |
| `-o FILE` | Export scan to file |
| `-f FILE` | Import scan from file |
| `-e` | Extended info |
| `--color dark` | Dark color theme |

---

### 💾 Export / Import

```bash
ncdu -o output.json /
ncdu -f output.json
