# Navigation and File Management

## Overview

Managing files and directories is one of the most fundamental skills in Linux. Security analysts routinely create, organize, move, inspect, and remove files while investigating security incidents, reviewing logs, managing scripts, and collecting forensic evidence.

Understanding how to efficiently navigate and manage the Linux file system is essential when working remotely through a terminal without a graphical user interface.

---

# Why It Matters

Linux file management is used daily in cybersecurity to:

- Organize investigation artifacts
- Review and collect log files
- Manage scripts and automation tools
- Navigate remote systems through SSH
- Locate configuration files
- Collect and preserve forensic evidence
- Maintain an organized working environment

---

# Current Working Directory (`pwd`)

Displays the full path of the current working directory.

### Syntax

```bash
pwd
```

### Example

```bash
pwd
```

Output:

```text
/home/analyst
```

### Common Uses

- Confirm your current location before making changes
- Verify working directories during investigations
- Avoid modifying the wrong files or directories

---

# Listing Directory Contents (`ls`)

Lists files and directories within the current directory.

### Syntax

```bash
ls
```

### Example

```bash
ls
```

Output:

```text
logs
notes
reports
temp
```

### Useful Options

```bash
ls -l      # Long listing format
ls -a      # Show hidden files
ls -lh     # Human-readable file sizes
```

### Common Uses

- View directory contents
- Verify files exist
- Confirm successful file operations

---

# Changing Directories (`cd`)

Changes the current working directory.

### Relative Path

```bash
cd reports
```

### Absolute Path

```bash
cd /home/analyst/reports
```

### Additional Examples

```bash
cd ..
```

Move up one directory.

```bash
cd ~
```

Return to the user's home directory.

```bash
cd /
```

Navigate to the root directory.

### Common Uses

- Navigate remote Linux systems
- Access log directories
- Locate configuration files
- Browse forensic evidence

---

# Creating Directories (`mkdir`)

Creates a new directory.

### Syntax

```bash
mkdir logs
```

### Example

```bash
mkdir investigations
```

### Common Uses

- Organize investigation files
- Store log collections
- Create project directories
- Separate evidence by incident

---

# Removing Directories (`rmdir`)

Removes an empty directory.

### Syntax

```bash
rmdir temp
```

### Common Uses

- Remove unused directories
- Clean up lab environments
- Maintain organized file structures

> **Note:** `rmdir` only removes empty directories.

---

# Creating Files (`touch`)

Creates an empty file or updates the timestamp of an existing file.

### Syntax

```bash
touch tasks.txt
```

### Common Uses

- Create notes
- Create scripts
- Create configuration files
- Prepare documentation

---

# Moving and Renaming Files (`mv`)

Moves or renames files and directories.

### Syntax

Move a file:

```bash
mv Q3patches.txt /home/analyst/reports/
```

Rename a file:

```bash
mv report.txt incident-report.txt
```

### Common Uses

- Organize investigation artifacts
- Rename reports
- Archive logs
- Move evidence into project folders

---

# Removing Files (`rm`)

Deletes files.

### Syntax

```bash
rm tempnotes.txt
```

### Common Uses

- Remove temporary files
- Delete obsolete scripts
- Clean lab environments

> **Warning:** Files deleted with `rm` cannot be recovered through the Linux Recycle Bin.

---

# Reading Files (`cat`)

Displays the contents of a file.

### Syntax

```bash
cat tasks.txt
```

### Example

```bash
cat /home/analyst/reports/Q3patches.txt
```

### Common Uses

- Read log files
- Review configuration files
- Examine reports
- Verify file contents

---

# Viewing File Headers (`head`)

Displays the beginning of a file.

### Syntax

```bash
head server_logs.txt
```

Display a specific number of lines:

```bash
head -n 5 server_logs.txt
```

### Common Uses

- Preview large log files
- Inspect reports
- Verify downloaded files

---

# Editing Files (`nano`)

A simple command-line text editor commonly available on Linux systems.

### Open a File

```bash
nano tasks.txt
```

### Basic Keyboard Shortcuts

| Shortcut | Action |
|-----------|--------|
| `Ctrl + O` | Save file |
| `Ctrl + X` | Exit Nano |
| `Ctrl + K` | Cut current line |
| `Ctrl + U` | Paste line |
| `Ctrl + W` | Search within file |

### Common Uses

- Edit configuration files
- Update documentation
- Modify scripts
- Create notes

---

# Lab Summary

During this lab, I practiced:

- Creating directories
- Removing directories
- Creating files
- Moving files
- Removing files
- Editing files with Nano
- Reading file contents
- Navigating Linux directories

### Commands Practiced

```text
pwd
ls
cd
mkdir
rmdir
touch
mv
rm
cat
head
nano
```

---

# Practical Cybersecurity Uses

These commands are frequently used when:

- Investigating security incidents
- Collecting forensic evidence
- Managing log files
- Organizing investigation artifacts
- Editing system configuration files
- Maintaining Linux servers
- Managing automation scripts
- Navigating remote systems over SSH

---

# Key Takeaways

- `pwd` displays the current working directory.
- `ls` lists directory contents.
- `cd` changes directories.
- `mkdir` creates directories.
- `rmdir` removes empty directories.
- `touch` creates new files.
- `mv` moves or renames files.
- `rm` deletes files.
- `cat` displays file contents.
- `head` previews the beginning of files.
- `nano` provides a simple command-line text editor for modifying files.

---

# Skills Practiced

- Linux File System Navigation
- File Management
- Directory Management
- Command-Line Operations
- File Editing
- Terminal Productivity
- Linux Administration Fundamentals
