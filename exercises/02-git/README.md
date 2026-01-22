# Exercise 2: Git basics

Practice version control with Git.

## Setup

Create a practice repository:

```bash
mkdir ~/git-exercise
cd ~/git-exercise
git init
```

## Tasks

### Part 1: First commit

1. **Check status**
   ```bash
   git status
   ```
   Should show "No commits yet" and nothing to commit.

2. **Create a file**
   ```bash
   echo "# My Practice Project" > README.md
   ```

3. **Check status again**
   ```bash
   git status
   ```
   Now you should see README.md as an "untracked file".

4. **Stage the file**
   ```bash
   git add README.md
   ```

5. **Check status**
   ```bash
   git status
   ```
   README.md should now be under "Changes to be committed".

6. **Commit**
   ```bash
   git commit -m "Add README"
   ```

7. **View history**
   ```bash
   git log
   ```

### Part 2: Making changes

1. **Edit the file**
   ```bash
   echo "This is a practice project for learning Git." >> README.md
   ```

2. **See the diff**
   ```bash
   git diff
   ```
   Shows what changed (+ means added line).

3. **Stage and commit**
   ```bash
   git add README.md
   git commit -m "Add project description"
   ```

4. **View history**
   ```bash
   git log --oneline
   ```

### Part 3: Branching

1. **Create a branch**
   ```bash
   git checkout -b feature/add-about
   ```

2. **Confirm you switched**
   ```bash
   git branch
   ```
   The `*` shows your current branch.

3. **Add a new file**
   ```bash
   echo "## About\n\nThis project helps me learn Git." > ABOUT.md
   git add ABOUT.md
   git commit -m "Add about section"
   ```

4. **Switch back to main**
   ```bash
   git checkout main
   ```

5. **Notice ABOUT.md is gone**
   ```bash
   ls
   ```
   It only exists on the feature branch!

6. **Switch back and confirm**
   ```bash
   git checkout feature/add-about
   ls
   ```
   ABOUT.md is back.

### Part 4: Clean up

```bash
cd ~
rm -rf git-exercise
```

## Bonus challenges

- Try `git log --graph --oneline --all` to see branches visually
- Create a merge conflict and resolve it:
  1. Make a change to README.md on main
  2. Make a different change to the same line on your feature branch
  3. Try to merge and see what happens

## Done?

You understand Git basics. Move on to Exercise 3 to use Claude Code for real prototyping!
