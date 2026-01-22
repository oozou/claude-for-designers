# Claude Code workflow

Claude Code is an AI assistant that helps you write code. It runs in your browser at
[claude.ai/code](https://claude.ai/code) - no installation needed. Think of it as pair programming
with an AI that can read your files, write code, and run commands.

## Getting started

1. Go to **[claude.ai/code](https://claude.ai/code)**
2. Log in with your Claude account
3. You're ready to start building

## The interface

Claude Code shows you:
- A chat interface where you type requests
- A file browser showing your project
- A preview pane for viewing your work
- A terminal for running commands

## Basic interaction

Just type what you want to do in natural language:

```
Create a simple HTML page with a blue header
```

Claude will:
1. Understand your request
2. Create or edit files
3. Show you what it's doing
4. Ask for confirmation on important actions

### Asking questions

```
What does this function do?
```

```
Explain the folder structure of this project
```

```
Why am I getting this error? [paste error]
```

### Making changes

```
Add a dark mode toggle to the header
```

```
Fix the CSS so the button is centered
```

```
Refactor this component to use Tailwind classes
```

## Working with projects

### Creating a new project

```
Create a new project called "my-landing-page" with HTML, CSS, and Tailwind
```

Claude will set up the project structure for you.

### Opening an existing project

```
Clone https://github.com/oozou/claude-for-designers
```

Or connect your GitHub account and browse your repositories.

## Working with files

Claude can read and modify your project files. Be specific about what you want:

**Good requests:**
- "Create a new file called `components/Header.tsx` with a responsive header"
- "In `index.html`, change the background color to dark gray"
- "Add a footer to the bottom of `pages/home.tsx`"

**Vague requests (Claude will ask for clarification):**
- "Make it look better" - better how?
- "Fix the layout" - what's wrong with it?

## Git integration

Claude handles Git operations for you. No need to memorize commands.

### Committing changes

```
Commit these changes with an appropriate message
```

Claude will:
1. Check what's changed
2. Stage the relevant files
3. Write a commit message
4. Create the commit

### Creating pull requests

```
Create a pull request for this branch
```

Claude will:
1. Push your branch to GitHub
2. Create a PR with a title and description
3. Give you the PR link

### Other Git operations

```
What's changed since my last commit?
```

```
Create a new branch called feature/new-header
```

```
Show me the recent commits
```

## Workflow example

Here's a typical workflow:

### 1. Start a new feature

```
Create a new branch called feature/contact-form
```

### 2. Build the feature

```
Create a contact form component with fields for name, email, and message.
Use Tailwind CSS for styling. Include form validation.
```

### 3. Preview your work

Claude shows a live preview. Check it looks right.

### 4. Iterate

```
Make the form more compact and add a success message after submission
```

### 5. Commit and push

```
Commit these changes and create a pull request
```

## Best practices

### Be specific

Instead of:
```
Make a button
```

Try:
```
Create a primary button component with:
- Blue background (#3B82F6)
- White text
- Rounded corners
- Hover state that darkens the background
- Padding of 12px vertical, 24px horizontal
```

### Provide context

```
I'm building a dashboard for tracking expenses. Create a card component
that shows the category name, total amount, and a small bar chart.
```

### Ask for explanations

```
Explain what this code does before making changes
```

```
Why did you choose this approach?
```

### Review changes before accepting

Claude shows you what it's about to do. Read it before confirming. If something
looks wrong, say:

```
Wait, don't do that. Instead, try...
```

### Iterate

Don't try to get everything perfect in one prompt. Build incrementally:

1. Get the basic structure
2. Refine the styling
3. Add interactions
4. Handle edge cases

## Common tasks for designers

### Converting designs to code

```
Here's what I need:
- A card with rounded corners (8px)
- Drop shadow
- White background
- 24px padding
- Title in bold 18px
- Description in gray 14px
- A "Learn more" link at the bottom
```

### Responsive adjustments

```
Make this layout stack vertically on mobile (below 768px)
```

### Adding animations

```
Add a subtle fade-in animation when the modal opens
```

### Color/styling changes

```
Change the primary color from blue to purple throughout the component
```

## Troubleshooting

### Claude seems stuck

Click the stop button or refresh the page, then try rephrasing your request.

### Claude made a mistake

Just tell it:
```
That's not quite right. The button should be on the right side, not the left.
```

### You want to undo changes

```
Undo the last change you made to Header.tsx
```

Or ask Claude to use Git:
```
Revert the last commit
```

### Claude is asking too many questions

Be more specific upfront:
```
Create a login form. Use email and password fields. Style it with Tailwind.
Center it on the page. Don't ask questions, just make reasonable choices.
```

## Exercise: Build with Claude Code

1. Go to [claude.ai/code](https://claude.ai/code)

2. Create a new project:
   ```
   Create a new project called "my-first-page" with a basic HTML file and Tailwind CSS
   ```

3. Build a page:
   ```
   Create a simple HTML page with a navigation bar
   ```

   ```
   Add three cards below the navigation with placeholder content
   ```

   ```
   Make it responsive using CSS Grid
   ```

4. Save your work:
   ```
   Commit this as "Initial page layout"
   ```

5. View the preview to see your result

## Next steps

Continue to [Frontend prototyping](04-frontend-prototyping.md) to learn about Tailwind and
shadcn/ui.
