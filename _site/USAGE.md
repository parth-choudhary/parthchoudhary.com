# Website Usage Guide

This guide explains how to manage this Hugo-based personal website. OpenCLAW (or any AI assistant) should follow these instructions when making changes.

---

## Site Overview

- **Theme**: Etch (clean, minimalist design)
- **Framework**: Hugo (static site generator)
- **Hosting**: GitHub Pages
- **Content Format**: Markdown (.md files)

---

## File Structure

```
parthchoudhary.com/
├── content/
│   ├── posts/              # Blog posts (Markdown files)
│   ├── about.md           # About page
│   └── projects.md        # Projects page
├── hugo.toml              # Site configuration
├── README.md              # Project documentation
├── USAGE.md               # This file
└── .github/workflows/     # GitHub Actions for deployment
```

---

## How to Add a New Blog Post

### Step 1: Create the post file

Create a new file in the `content/posts/` directory.

Example: `content/posts/my-first-post.md`

### Step 2: Add frontmatter and content

```markdown
+++
title = "My First Post"
date = 2026-02-26
categories = ["blog"]
draft = false
+++

Write your blog post content here in Markdown.

## Section Heading

Paragraph text here.

- Bullet point 1
- Bullet point 2
```

### Frontmatter Fields

| Field | Required | Description |
|-------|----------|-------------|
| `title` | Yes | Title of your post |
| `date` | Yes | Publication date (YYYY-MM-DD format) |
| `categories` | No | Categories like `["blog"]`, `["tech"]` |
| `draft` | No | Set to `true` to hide from production |
| `tags` | No | Array of tags like `["tag1", "tag2"]` |

### Supported Markdown Features

- **Headings**: Use `#`, `##`, `###`
- **Bold**: `**text**`
- *Italic*: `*text*`
- Links: `[text](url)`
- Code blocks: ``` ```language
- Lists: `- item` or `1. item`
- Images: `![alt](image-url)`

---

## How to Add a New Project

### Step 1: Edit content/projects.md

Open `content/projects.md` and add your project in this format:

```markdown
+++
title = "Projects"
date = 2026-02-23
draft = false
+++

# My Projects

## Project Name

Brief description of what the project does.

- **Tech Stack**: List technologies used
- **Link**: [View Project](project-url) or leave out if no link
- **GitHub**: [Source Code](github-url)
```

### Example Project Entry

```markdown
## My Todo App

A simple todo list application built with React.

- **Tech Stack**: React, Node.js, MongoDB
- **Live Demo**: [View App](https://my-todo-app.com)
- **GitHub**: [Source Code](https://github.com/parth-choudhary/todo-app)
```

---

## How to Update the About Page

### Edit content/about.md

Open `content/about.md` and modify the content. The frontmatter should remain:

```markdown
+++
title = "About"
date = 2026-02-23
draft = false
+++
```

Simply edit the Markdown content below the frontmatter.

---

## How to Update Site Configuration

### Edit hugo.toml

Common settings to modify:

```toml
baseURL = 'https://parth-choudhary.github.io/'
title = 'Parth Choudhary'

[params]
  description = 'Your description'
  author = 'Your Name'
  github = 'your-username'
  email = 'your@email.com'
```

---

## Local Development

To preview changes locally:

```bash
# Install Hugo (extended version)
# macOS: brew install hugo
# Linux: apt install hugo
# Windows: choco install hugo

# Start local server
hugo server

# View at http://localhost:1313
```

---

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch via GitHub Actions.

To deploy:
1. Commit your changes
2. Push to GitHub
3. Go to Repository → Actions to monitor deployment
4. Site will be live at `https://parth-choudhary.github.io/repository-name`

---

## Adding Images

### Option 1: External URL
Use any image hosting service:
```markdown
![Description](https://example.com/image.jpg)
```

### Option 2: Add to repository
1. Add your image to `static/` directory
2. Reference it:
```markdown
![Description](/image.jpg)
```

---

## Quick Reference for OpenCLAW

When asked to add a blog post:
1. Create file in `content/posts/` with descriptive name
2. Use frontmatter with `title`, `date`, `categories`
3. Set `draft = false` to publish

When asked to add a project:
1. Edit `content/projects.md`
2. Add project entry with name, description, tech stack, links

When asked to change site settings:
1. Edit `hugo.toml`
2. Run `hugo server` locally to preview changes

When asked to build for production:
1. Run `hugo --minify`
2. Output goes to `public/` directory
3. GitHub Actions handles this automatically on push
