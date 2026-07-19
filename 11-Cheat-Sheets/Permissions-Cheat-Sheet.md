# Linux Permissions Cheat Sheet

## Permission Types

| Symbol | Meaning |
|----------|---------|
| `r` | Read |
| `w` | Write |
| `x` | Execute |
| `-` | No Permission |

---

## Owner Types

| Symbol | Meaning |
|----------|---------|
| `u` | User (Owner) |
| `g` | Group |
| `o` | Others |
| `a` | All Users |

---

## Permission Operations

| Symbol | Action |
|----------|---------|
| `+` | Add Permission |
| `-` | Remove Permission |
| `=` | Assign Exact Permission |

---

## Common chmod Examples

Grant execute permission to user

```bash
chmod u+x script.sh
```

Remove write permission from group

```bash
chmod g-w file.txt
```

Remove read permission from others

```bash
chmod o-r file.txt
```

Grant read permission to everyone

```bash
chmod a+r file.txt
```

---

## Numeric Permissions

| Number | Permission |
|----------|------------|
| 0 | --- |
| 1 | --x |
| 2 | -w- |
| 3 | -wx |
| 4 | r-- |
| 5 | r-x |
| 6 | rw- |
| 7 | rwx |

---

## Common Numeric Permissions

| Permission | Meaning |
|------------|---------|
| `644` | Owner Read/Write, Everyone Else Read |
| `600` | Owner Read/Write Only |
| `755` | Owner Full Access, Others Read/Execute |
| `700` | Owner Full Access Only |
| `777` | Full Access (Avoid) |

---

## Viewing Permissions

```bash
ls -l
```

Include hidden files

```bash
ls -la
```

---

## Ownership

Change owner

```bash
chown username file.txt
```

Change owner and group

```bash
chown username:group file.txt
```

Change group

```bash
chgrp groupname file.txt
```

---

## Principle of Least Privilege (PoLP)

✔ Give users only the permissions required to perform their job.

Benefits:

- Reduce attack surface
- Prevent accidental modification
- Improve compliance
- Limit insider threats
