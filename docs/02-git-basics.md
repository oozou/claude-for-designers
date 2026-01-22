# Git basics

Git is a version control system. Think of it as "save points" for your code that let you:
- Track every change you make
- Go back to previous versions
- Collaborate with others without overwriting each other's work

GitHub is a website that hosts Git repositories online, making collaboration and backup easy.

## Core concepts

### Repository (repo)

A project folder tracked by Git. Contains your files plus a hidden `.git` folder with all the
version history.

### Commit

A snapshot of your project at a point in time. Like a save point in a video game - you can always
go back to it.

### Branch

A parallel version of your code. The main branch is usually called `main`. You create branches to
work on features without affecting the main code.

### Remote

A copy of your repository on a server (like GitHub). Your local repo can "push" changes to and
"pull" changes from the remote.

## Setting up Git

### Configure your identity

Git needs to know who you are for commit messages:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@oozou.com"
```

### Check your config

```bash
git config --list
```

## Basic workflow

The typical Git workflow:

1. Make changes to files
2. **Stage** the changes you want to commit
3. **Commit** with a message describing what you did
4. **Push** to GitHub

### Check status (do this constantly)

```bash
git status
```

This shows:
- What branch you're on
- What files have changed
- What's staged for commit
- What's not tracked

### Stage changes

```bash
git add filename.txt
```

Stage a specific file.

```bash
git add .
```

Stage all changed files in the current directory.

### Commit changes

```bash
git commit -m "Add login button to homepage"
```

The `-m` flag lets you add a message inline. Messages should:
- Start with a verb (Add, Fix, Update, Remove)
- Describe what the commit does
- Be concise but clear

### Push to GitHub

```bash
git push
```

Uploads your commits to the remote repository.

### Pull from GitHub

```bash
git pull
```

Downloads the latest changes from the remote. Do this before starting work.

## Starting a new project

### Option 1: Clone an existing repo

```bash
git clone https://github.com/username/repo-name.git
cd repo-name
```

### Option 2: Initialize a new repo

```bash
mkdir my-project
cd my-project
git init
```

Then create a repo on GitHub and connect it:

```bash
git remote add origin https://github.com/username/my-project.git
git push -u origin main
```

## Branching

### See all branches

```bash
git branch
```

The current branch has a `*` next to it.

### Create and switch to a new branch

```bash
git checkout -b feature/new-header
```

This creates a branch called `feature/new-header` and switches to it.

### Switch between branches

```bash
git checkout main
git checkout feature/new-header
```

### Push a new branch to GitHub

```bash
git push -u origin feature/new-header
```

The `-u` flag sets up tracking so future pushes just need `git push`.

## Pull requests

A pull request (PR) is how you propose changes on GitHub. It lets others review your code before
merging it into main.

### Using GitHub CLI (gh)

Create a pull request:

```bash
gh pr create
```

This will prompt you for:
- Title
- Description
- Base branch (usually `main`)

Or do it all in one command:

```bash
gh pr create --title "Add new header design" --body "Implements the header from Figma design #123"
```

### View pull requests

```bash
gh pr list
```

### Check out someone's PR to test it

```bash
gh pr checkout 42
```

(where 42 is the PR number)

## Viewing history

### See commit history

```bash
git log
```

Press `q` to exit.

### Compact log

```bash
git log --oneline
```

### See what changed

```bash
git diff
```

Shows unstaged changes.

```bash
git diff --staged
```

Shows staged changes (what will be in next commit).

## Undoing things

### Discard changes to a file

```bash
git checkout -- filename.txt
```

Reverts the file to the last committed version. Changes are lost.

### Unstage a file

```bash
git reset HEAD filename.txt
```

Removes from staging area but keeps your changes.

### Undo the last commit (keep changes)

```bash
git reset --soft HEAD~1
```

Removes the commit but keeps your changes staged.

## Common scenarios

### "I want to start fresh from GitHub"

```bash
git fetch origin
git reset --hard origin/main
```

Warning: This deletes all local changes.

### "I made changes but want to switch branches"

```bash
git stash
git checkout other-branch
# do stuff
git checkout original-branch
git stash pop
```

Stash temporarily saves your changes.

### "I committed to the wrong branch"

```bash
git log --oneline  # note the commit hash
git checkout correct-branch
git cherry-pick abc123  # use the commit hash
git checkout wrong-branch
git reset --hard HEAD~1  # remove from wrong branch
```

## Exercise: Git workflow

1. Create a new folder and initialize Git:
   ```bash
   mkdir git-practice
   cd git-practice
   git init
   ```

2. Create a file:
   ```bash
   echo "# My Project" > README.md
   ```

3. Check status:
   ```bash
   git status
   ```

4. Stage and commit:
   ```bash
   git add README.md
   git commit -m "Initial commit with README"
   ```

5. Create a branch:
   ```bash
   git checkout -b feature/add-description
   ```

6. Make a change:
   ```bash
   echo "This is a practice project." >> README.md
   ```

7. Commit the change:
   ```bash
   git add README.md
   git commit -m "Add project description"
   ```

8. Switch back to main:
   ```bash
   git checkout main
   ```

9. Check the file - notice your change isn't there (it's on the other branch):
   ```bash
   cat README.md
   ```

## Common mistakes

**"Your branch is behind"**
- Run `git pull` to get the latest changes

**"Merge conflict"**
- Two people edited the same part of a file
- Open the file, look for `<<<<<<<` markers
- Decide which version to keep, remove the markers
- Stage and commit

**"Detached HEAD"**
- You checked out a specific commit instead of a branch
- Run `git checkout main` to get back to a branch

## Quick reference

| Command | What it does |
|---------|--------------|
| `git status` | See current state |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Create a commit |
| `git push` | Upload to GitHub |
| `git pull` | Download from GitHub |
| `git checkout -b name` | Create and switch to branch |
| `git checkout main` | Switch to main branch |
| `gh pr create` | Create a pull request |

## Next steps

Continue to [Claude Code workflow](03-claude-code.md) to learn AI-assisted development.
