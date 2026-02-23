# Website Usage Guide

This guide explains how to manage this Jekyll-based personal website. OpenCLAW (or any AI assistant) should follow these instructions when making changes.

---

## Site Overview

- **Theme**: Minima (clean, minimalist design)
- **Framework**: Jekyll (static site generator)
- **Hosting**: GitHub Pages
- **Content Format**: Markdown (.md files)

---

## File Structure

```
parthchoudhary.com/
├── _posts/              # Blog posts (Markdown files)
├── _config.yml         # Site configuration
├── index.md            # Homepage
├── about.md            # About page
├── projects.md         # Projects page
├── README.md           # Project documentation
├── USAGE.md            # This file
└── .github/workflows/  # GitHub Actions for deployment
```

---

## How to Add a New Blog Post

### Step 1: Create the post file

Create a new file in the `_posts/` directory with the naming convention:
`YYYY-MM-DD-your-post-title.md`

Example: `_posts/2026-02-24-my-first-project.md`

### Step 2: Add frontmatter and content

```yaml
---
layout: post
title: "My First Project"
date: 2026-02-24
categories: blog
---

Write your blog post content here in Markdown.

## Section Heading

Paragraph text here.

- Bullet point 1
- Bullet point 2
```

### Frontmatter Fields

| Field | Required | Description |
|-------|----------|-------------|
| `layout` | Yes | Use `post` for blog posts |
| `title` | Yes | Title of your post |
| `date` | Yes | Publication date (YYYY-MM-DD format) |
| `categories` | No | Categories like `blog`, `tech`, `personal` |

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

### Step 1: Edit projects.md

Open `projects.md` and add your project in this format:

```markdown
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
- **GitHub**: [Source Code](https://github.com/parthchoudhary/todo-app)
```

---

## How to Update the About Page

### Edit about.md

Open `about.md` and modify the content. The frontmatter should remain:

```yaml
---
layout: page
title: About
permalink: /about/
---
```

Simply edit the Markdown content below the frontmatter.

---

## How to Update Site Configuration

### Edit _config.yml

Common settings to modify:

```yaml
title: Your Name           # Site title
email: you@example.com    # Your email
description: Your description
url: "https://yourdomain.com"
github_username: your-username
twitter_username: your-username
```

After modifying `_config.yml`, restart the local server for changes to take effect.

---

## Local Development

To preview changes locally:

```bash
# Install dependencies
bundle install

# Start local server
bundle exec jekyll serve

# View at http://localhost:4000
```

---

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch via GitHub Actions.

To deploy:
1. Commit your changes
2. Push to GitHub
3. Go to Repository → Actions to monitor deployment
4. Site will be live at `https://your-username.github.io/repository-name`

---

## Adding Images

### Option 1: External URL
Use any image hosting service (Imgur, Cloudinary, etc.):
```markdown
![Description](https://example.com/image.jpg)
```

### Option 2: Add to repository
1. Create an `assets/images/` directory
2. Add your image there
3. Reference it:
```markdown
![Description](/assets/images/your-image.png)
```

---

## Quick Reference for OpenCLAW

When asked to add a blog post:
1. Create file in `_posts/` with date prefix
2. Use `layout: post` in frontmatter
3. Write content in Markdown

When asked to add a project:
1. Edit `projects.md`
2. Add project entry with name, description, tech stack, links

When asked to change site settings:
1. Edit `_config.yml`
2. Restart jekyll serve to see changes locally
