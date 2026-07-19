# Searching and Filtering

## Overview

Searching and filtering are essential Linux skills that allow administrators and security analysts to quickly locate files, identify relevant information, and analyze logs. These commands become especially valuable when investigating security events or reviewing large datasets.

---

## Why It Matters

Security analysts routinely search through thousands of log entries, configuration files, and user records. Efficient searching reduces investigation time and improves incident response.

Common use cases include:

- Investigating authentication failures
- Identifying malicious IP addresses
- Reviewing application logs
- Finding configuration files
- Locating compromised user accounts

---

# grep

Searches files for matching text.

### Syntax

```bash
grep "pattern" filename
```

Example

```bash
grep error server_logs.txt
```

Example Output

```
error: failed login
error: invalid request
```

Common Uses

- Search logs
- Find usernames
- Locate IP addresses
- Search configuration files

---

# Piping

The pipe operator (`|`) sends the output of one command as input to another.

Example

```bash
ls | grep Q1
```

Example

```bash
ls | grep access
```

Common Uses

- Filter command output
- Combine Linux commands
- Reduce unnecessary output

---

# Lab Summary

Commands practiced:

- `grep`
- `ls`
- `cd`
- `|` (pipe)

Activities completed:

- Located error messages in server logs
- Filtered filenames using grep
- Searched user reports
- Identified deleted users
- Located Human Resources employees

---

# Practical Cybersecurity Uses

These commands are commonly used to:

- Search authentication logs
- Investigate failed login attempts
- Identify compromised accounts
- Filter large datasets
- Review firewall logs
- Examine SIEM exports

---

# Key Takeaways

- `grep` searches files for matching text.
- Pipes combine multiple commands into a single workflow.
- Filtering allows analysts to quickly isolate relevant information.
- These commands are essential for Linux administration and cybersecurity investigations.
