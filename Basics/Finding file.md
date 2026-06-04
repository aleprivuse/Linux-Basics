# Base of Finding Commands

In finding commands there are only 2 commands you are going to need to learn, the first one is `grep` and the second one is `find`.

What is the difference between `grep` and `find`? Imagine `grep` is like finding a word in a book and `find` is like finding a book in a library.

## Important Symbols

| Symbol | Description |
|--------|-------------|
| `.` | Select all files in the current folder |
| `/` | Select all folders/files in the computer (called root) |

---

## grep

`grep` is a combination of these things:

```
grep [flag] "the word" filename
```

Flags are optional, you can even use multiple in one command:

| Flag | Description |
|------|-------------|
| `-i` | Ignore upper case / lower case |
| `-n` | Show line numbers |
| `-r` | Select all files in the folder |

**Examples:**
```
grep -i "hello" file.txt
grep -in "hello" file.txt
```

---

## find

`find` is a combination of these things:

```
find [where] [what type] "the name"
```

**Where:**

| Symbol | Description |
|--------|-------------|
| `.` | Current folder |
| `/` | Root (entire computer) |

**What type:**

| Option | Description |
|--------|-------------|
| `-name` | Find by name |
| `-type f` | Find by file |
| `-type d` | Find by folder |
| `-size` | Find by size |
| `-user` | Find by who owns the file |


**Examples:**
```
find / -name "hello.txt"
find . -type d
find / -type f
```


