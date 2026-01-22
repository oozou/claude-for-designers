# Exercise 1: Terminal navigation

Practice navigating using the terminal. You can do this exercise in Claude Code's built-in
terminal at [claude.ai/code](https://claude.ai/code).

## Why learn terminal basics?

Even though Claude Code handles most commands for you, understanding terminal basics helps you:
- Read what Claude is doing
- Debug when things go wrong
- Feel confident asking Claude to run commands

## Tasks

Try these commands in Claude Code. Just ask Claude to run them, or type them in the terminal pane.

### 1. Find your location

```
Run pwd to see where I am
```

This shows your current directory (folder).

### 2. List files

```
Run ls to see what files are here
```

```
Run ls -la to see hidden files and details
```

### 3. Create a folder

```
Create a folder called "practice"
```

Or run directly: `mkdir practice`

### 4. Navigate into it

```
Go into the practice folder
```

Or run: `cd practice`

### 5. Create some files

```
Create three empty text files called file1.txt, file2.txt, and file3.txt
```

Or run: `touch file1.txt file2.txt file3.txt`

### 6. Check your work

```
List the files to confirm they were created
```

### 7. Clean up

```
Delete the practice folder and everything in it
```

Or run: `rm -r practice`

## Key commands to remember

| Command | What it does |
|---------|--------------|
| `pwd` | Print working directory (where am I?) |
| `ls` | List files |
| `ls -la` | List all files with details |
| `cd folder` | Change into a folder |
| `cd ..` | Go up one level |
| `mkdir name` | Create a folder |
| `touch file` | Create an empty file |
| `rm file` | Delete a file |
| `rm -r folder` | Delete a folder and contents |

## Bonus: Ask Claude

Instead of memorizing commands, just ask Claude:

- "What files are in this folder?"
- "Create a new folder called components"
- "Show me the contents of package.json"

Claude translates your requests into the right commands.

## Done?

You understand the basics of terminal navigation. Move on to Exercise 2 to learn Git!
