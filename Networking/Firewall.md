# Networking 101

>  It would be great if you completed the **ports file** first.

---

## Firewall

Now what is a firewall you ask? You can think of it like a bouncer at a club — it blocks people from entering. That's a firewall.

There are 2 types of firewall:

**Stateless** — a worse version of stateful because it doesn't record the conversation between the data, so sometimes it blocks it or just lets it in without checking properly.

**Stateful** — it records all the data conversation with the receiver. A better and more secure version than stateless.

---

### Commands

Check if your firewall is active:
```bash
sudo ufw status
```

Enable the firewall:
```bash
sudo ufw enable
```

Disable the firewall:
```bash
sudo ufw disable
```

>  **Note:** Always allow SSH first so you don't lock yourself out of your own server:
> ```bash
> sudo ufw allow 22
> ```

Open a port and allow it:
```bash
sudo ufw allow 22
```

IP ban a specific address:
```bash
sudo ufw deny from (IP)
```

Allow a specific IP on port 22:
```bash
sudo ufw allow from (IP) to any port 22
```

Block all incoming data by default:
```bash
sudo ufw default deny incoming
```

Allow all outgoing data by default:
```bash
sudo ufw default allow outgoing
```

Block all outgoing data by default:
```bash
sudo ufw default deny outgoing
```

---

### Incoming vs Outgoing

**Outgoing** = the data that you send out

**Incoming** = the data that comes back to you

---

### Example

With google.com:

- **Outgoing** → you send a request to google.com to access their server
- **Incoming** → Google sends the page back to you



