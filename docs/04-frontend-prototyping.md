# Frontend prototyping

This guide covers the modern tools for rapid frontend prototyping. You'll learn to scaffold
projects and build UIs quickly using Tailwind CSS and shadcn/ui.

## The modern frontend stack

### Tailwind CSS

A utility-first CSS framework. Instead of writing custom CSS, you apply pre-built classes directly
to elements:

```html
<!-- Traditional CSS approach -->
<button class="primary-button">Click me</button>
<style>
  .primary-button {
    background-color: blue;
    color: white;
    padding: 12px 24px;
    border-radius: 8px;
  }
</style>

<!-- Tailwind approach -->
<button class="bg-blue-500 text-white px-6 py-3 rounded-lg">Click me</button>
```

Why Tailwind?
- No switching between HTML and CSS files
- Consistent spacing, colors, and sizing
- Responsive design built in
- Easy to iterate quickly

### shadcn/ui

A collection of beautifully designed, accessible components you can copy into your project. Not a
component library you install - you own the code and can customize everything.

Components include:
- Buttons, inputs, cards
- Dialogs, popovers, tooltips
- Data tables, forms
- Navigation menus
- And much more

## Setting up a new project

In Claude Code ([claude.ai/code](https://claude.ai/code)), just ask for what you need:

```
Create a new Vite project with React, TypeScript, and Tailwind CSS
```

Claude handles all the setup for you.

### Adding shadcn/ui

Ask Claude:

```
Add shadcn/ui to this project with the button, card, and input components
```

Claude will install and configure everything.

## Tailwind CSS essentials

### Spacing

Tailwind uses a consistent spacing scale. The number represents 0.25rem increments:

| Class | Value |
|-------|-------|
| `p-1` | 4px padding |
| `p-2` | 8px padding |
| `p-4` | 16px padding |
| `p-6` | 24px padding |
| `p-8` | 32px padding |

Directions:
- `p-4` - padding all sides
- `px-4` - padding left and right
- `py-4` - padding top and bottom
- `pt-4` - padding top only
- `pl-4` - padding left only

Same pattern for margin: `m-4`, `mx-4`, `my-4`, `mt-4`, etc.

### Colors

Tailwind has a default color palette with shades from 50 (lightest) to 950 (darkest):

```html
<div class="bg-blue-500 text-white">Blue background</div>
<div class="bg-gray-100 text-gray-900">Light gray background</div>
<div class="border border-red-500">Red border</div>
```

Common colors: `slate`, `gray`, `zinc`, `red`, `orange`, `yellow`, `green`, `blue`, `purple`, `pink`

### Typography

```html
<h1 class="text-4xl font-bold">Large bold heading</h1>
<p class="text-base text-gray-600">Normal paragraph text</p>
<span class="text-sm text-gray-400">Small muted text</span>
```

Sizes: `text-xs`, `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`

Weights: `font-normal`, `font-medium`, `font-semibold`, `font-bold`

### Flexbox

```html
<div class="flex items-center justify-between gap-4">
  <span>Left</span>
  <span>Right</span>
</div>
```

- `flex` - enable flexbox
- `items-center` - vertical center
- `justify-between` - space between items
- `justify-center` - horizontal center
- `gap-4` - gap between items
- `flex-col` - stack vertically

### Grid

```html
<div class="grid grid-cols-3 gap-4">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

- `grid-cols-2`, `grid-cols-3`, `grid-cols-4` - number of columns
- `col-span-2` - span multiple columns

### Responsive design

Prefix any class with a breakpoint:

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
  <!-- 1 column on mobile, 2 on tablet, 3 on desktop -->
</div>
```

Breakpoints:
- `sm:` - 640px and up
- `md:` - 768px and up
- `lg:` - 1024px and up
- `xl:` - 1280px and up

### Hover and focus states

```html
<button class="bg-blue-500 hover:bg-blue-600 focus:ring-2 focus:ring-blue-300">
  Hover me
</button>
```

### Common patterns

**Centered container:**
```html
<div class="max-w-4xl mx-auto px-4">
  Content here
</div>
```

**Card:**
```html
<div class="bg-white rounded-lg shadow-md p-6">
  Card content
</div>
```

**Button:**
```html
<button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-md transition-colors">
  Click me
</button>
```

**Input:**
```html
<input
  type="text"
  class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
  placeholder="Enter text..."
/>
```

## shadcn/ui components

### Using components

After Claude adds a component, import and use it in your code:

```tsx
import { Button } from "@/components/ui/button"

export function MyComponent() {
  return (
    <Button variant="default">Click me</Button>
  )
}
```

### Common components

**Button variants:**
```tsx
<Button variant="default">Primary</Button>
<Button variant="secondary">Secondary</Button>
<Button variant="outline">Outline</Button>
<Button variant="ghost">Ghost</Button>
<Button variant="destructive">Delete</Button>
```

**Card:**
```tsx
import { Card, CardHeader, CardTitle, CardDescription, CardContent } from "@/components/ui/card"

<Card>
  <CardHeader>
    <CardTitle>Card Title</CardTitle>
    <CardDescription>Card description goes here</CardDescription>
  </CardHeader>
  <CardContent>
    <p>Card content</p>
  </CardContent>
</Card>
```

**Input with label:**
```tsx
import { Input } from "@/components/ui/input"
import { Label } from "@/components/ui/label"

<div className="space-y-2">
  <Label htmlFor="email">Email</Label>
  <Input id="email" type="email" placeholder="you@example.com" />
</div>
```

### Customizing components

shadcn/ui components live in your `components/ui` folder. You own the code - edit them directly:

```tsx
// components/ui/button.tsx
// Change default styles, add new variants, etc.
```

## Prototyping workflow

### 1. Start with structure

Ask Claude:
```
Create a dashboard layout with:
- A sidebar on the left (250px wide)
- A header at the top
- Main content area
Use Tailwind CSS
```

### 2. Add components

```
Add a stats section at the top of the main area with 4 cards showing:
- Total Users
- Revenue
- Active Projects
- Pending Tasks
Use shadcn/ui Card components
```

### 3. Make it responsive

```
Make the sidebar collapse to a hamburger menu on mobile
```

### 4. Add interactivity

```
Add a dropdown menu to the user avatar in the header with options for
Profile, Settings, and Logout
```

### 5. Polish

```
Add hover states and transitions to make it feel more polished
```

## Exercise: Build a prototype

Create a simple dashboard using Claude Code:

1. Go to [claude.ai/code](https://claude.ai/code)

2. Ask Claude to scaffold it:
   ```
   Create a Vite + React + TypeScript project with Tailwind CSS and shadcn/ui.
   Set up the basic configuration.
   ```

3. Build the layout:
   ```
   Create a dashboard layout with a sidebar containing navigation links
   (Dashboard, Projects, Team, Settings) and a main content area.
   ```

4. Add content:
   ```
   Add a grid of 4 stat cards at the top and a table of recent projects below.
   Use shadcn/ui components.
   ```

5. Preview your work in Claude Code's preview pane

6. Refine with Claude:
   ```
   The cards need more padding and the table should have alternating row colors
   ```

## Tips for designers

### Translating designs to Tailwind

When you have a Figma design:

1. **Note the spacing** - Convert px to Tailwind scale (divide by 4)
   - 8px = `p-2`
   - 16px = `p-4`
   - 24px = `p-6`

2. **Match colors** - Use Tailwind's palette or add custom colors
   - Tell Claude: "Add a custom color called 'brand' with value #6366F1"

3. **Get the typography right**
   - Font sizes, weights, line heights
   - Tell Claude your exact values

### When to use what

**Use Tailwind directly when:**
- Building simple, custom layouts
- You need full control over every detail
- The design is unique

**Use shadcn/ui when:**
- You need common UI patterns (forms, dialogs, tables)
- You want accessible components out of the box
- You're prototyping quickly and can customize later

### Keeping things organized

For larger prototypes, organize your components:

```
src/
├── components/
│   ├── ui/           # shadcn/ui components
│   ├── layout/       # Header, Sidebar, Footer
│   └── features/     # Feature-specific components
├── pages/            # Page components
└── styles/           # Global styles
```

## Resources

- [Tailwind CSS docs](https://tailwindcss.com/docs)
- [shadcn/ui docs](https://ui.shadcn.com)
- [Tailwind CSS cheat sheet](https://nerdcave.com/tailwind-cheat-sheet)

## Getting help

If you're stuck:

1. **Describe what you see vs. what you want** - "The button is at the top but I want it at the
   bottom right"
2. **Share your screen or screenshot** - Visual context helps
3. **Ask in #ai-designers** - Mention **@const** for help

Happy prototyping!
