# User and Group Management

## Overview

User and group management is a core component of Linux system administration and cybersecurity. Administrators use these tools to control authentication, authorization, and ownership of files and system resources.

Proper user management helps enforce the Principle of Least Privilege (PoLP), ensuring users only receive the access necessary to perform their job responsibilities.

---

# Why It Matters

Managing user accounts is critical for maintaining a secure Linux environment.

Security analysts routinely perform tasks such as:

- Creating user accounts
- Assigning users to security groups
- Managing file ownership
- Granting or revoking permissions
- Removing inactive accounts
- Auditing user access

Proper identity management reduces the risk of unauthorized access and privilege escalation.

---

# Using `sudo`

Many administrative commands require elevated privileges.

The `sudo` command temporarily grants administrative (root) privileges to authorized users.

### Syntax

```bash
sudo command
```

### Example

```bash
sudo useradd researcher9
```

---

# Creating Users (`useradd`)

Creates a new user account.

### Syntax

```bash
sudo useradd username
```

### Example

```bash
sudo useradd researcher9
```

### Create User and Assign Primary Group

```bash
sudo useradd researcher9 -g research_team
```

### Common Uses

- Onboard new employees
- Create service accounts
- Build lab environments

---

# Modifying Users (`usermod`)

Updates an existing user account.

---

## Change Primary Group

```bash
sudo usermod -g research_team researcher9
```

---

## Add User to a Supplementary Group

```bash
sudo usermod -a -G sales_team researcher9
```

### Common Uses

- Department transfers
- Additional project access
- Role changes

---

# Changing File Ownership (`chown`)

Changes the ownership of files and directories.

### Syntax

```bash
sudo chown username filename
```

### Example

```bash
sudo chown researcher9 project_r.txt
```

### Common Uses

- Assign project ownership
- Correct ownership after migrations
- Secure sensitive files

---

# Deleting Users (`userdel`)

Removes a user account from the system.

### Syntax

```bash
sudo userdel researcher9
```

### Common Uses

- Employee offboarding
- Removing temporary accounts
- Cleaning lab environments

---

# Deleting Groups (`groupdel`)

Removes unused groups.

### Syntax

```bash
sudo groupdel researcher9
```

### Common Uses

- Remove orphaned groups
- Maintain clean user management
- Reduce unnecessary access groups

---

# Primary vs Supplementary Groups

## Primary Group

Every Linux user belongs to one primary group.

Example:

```bash
sudo usermod -g research_team researcher9
```

---

## Supplementary Groups

Users can belong to multiple secondary groups.

Example:

```bash
sudo usermod -a -G sales_team researcher9
```

This allows access to resources shared across departments while maintaining a single primary group.

---

# File Ownership

Each Linux file has:

- Owner (User)
- Group
- Permissions

Example:

```text
-rw-r----- researcher9 research_team project_r.txt
```

Changing ownership allows responsibility for files to be transferred securely between users.

---

# Principle of Least Privilege (PoLP)

One of the most important cybersecurity principles demonstrated in this lab is the Principle of Least Privilege.

Users should receive:

- Only the permissions they need
- Only access to required resources
- Only membership in necessary groups

Benefits include:

- Reduced insider threats
- Reduced attack surface
- Improved compliance
- Better accountability

---

# Authentication vs Authorization

Authentication verifies **who a user is**.

Example:

- Logging into Linux with a username and password.

Authorization determines **what a user is allowed to access**.

Example:

- Membership in the `research_team` group.
- Ownership of project files.
- Linux file permissions.

Both concepts work together to protect system resources.

---

# Lab Summary

During this lab I practiced:

- Creating users
- Assigning primary groups
- Assigning supplementary groups
- Changing file ownership
- Removing users
- Removing groups

### Commands Practiced

```text
sudo
useradd
usermod
chown
userdel
groupdel
```

---

# Practical Cybersecurity Uses

These commands are commonly used when:

- Onboarding new employees
- Offboarding departing employees
- Managing privileged accounts
- Conducting access reviews
- Investigating unauthorized access
- Implementing Identity and Access Management (IAM)
- Supporting compliance requirements
- Securing Linux servers

---

# Key Takeaways

- `sudo` executes commands with elevated privileges.
- `useradd` creates user accounts.
- `usermod` modifies user accounts and group memberships.
- `chown` changes ownership of files and directories.
- `userdel` removes user accounts.
- `groupdel` removes unused groups.
- Proper user management supports secure authentication and authorization.

---

# Skills Practiced

- Linux User Administration
- User Management
- Group Management
- Authentication
- Authorization
- Identity and Access Management (IAM)
- File Ownership
- Principle of Least Privilege (PoLP)
- Linux Administration
