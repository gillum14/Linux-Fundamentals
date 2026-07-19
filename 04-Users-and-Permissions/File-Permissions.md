# Users and Permissions

## Overview

Linux permissions determine who can read, write, and execute files and directories. Proper permission management is a fundamental security practice that helps prevent unauthorized access, protect sensitive data, and enforce the principle of least privilege.

Understanding file permissions is essential for system administrators and cybersecurity professionals responsible for securing Linux systems.

---

# Why It Matters

Misconfigured permissions are a common cause of security incidents. Improper authorization can allow unauthorized users to:

- View sensitive information
- Modify critical system files
- Execute malicious code
- Escalate privileges
- Compromise system integrity

Security analysts regularly audit and modify permissions to reduce organizational risk.

---

# Viewing Permissions

Display files using the long listing format.

```bash
ls -l
```

Example Output

```text
-rw-rw-r-- 1 researcher2 research_team project_r.txt
```

Display hidden files as well.

```bash
ls -la
```

---

# Understanding Permission Strings

Example:

```text
-rw-rw-r--
```

| Position | Meaning |
|----------|---------|
| `-` | Regular file |
| `d` | Directory |
| `r` | Read |
| `w` | Write |
| `x` | Execute |

Permissions are divided into three ownership groups:

| Owner Type | Characters |
|------------|------------|
| User | 2-4 |
| Group | 5-7 |
| Other | 8-10 |

Example

```text
-rwxr-xr--
```

- User: Read, Write, Execute
- Group: Read, Execute
- Other: Read

---

# Hidden Files

Hidden files begin with a period (`.`).

Example:

```text
.project_x.txt
```

View hidden files:

```bash
ls -la
```

Hidden files are commonly used for:

- Configuration files
- User settings
- System metadata

---

# Changing Permissions (`chmod`)

Modify file or directory permissions.

## Remove write permission for others

```bash
chmod o-w project_k.txt
```

---

## Remove read permission from the group

```bash
chmod g-r project_m.txt
```

---

## Remove write permission from both user and group

```bash
chmod u-w,g-w .project_x.txt
```

---

## Remove execute permission from a directory

```bash
chmod g-x drafts
```

---

# Permission Symbols

| Symbol | Meaning |
|--------|---------|
| `u` | User (Owner) |
| `g` | Group |
| `o` | Others |
| `a` | All Users |

Operations

| Symbol | Action |
|--------|--------|
| `+` | Add Permission |
| `-` | Remove Permission |
| `=` | Assign Exact Permission |

Examples

```bash
chmod u+x script.sh

chmod g-w file.txt

chmod o-r confidential.txt
```

---

# Principle of Least Privilege

One of the most important cybersecurity concepts demonstrated in this lab is the **Principle of Least Privilege (PoLP).**

PoLP ensures users receive only the permissions necessary to perform their job responsibilities.

Benefits include:

- Reduced attack surface
- Protection against accidental changes
- Reduced insider threats
- Improved regulatory compliance
- Better overall system security

---

# Lab Summary

During this lab I practiced:

- Viewing Linux file permissions
- Identifying hidden files
- Removing unnecessary write permissions
- Restricting group access
- Managing directory permissions
- Applying the Principle of Least Privilege

Commands practiced:

```text
ls -l
ls -la
chmod
```

---

# Practical Cybersecurity Uses

Linux permissions are critical when:

- Hardening Linux servers
- Securing sensitive files
- Restricting administrator access
- Protecting configuration files
- Securing log files
- Performing security audits
- Investigating privilege escalation
- Implementing access control

---

# Key Takeaways

- `ls -l` displays permissions.
- `ls -la` includes hidden files.
- `chmod` modifies permissions.
- Hidden files begin with a period (`.`).
- File permissions are assigned to User, Group, and Other.
- Proper permissions enforce the Principle of Least Privilege.

---

# Skills Practiced

- Linux Permissions
- Authorization
- Access Control
- Principle of Least Privilege (PoLP)
- File Security
- Directory Security
- Linux Administration
- Security Hardening
