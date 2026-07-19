# Linux File System Cheat Sheet

## Linux Directory Structure

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var
```

---

## Important Directories

| Directory | Purpose |
|-----------|----------|
| `/` | Root of filesystem |
| `/home` | User home directories |
| `/root` | Root user's home directory |
| `/etc` | System configuration files |
| `/var` | Variable data (logs, mail, cache) |
| `/tmp` | Temporary files |
| `/usr` | User applications and utilities |
| `/bin` | Essential user commands |
| `/sbin` | System administration commands |
| `/boot` | Bootloader files |
| `/dev` | Device files |
| `/proc` | Process information |
| `/sys` | Kernel information |

---

## Paths

### Absolute Path

Starts from root (`/`)

Example

```text
/home/caitlin/Documents/file.txt
```

---

### Relative Path

Starts from current directory

Example

```text
Documents/file.txt
```

---

## Special Directory Symbols

| Symbol | Meaning |
|----------|---------|
| `.` | Current Directory |
| `..` | Parent Directory |
| `~` | Home Directory |
| `/` | Root Directory |

---

## Hidden Files

Hidden files begin with a period (`.`)

Example

```text
.bashrc
```

Display hidden files

```bash
ls -la
```

---

## Common Navigation Commands

```bash
pwd
ls
cd
```

---

## Common File Management Commands

```bash
mkdir
touch
cp
mv
rm
cat
head
tail
nano
```

---

## Common Search Commands

```bash
grep
find
locate
which
whereis
```

---

## Cybersecurity Relevance

Security analysts commonly work within:

| Directory | Why |
|-----------|-----|
| `/var/log` | Investigate logs |
| `/etc` | Review configurations |
| `/home` | Examine user files |
| `/tmp` | Investigate malware staging |
| `/proc` | Review running processes |
| `/usr/bin` | Verify installed binaries |

---

## Common Log Locations

| File | Purpose |
|------|---------|
| `/var/log/syslog` | System logs |
| `/var/log/auth.log` | Authentication logs |
| `/var/log/messages` | General system messages |
| `/var/log/kern.log` | Kernel logs |
