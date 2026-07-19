# Navigation and File Management

## Overview

Navigating the Linux file system is a fundamental skill for system administrators and cybersecurity professionals. Analysts frequently use these commands to locate logs, configuration files, user directories, and evidence during security investigations.

---

# Why It Matters

Security analysts routinely work from remote Linux systems without a graphical interface. Understanding how to efficiently navigate the filesystem and inspect files is essential when:

- Investigating security incidents
- Reviewing log files
- Examining user accounts
- Finding configuration files
- Collecting forensic evidence

---

# pwd

Displays the current working directory.

### Syntax

```bash
pwd
```

Example Output

```
/home/analyst
```

---

# ls

Lists the contents of the current directory.

### Syntax

```bash
ls
```

Example Output

```
logs
projects
reports
temp
```

Common options

```bash
ls -l
ls -a
ls -lh
```

---

# cd

Changes the current directory.

### Relative Path

```bash
cd reports
```

### Absolute Path

```bash
cd /home/analyst/reports
```

Examples

```bash
cd ..

cd ~

cd /
```

---

# cat

Displays the contents of a file.

### Syntax

```bash
cat Q1_added_users.txt
```

Example

```bash
cat /home/analyst/reports/users/Q1_added_users.txt
```

Common Uses

- Read log files
- View configuration files
- Examine reports
- Review user information

---

# head

Displays the beginning of a file.

### Syntax

```bash
head server_logs.txt
```

Display first five lines

```bash
head -n 5 server_logs.txt
```

Common Uses

- Preview large log files
- Verify file contents
- Quickly inspect reports

---

# Lab Summary

During this lab I practiced:

- Determining the current working directory
- Navigating directories using relative and absolute paths
- Listing directory contents
- Reading file contents
- Viewing the beginning of log files

Commands practiced:

- `pwd`
- `ls`
- `cd`
- `cat`
- `head`

---

# Practical Cybersecurity Uses

These commands are frequently used by security analysts when:

- Investigating security incidents
- Reviewing authentication logs
- Examining configuration files
- Reading system reports
- Collecting forensic evidence
- Navigating remote Linux systems over SSH

---

# Key Takeaways

- `pwd` displays the current working directory.
- `ls` lists files and directories.
- `cd` changes directories.
- `cat` displays complete file contents.
- `head` previews the beginning of a file.
