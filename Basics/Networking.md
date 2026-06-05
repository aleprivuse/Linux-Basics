# Networking 101

Before I start explaining the commands let me explain what an IP address is. An IP address is like the address of your real home but online, it's needed so when the server sends back a signal it knows where to send it.

You can see your IP address with this command:

```
ip a
```

## Full list of commands

| Command | Description |
|---------|-------------|
| `ping google.com` | Check if google is online (you can use another url) |
| `ping -c 4 google.com` | Test the server connection 4 times then stop |
| `curl google.com` | Get the content of a website (you can use another url) |
| `curl -I google.com` | Get the headers of a website |
| `ssh user@ip` | Connect to another machine if you have the username and the IP |
| `wget url` | Download a file |
