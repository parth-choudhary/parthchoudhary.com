# Parth Choudhary's Personal Website

A clean, minimalist personal website built with Jekyll and hosted on GitHub Pages.

## Features

- **Blog**: Write posts in Markdown in the `_posts/` directory
- **Projects**: Showcase your projects on the projects page
- **Clean Design**: Uses the minima theme for a minimal, readable layout

## Writing Posts

Create new blog posts in the `_posts/` directory with the naming convention:
`YYYY-MM-DD-your-post-title.md`

Example frontmatter:
```yaml
---
layout: post
title: "Your Post Title"
date: 2026-02-23
categories: blog
---
```

## Local Development

1. Install Ruby and Bundler
2. Run `bundle install` to install dependencies
3. Run `bundle exec jekyll serve` to start the local server
4. Open http://localhost:4000 in your browser

## Deployment

This site is automatically deployed to GitHub Pages via GitHub Actions. Simply push your changes to the `main` branch, and the site will be built and deployed automatically.

## Project Structure

```
├── _posts/          # Blog posts (Markdown)
├── _config.yml      # Jekyll configuration
├── index.md         # Home page
├── projects.md     # Projects page
├── about.md        # About page
└── Gemfile          # Ruby dependencies
```
