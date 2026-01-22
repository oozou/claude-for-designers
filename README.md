# Claude for Designers

An interactive tutorial for OOZOU designers to learn terminal basics, Git, and Claude Code for
frontend prototyping.

## Prerequisites

Before starting, make sure you have:

- A Mac with macOS
- A GitHub account (create one at [github.com](https://github.com) if needed)
- A Claude Pro or Max subscription (or Claude for Teams/Enterprise access)

## Getting started

### Step 1: Open Claude Code

Go to **[claude.ai/code](https://claude.ai/code)** and log in with your Claude account.

That's it. Claude Code runs in your browser - no installation needed.

### Step 2: Connect to GitHub

In Claude Code, ask:

```
Help me connect to GitHub
```

Claude will guide you through the authentication process.

### Step 3: Start learning

You're ready to go. Work through the tutorial modules below, asking Claude Code to help you at
each step.

## Tutorial modules

Work through these in order:

1. **[Terminal basics](docs/01-terminal-basics.md)** - Navigate your Mac like a pro
2. **[Git fundamentals](docs/02-git-basics.md)** - Track changes and collaborate
3. **[Claude Code workflow](docs/03-claude-code.md)** - AI-assisted development
4. **[Frontend prototyping](docs/04-frontend-prototyping.md)** - Tailwind, shadcn/ui, and rapid
   prototyping

## Quick reference

### Essential terminal commands

These commands work in Claude Code's built-in terminal:

| Command | What it does | Example |
|---------|--------------|---------|
| `cd` | Change directory | `cd Projects` |
| `ls` | List files | `ls -la` |
| `pwd` | Print current directory | `pwd` |
| `mkdir` | Make directory | `mkdir my-project` |

### Essential Git commands

| Command | What it does |
|---------|--------------|
| `git status` | See what's changed |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Save changes with a message |
| `git push` | Upload to GitHub |
| `git pull` | Download latest changes |

### Talking to Claude Code

Just type naturally. Examples:

| What you want | What to say |
|---------------|-------------|
| Create a file | "Create an index.html with a basic page structure" |
| Edit code | "Change the background color to blue in styles.css" |
| Commit changes | "Commit these changes with an appropriate message" |
| Create a PR | "Create a pull request for this branch" |
| Get help | "Explain what this code does" |

## Need help?

If you get stuck:

1. **Ask Claude** - paste the error and ask what it means
2. **Check the docs** - [claude.ai/code/docs](https://code.claude.com/docs/en/setup)
3. **Ask in Slack** - post in **#ai-designers** and mention **@const**

## Project structure

```
claude-for-designers/
├── README.md              # You are here
├── docs/
│   ├── 01-terminal-basics.md
│   ├── 02-git-basics.md
│   ├── 03-claude-code.md
│   └── 04-frontend-prototyping.md
└── exercises/
    ├── 01-terminal/
    ├── 02-git/
    └── 03-prototype/
```
