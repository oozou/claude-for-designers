# Exercise 1: Terminal navigation

Practice navigating your Mac using the terminal.

## Tasks

1. **Find your location**
   - Open Terminal
   - Run `pwd` to see where you are
   - Expected: something like `/Users/yourname`

2. **Explore your home folder**
   - Run `ls` to see what's in your home folder
   - Run `ls -la` to see hidden files too
   - Notice files starting with `.` - these are hidden config files

3. **Navigate to Documents**
   - Run `cd Documents`
   - Run `pwd` to confirm
   - Run `ls` to see what's there

4. **Create a practice folder**
   - Run `mkdir terminal-exercise`
   - Run `cd terminal-exercise`
   - Run `pwd` to confirm you're inside

5. **Create some files**
   - Run `touch file1.txt file2.txt file3.txt`
   - Run `ls` to see them
   - Run `ls -la` to see details (they should be 0 bytes)

6. **Navigate with paths**
   - Run `cd ~` to go home
   - Run `cd ~/Documents/terminal-exercise` to go directly there
   - Run `cd ..` to go up one level
   - Run `pwd` - you should be in Documents

7. **Clean up**
   - Run `rm -r terminal-exercise`
   - Run `ls` to confirm it's gone

## Bonus challenges

- Use Tab completion: type `cd Doc` and press Tab
- Use the up arrow to recall previous commands
- Run `history` to see all your recent commands
- Try `cd -` to go back to the previous directory

## Done?

You've mastered basic terminal navigation. Move on to Exercise 2!
