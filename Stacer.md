# Stacer in Linux - Mini Cheat Sheet

## Description

**Stacer** is an open-source system optimizer and monitoring tool for Linux. It provides an intuitive GUI to manage system resources, startup applications, services, and more.

## Installation

### Debian/Ubuntu

```bash
sudo apt update && sudo apt install stacer -y
```

### Arch Linux

```bash
sudo pacman -S stacer
```

### Fedora

```bash
sudo dnf install stacer
```

### AppImage (Universal)

```bash
wget https://github.com/oguzhaninan/Stacer/releases/download/v1.1.0/Stacer-1.1.0-x64.AppImage
chmod +x Stacer-1.1.0-x64.AppImage
./Stacer-1.1.0-x64.AppImage
```

## Features & Usage

### Launch Stacer

```bash
stacer
```

### System Monitoring

- View CPU, RAM, and Disk usage.
    
- Monitor network activity.
    

### Startup Applications

- Manage programs that launch on startup.
    

### System Cleaner

- Remove cache, logs, and package leftovers.
    

### Services & Processes

- Start, stop, and manage system services.
    
- Kill or monitor running processes.
    

### Uninstaller

- Remove installed packages easily.
    

### APT Repository Manager

- Enable/disable software repositories.
    

## Uninstall Stacer

### Debian/Ubuntu

```bash
sudo apt remove --purge stacer -y
```

### Arch Linux

```bash
sudo pacman -Rns stacer
```

### Fedora

```bash
sudo dnf remove stacer
```

## Conclusion

Stacer is a powerful tool for Linux users who prefer a GUI-based system optimizer. It simplifies system management, making tasks like cleaning, monitoring, and startup application control easier.