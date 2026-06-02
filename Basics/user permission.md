# Permission

## Important to learn

Before going to the commands I'm going to explain the basics.
Imagine that in your computer there are 3 groups, one is the owner (you), the group (you can think about it like multiple users on your account) and the last is everyone else.

## Now we are going to go to the permission (not the commands)

First you are going to need to understand this:

`-rwxr-xr--` (this is a string you get by using `ls -la` on your computer)

We are going to first understand what r w x mean:
1. r = read
2. w = write
3. x = execute
4. `-` = the properties they don't have

The order of the properties are always like this, now that we understand the basics let's go to how to read the string. The string is always divided in 3 parts, let's take the one before as example:

`-rwxr-xr--`

`-` = what is that you are going to ask, that is just where the file is from, what does it mean:
1. `-` = from a regular file
2. `d` = from the directory
3. `l` = from a link (a shortcut to another file)

`rwx` => the first part = rwx that is the owner, they can do everything (read, write, execute)

`r-x` => the second part = r-x that is the group, they can do everything except write

`r--` => the last part = r-- that is everyone else, they can only read
