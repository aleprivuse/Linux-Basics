# Linux Basic Commands
---

## File Navigation

1. `pwd` = shows where you are
2. `ls` = shows files and folders in your current directory
3. `ls -la` = shows all details including hidden files
4. `cd ..` = go up one level in the folder tree
5. `cd` = move into a folder
6. `mkdir` = create a folder
7. `touch` = creates an empty file
8. `echo` = adds text inside a file:
   - `>` generates new text (overwrites)
   - `>>` adds new text and keeps the old one
9. `cat` = shows the content of a file
10. `rm file.txt` = deletes a file
11. `rm -r folder` = deletes an entire folder

### Example

```bash
mkdir test
touch test/text.txt
echo "I'm learning Linux" > test/text.txt
cat test/text.txt
```
> Use `>>` instead of `>` if you want to keep the old text.
