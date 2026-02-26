# Parth Choudhary's Personal Website

A clean, minimalist personal website built with Hugo and the Etch theme, hosted on GitHub Pages.

## Features

- **Blog**: Write posts in Markdown in the `content/posts/` directory
- **Projects**: Showcase your projects on the projects page
- **Clean Design**: Uses the Etch theme for a minimal, elegant layout

## Writing Posts

Create new blog posts in the `content/posts/` directory:

```markdown
+++
title = "Your Post Title"
date = 2026-02-26
categories = ["blog"]
draft = false
+++

Write your content here in Markdown.
```

## Local Development

1. Install Hugo (extended version recommended)
2. Run `hugo server` to start the local server
3. Open http://localhost:1313 in your browser

## Deployment

This site is automatically deployed to GitHub Pages via GitHub Actions. Simply push your changes to the `main` branch, and the site will be built and deployed automatically.

## Project Structure

```
├── content/
│   ├── posts/          # Blog posts (Markdown)
│   ├── about.md       # About page
│   └── projects.md    # Projects page
├── hugo.toml          # Hugo configuration
└── .github/workflows/ # GitHub Actions for deployment
```
