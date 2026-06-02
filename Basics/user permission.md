# Permission

## Important to learn

Before going to the commands I'm going to explain the basics.
Imagine that in your computer there are 3 groups, one is the owner (you), the group (you can think about it like multiple users on your account) and the last is everyone else.

## Now we are going to go to the permissions (not the commands)

First you are going to need to understand this:

`-rwxr-xr--` (this is a string you get by using `ls -la` on your computer)

We are going to first understand what r w x mean:
1. `r` = read
2. `w` = write
3. `x` = execute
4. `-` = the properties they don't have

The order of the properties are always like this, now that we understand the basics let's go to how to read the string. The string is always divided in 4 parts, let's take the one before as example:

`-rwxr-xr--`

`-` = what is that you are going to ask, that is just where the file is from, what does it mean:
1. `-` = from a regular file
2. `d` = from the directory
3. `l` = from a link (a shortcut to another file)

`rwx` => the first part = rwx that is the owner, they can do everything (read, write, execute)

`r-x` => the second part = r-x that is the group, they can do everything except write

`r--` => the last part = r-- that is everyone else, they can only read

## Commands

We are going to have only 2, the first one is `chmod` and `chown`:
- `ch` = change
- `mod` = mode
- `own` = owner

Remember the `r`, `w` and `x` from before? They all have a number value too:
1. `r` => 4
2. `w` => 2
3. `x` => 1

### How can you use chmod and chown

With `chmod` you can write something like this:

```
chmod 700 filetest.txt
```
That means the owner gets everything and the rest get nothing. Remember the position really matters.

With `chown` you can do something like this:

```
chown sarah filetest.txt
```
Or assign to a group:
```
chown sarah:developer filetest.txt
```

