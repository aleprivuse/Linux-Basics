# Networking 101

>  Before you go into this folder, finish the **basics folder** first, then you can move on.

---

## Ports

Before i go into the commands, let me explain what a port is.

Imagine the **IP address** is like the address of a building — the **port** is the apartment inside that building.

### Well-known Ports (0 - 1023)
These are reserved for trusted, serious services. Only **root** can open them — this is a security feature so a random program can't pretend to be a trusted server.

| Port | What it does |
|------|--------------|
| 22   | SSH (remote access) |
| 80   | HTTP (normal website) |
| 443  | HTTPS (secure website) |

### Ephemeral Ports (1024+)
These are temporary ports your computer picks randomly when YOU connect to something.

Example: you open two tabs to google.com at the same time:
```
Tab 1 → your port 52847 → google.com:443
Tab 2 → your port 61203 → google.com:443
```
Your computer uses the port number to know which response goes to which tab.

---

## Protocols

**TCP (Transmission Control Protocol)**
Like sending a package with a tracker — you know if it arrived.

**UDP (User Datagram Protocol)**
Like sending a package without a tracker — faster, but you don't know if it arrived.

---

## Commands

See all open ports on your machine:
```bash
ss -tuln
```

| Flag | Meaning |
|------|---------|
| `-t` | TCP |
| `-u` | UDP |
| `-l` | listening (waiting for connections) |
| `-n` | show numbers, not names |

