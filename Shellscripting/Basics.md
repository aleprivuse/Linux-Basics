 The Basics

> Even if you already learned a coding language, stick around here — the syntax is completely different.

---

## Shell Scripting

So what is it you may ask? Really simple — it's a script that lets you save commands and run them whenever you want.

Here are the basic commands you need to get started:

| Command | What it does |
|---------|-------------|
| `#!/bin/bash` | Put it on the top of your script so Linux knows it's a bash script |
| `bash script.sh` | Run your script |
| `nano script.sh` | Open, create, or modify your script |

>  **Note:** When you finish writing your script press `CTRL+X` → `Y` → `Enter` to save it.

---

## Variables

Variables are like books that you store your information inside.

Here's how you create and use one:

```bash
name="Mario"
echo "Hello $name"
```

>  **Note:** Always put `""` if you want to write a string. A string is a list of characters that are not numbers.

---

## If / Else Statement

Think of it like giving the computer a choice — if the number is bigger run this, but if it's smaller run this other thing.

Here's the syntax:

```bash
port=80

if [ $port -eq 80 ]; then
    echo "HTTP"
else
    echo "NOT HTTP"
fi
```

>  **Important:** Shell scripting is strict about spaces and upper/lowercase — always double check you wrote it right.

>  **Tip:** If/else always starts with `if` and ends with `fi`.

### Comparison Operators

| Operator | Meaning | Use for |
|----------|---------|---------|
| `-eq` | equal | numbers |
| `-ne` | not equal | numbers |
| `-gt` | greater than | numbers |
| `-lt` | less than | numbers |
| `=` | equal | strings |
| `!=` | not equal | strings |

---

## Loops

Loops are just repeated actions that you tell the computer to do.

Here's a real example that checks if ports are open:

```bash
for port in 22 80 443; do
    if ss -tuln | grep -q "$port"; then
        echo "Port $port is open"
    else
        echo "Port $port is closed"
    fi
done
```

 **Tip:** The loop starts with `do` and ends with `done`. The `|` means "take the output of this command and send it to the next one."




  
