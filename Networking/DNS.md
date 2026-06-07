# Networking 101

 It would be great if you finished the **Firewall** and **Ports** files first.

---

## DNS

So what is DNS (Domain Name System)? Think about it like a dictionary — when you type `google.com` it searches the dictionary for the word "google" and finds its IP address so you can connect.

---

### Caching

Now think — if you open Google 50 times in a row, what does the computer do?

Simple: the first time it asks the DNS for Google's IP, then it saves it for around 300 seconds. So the next time you want to visit it, it doesn't need to ask again.

In networking terms we call that **TTL (Time To Live)** — every DNS record has one. When the 300 seconds pass it throws the answer away, then the cycle starts again.

---

### DNS Resolution

So what is that you may ask? It's simply the term we use when our DNS does not know where an IP came from.

In my case my DNS server is my router. If he doesn't know the IP of a specific server, it's going to ask the DNS of Sunrise (my provider). Then if Sunrise doesn't know it, it's going to ask the **Root DNS** — there are 13 of them and they run the whole internet.

```
Your computer
      ↓
Router
      ↓
Sunrise (ISP)
      ↓
Root DNS (13 servers — run the whole internet)
```

---

### DNS Recursion

So now you ask — what if the root doesn't know it?

Simple: it goes and asks another DNS. In the case of `google.com` it's going to ask the `.com` DNS, and the `.com` DNS is going to ask Google's DNS, and then it returns the IP. That's called **DNS recursion**.

```
Root DNS → knows who handles .com
      ↓
.com DNS → knows who handles google.com
      ↓
Google DNS → returns the exact IP 
```

---

## Commands

Look up the IP of a domain:
```bash
nslookup google.com
```

More detailed DNS lookup:
```bash
dig google.com
```

Ask a specific DNS server (Google's):
```bash
nslookup google.com 8.8.8.8
```

Ask Cloudflare's DNS server:
```bash
nslookup google.com 1.1.1.1
```

See which DNS server your computer is using:
```bash
cat /etc/resolv.conf
```

---

### Cloudflare (1.1.1.1) vs Sunrise DNS

So what is Cloudflare? It's a faster and more private DNS server.

You may ask — why use Cloudflare instead of your normal one?

| DNS | Who runs it | Do they log your visits? |
|-----|-------------|--------------------------|
| Sunrise DNS | Your ISP | Yes |
| 8.8.8.8 | Google | Yes |
| 1.1.1.1 | Cloudflare | No |

In my case I use Sunrise by default — they can see and log every website I visit. Cloudflare specifically promises not to log it, and it's also the fastest DNS server in the world.


