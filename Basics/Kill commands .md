# Kill Commands

In Linux they don't have a task manager like Windows but they do have something similar: `ps` (processor status).

In Linux every program or software that you run is called a process, every process has a unique ID of its own called the Process ID or PID. Now I'm going to show you how to use the kill command to end a process and how to see the `ps`.

## How to see the ps or process list

| Command | Description |
|---------|-------------|
| `ps` | Opens a list of your processes |
| `ps aux` | Opens a list of all the processes |
| `top` | A live process viewer, think of it like the Windows task manager (to exit press `Q`) |

## How to kill a process

Like I said before, every process has a PID, you are going to need that to kill a program. Here is how to write it:

```
kill PID
kill -9 PID
```

There are two methods to kill a program, the first command asks nicely, the second one just doesn't care and forces it to close.

> **Note:** use `kill -9` only if the normal one doesn't work

### Example

Let's say your process number is 6970:

```
kill 6970
```

Really easy! You can try it on your own, just use `sleep 300 &` then try to find its PID and delete it.
