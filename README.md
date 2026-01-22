# Claude for Designers

An interactive tutorial for OOZOU designers to learn terminal basics, Git, and Claude Code for
frontend prototyping.

## Prerequisites

Before starting, make sure you have:

- A Mac with macOS
- A GitHub account (create one at [github.com](https://github.com) if needed)
- VS Code installed ([download here](https://code.visualstudio.com))

## Getting started

### Step 1: Open Terminal

Press `Cmd + Space`, type "Terminal", and hit Enter. You'll see a window with a command prompt -
this is where you'll type commands.

Don't panic. The terminal is just a text-based way to talk to your computer. Think of it as
texting your Mac instead of clicking around.

### Step 2: Install Homebrew (the Mac package manager)

Copy and paste this into Terminal, then press Enter:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Follow the prompts. This installs Homebrew, which lets you install other tools easily.

After installation, run the commands shown in the terminal to add Homebrew to your PATH (usually
two commands starting with `echo` and `eval`).

### Step 3: Install the essential tools

```bash
brew install git gh node
```

This installs:
- **git** - version control (track changes to your code)
- **gh** - GitHub's command-line tool
- **node** - JavaScript runtime (needed for frontend tools)

### Step 4: Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

### Step 5: Set up GitHub authentication

```bash
gh auth login
```

Choose:
- GitHub.com
- HTTPS
- Yes (authenticate Git with GitHub credentials)
- Login with a web browser

### Step 6: Clone this repository

```bash
cd ~/Projects
git clone https://github.com/oozou/claude-for-designers.git
cd claude-for-designers
```

Note: Create the Projects folder first if it doesn't exist: `mkdir -p ~/Projects`

### Step 7: Start Claude Code

```bash
claude
```

You're now ready to start learning. Type your questions or requests to Claude directly.

## Tutorial modules

Work through these in order:

1. **[Terminal basics](docs/01-terminal-basics.md)** - Navigate your Mac like a pro
2. **[Git fundamentals](docs/02-git-basics.md)** - Track changes and collaborate
3. **[Claude Code workflow](docs/03-claude-code.md)** - AI-assisted development
4. **[Frontend prototyping](docs/04-frontend-prototyping.md)** - Tailwind, shadcn/ui, and rapid
   prototyping

## Quick reference

### Essential terminal commands

| Command | What it does | Example |
|---------|--------------|---------|
| `cd` | Change directory | `cd Projects` |
| `ls` | List files | `ls -la` |
| `pwd` | Print current directory | `pwd` |
| `mkdir` | Make directory | `mkdir my-project` |
| `code .` | Open VS Code here | `code .` |

### Essential Git commands

| Command | What it does |
|---------|--------------|
| `git status` | See what's changed |
| `git add .` | Stage all changes |
| `git commit -m "message"` | Save changes with a message |
| `git push` | Upload to GitHub |
| `git pull` | Download latest changes |

### Essential Claude Code commands

| Command | What it does |
|---------|--------------|
| `claude` | Start Claude Code |
| `/help` | Show available commands |
| `/clear` | Clear conversation |
| `Ctrl+C` | Cancel current operation |
| `Cmd+D` or type `exit` | Exit Claude Code |

## Need help?

If you get stuck:

1. **Read the error message** - it usually tells you what went wrong
2. **Ask Claude** - paste the error and ask what it means
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
