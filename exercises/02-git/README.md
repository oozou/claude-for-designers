# Exercise 2: Git basics

Practice version control with Git. You can do this exercise in Claude Code at
[claude.ai/code](https://claude.ai/code) - Claude handles Git commands for you.

## Why learn Git basics?

Git tracks changes to your code. It lets you:
- Save checkpoints you can return to
- See what changed and when
- Collaborate without overwriting each other's work

Claude Code handles Git for you, but understanding the concepts helps you work more effectively.

## Core concepts

### Repository (repo)
A project folder tracked by Git.

### Commit
A snapshot of your project at a point in time. Like a save point in a game.

### Branch
A parallel version of your code for working on features without affecting the main code.

## Tasks

### Part 1: Create a repo and make commits

1. **Create a new project**
   ```
   Create a new project called "git-practice" with a README.md file
   ```

2. **Check the status**
   ```
   What's the git status?
   ```
   Claude will show you that README.md is ready to be committed.

3. **Make your first commit**
   ```
   Commit the README with the message "Initial commit"
   ```

4. **Edit the file**
   ```
   Add a description to the README: "This is a practice project for learning Git."
   ```

5. **See what changed**
   ```
   What changed since my last commit?
   ```
   Claude will show you the diff (the difference).

6. **Commit the change**
   ```
   Commit this change with the message "Add project description"
   ```

7. **View history**
   ```
   Show me the commit history
   ```

### Part 2: Branching

1. **Create a branch**
   ```
   Create a new branch called "feature/add-about"
   ```

2. **Make a change on the branch**
   ```
   Create a file called ABOUT.md with some text about the project
   ```

3. **Commit it**
   ```
   Commit this new file
   ```

4. **Switch back to main**
   ```
   Switch to the main branch
   ```

5. **Notice the difference**
   ```
   What files are in this project?
   ```
   ABOUT.md won't be there - it only exists on your feature branch.

6. **Switch back to see it**
   ```
   Switch to the feature/add-about branch
   ```
   Now ABOUT.md is back.

## Key Git concepts

| Concept | What it means |
|---------|---------------|
| Repository | Your project folder with Git tracking |
| Commit | A saved snapshot of your project |
| Branch | A parallel version for working on features |
| Main | The primary branch (the "real" version) |
| Staging | Preparing files to be committed |
| Diff | The changes between two versions |

## How to talk to Claude about Git

Instead of memorizing commands, just describe what you want:

| What you want | What to say |
|---------------|-------------|
| See changes | "What's changed since my last commit?" |
| Save work | "Commit these changes" |
| New feature | "Create a branch called feature/login" |
| Switch branches | "Switch to the main branch" |
| Upload to GitHub | "Push this to GitHub" |
| Get latest | "Pull the latest changes" |

## Done?

You understand Git basics. Move on to Exercise 3 to build a real prototype!
