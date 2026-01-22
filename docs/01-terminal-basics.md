# Terminal basics

The terminal (also called command line or shell) is a text interface to your computer. Instead of
clicking icons, you type commands. It's faster once you get the hang of it.

## Opening Terminal

- Press `Cmd + Space` to open Spotlight
- Type "Terminal" and press Enter

Or find it in Applications > Utilities > Terminal.

## Understanding the prompt

When you open Terminal, you'll see something like:

```
yourname@MacBook ~ %
```

This is your **prompt**. It shows:
- Your username
- Your computer name
- Your current location (`~` means your home folder)
- The `%` or `$` indicates it's ready for input

## Your first commands

### Where am I?

```bash
pwd
```

**P**rint **W**orking **D**irectory - shows your current location.

```
/Users/yourname
```

### What's here?

```bash
ls
```

**L**i**s**t - shows files and folders in your current location.

```bash
ls -la
```

The `-la` flags show:
- `-l` long format (details like size, date)
- `-a` all files (including hidden ones starting with `.`)

### Moving around

```bash
cd Documents
```

**C**hange **D**irectory - move into a folder.

```bash
cd ..
```

Go up one level (to the parent folder).

```bash
cd ~
```

Go to your home folder (shortcut).

```bash
cd ~/Projects
```

Go directly to Projects in your home folder.

## File and folder operations

### Create a folder

```bash
mkdir my-project
```

**M**a**k**e **Dir**ectory - creates a new folder.

```bash
mkdir -p projects/web/my-site
```

The `-p` flag creates parent folders if they don't exist.

### Create a file

```bash
touch notes.txt
```

Creates an empty file (or updates its timestamp if it exists).

### View file contents

```bash
cat README.md
```

Shows the entire file contents.

```bash
less README.md
```

View file with scrolling (press `q` to quit).

### Copy files

```bash
cp original.txt copy.txt
```

Copy a file.

```bash
cp -r folder/ folder-copy/
```

Copy a folder (the `-r` means recursive - includes everything inside).

### Move or rename files

```bash
mv old-name.txt new-name.txt
```

Rename a file.

```bash
mv file.txt Documents/
```

Move a file to another folder.

### Delete files (careful!)

```bash
rm unwanted-file.txt
```

**R**e**m**ove - deletes a file. No trash can. Gone forever.

```bash
rm -r unwanted-folder/
```

Delete a folder and everything in it. Be very careful with this.

## Keyboard shortcuts

| Shortcut | What it does |
|----------|--------------|
| `Tab` | Autocomplete file/folder names |
| `Up Arrow` | Previous command |
| `Ctrl + C` | Cancel current command |
| `Ctrl + A` | Jump to start of line |
| `Ctrl + E` | Jump to end of line |
| `Ctrl + L` | Clear screen (same as `clear`) |
| `Cmd + K` | Clear terminal completely |

## Tab completion

This is your best friend. Type the first few letters of a file or folder name and press `Tab`:

```bash
cd Docu[Tab]
```

Becomes:

```bash
cd Documents/
```

If there are multiple matches, press `Tab` twice to see options.

## Paths explained

### Absolute paths

Start with `/` and specify the complete location:

```
/Users/yourname/Projects/my-site
```

### Relative paths

Relative to where you currently are:

```
./my-site          # my-site in current folder
../other-project   # other-project in parent folder
~/Downloads        # Downloads in your home folder
```

Special symbols:
- `.` current directory
- `..` parent directory
- `~` home directory

## Useful commands

### Find files

```bash
find . -name "*.txt"
```

Find all `.txt` files in current directory and subdirectories.

### Search file contents

```bash
grep "search term" file.txt
```

Find lines containing "search term" in a file.

### Check command history

```bash
history
```

Shows your recent commands.

### Get help

```bash
man ls
```

Shows the **man**ual for any command. Press `q` to quit.

## Exercise: Terminal navigation

1. Open Terminal
2. Run `pwd` to see where you are
3. Run `ls` to see what's in your home folder
4. Create a test folder: `mkdir terminal-practice`
5. Move into it: `cd terminal-practice`
6. Create a file: `touch hello.txt`
7. List to confirm: `ls`
8. Go back up: `cd ..`
9. Delete the test folder: `rm -r terminal-practice`

Congratulations! You've completed the terminal basics.

## Common mistakes

**"command not found"**
- Check for typos
- Make sure the tool is installed

**"permission denied"**
- You might need `sudo` (admin access) - but be careful
- Or you're trying to modify a protected file

**"No such file or directory"**
- Check the path is correct
- Use `ls` to see what's actually there
- Remember paths are case-sensitive

## Next steps

Continue to [Git basics](02-git-basics.md) to learn version control.
