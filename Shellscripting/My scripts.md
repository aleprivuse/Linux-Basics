# My Scripts

Here are some basic scripts that I created to make my life easier.

---

## update.sh

Updates and upgrades all packages automatically.

```bash
#!/bin/bash

sudo apt update && sudo apt upgrade -y
```

### Automating it with cron

To run this script automatically every day at 8:30am:

```bash
crontab -e
```

Add this line:
```
30 8 * * * bash /home/(your username)/update.sh
```

## when using 

When you run the bash script you might have this problem.

### Problem — apt is locked / "Waiting for cache lock"

While running an update manually, it got stuck waiting because 
Ubuntu's automatic security updates (`unattended-upgrades`) were 
already running in the background and holding the lock.

**Solution:** Just wait — never force-kill it, as that could 
corrupt the package database. Ubuntu runs this automatically 
to install security patches even without user interaction.
