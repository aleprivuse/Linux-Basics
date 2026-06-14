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

