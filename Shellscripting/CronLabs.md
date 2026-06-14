# Cron Jobs

So what is a cron job you may ask? Really simple — it's like a schedule for your computer. You are just telling your computer to run something at a specific time and date automatically.

---

## Commands

Open the cron editor:
```bash
crontab -e
```

List all your cron jobs:
```bash
crontab -l
```

---

## The Syntax

```
*  *  *  *  *  command
│  │  │  │  │
│  │  │  │  └── day of week (0=Sun, 1=Mon, 2=Tue, 3=Wed, 4=Thu, 5=Fri, 6=Sat)
│  │  │  └───── month (1-12)
│  │  └──────── day of month (1-31)
│  └─────────── hour (0-23)
└────────────── minute (0-59)
```

 **Tip:** `*` means "every" — so `* * * * *` means every minute of every hour of every day.

---

## Examples

| Cron | When it runs |
|------|-------------|
| `0 8 * * *` | Every day at 8am |
| `0 8 * * 1` | Every Monday at 8am |
| `30 3 * * *` | Every day at 3:30am |
| `0 0 * * 1,4` | Every Monday and Thursday at midnight |
| `*/30 * * * *` | Every 30 minutes |
| `0 6 * * 1-5` | Every weekday at 6am |

---

## Save output to a file

```bash
# append to file (keeps old results)
0 8 * * * bash /home/(your username)/script.sh >> /home/user/report.txt

# overwrite file (starts fresh every time)
0 8 * * * bash /home/(your username)/script.sh > /home/user/report.txt
```
if you dont know your username use this `whoami`
