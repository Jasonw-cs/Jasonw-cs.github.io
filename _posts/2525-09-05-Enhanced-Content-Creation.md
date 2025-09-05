---
layout: post
title: Enhanced Content Creation
subtitle: New Markdown and image features
date: 2025-09-05
author: Jason-json
header-img: img/posts/elden-ring.jpg
tags: [Jekyll, Refactor, Update, Features]
---

The "Jekyll Update Phase Two" plan is officially complete! The goal was to make content creation easier and more professional without fighting the limitations of Jekyll or GitHub Pages. This post serves as both a log of the changes and a guide on how to use these powerful new features.

---

## Part 1: The Refactoring Log

Here is a summary of the files that were created or modified to bring these new features to life.

#### 1. Configuration (`_config.yml`)
- **GFM Enabled**: We configured the `kramdown` markdown processor to use GitHub Flavored Markdown (`GFM`). This instantly enables features like task lists and better table handling.
- **Code Highlighting**: Settings for the `rouge` syntax highlighter were refined to enable line numbers on code blocks by default.

#### 2. Layout (`_includes/head.html`)
- **Math & Diagram Support**: We added CDN links for **MathJax** and **Mermaid.js**. This allows the browser to render complex math equations and flowcharts without requiring any special Jekyll plugins, ensuring full compatibility with GitHub Pages.

#### 3. New Image System
- **Reusable Components**: Two new include files were created:
  - `_includes/responsive-image.html`: For embedding a single, responsive image with an optional caption.
  - `_includes/image-gallery.html`: For creating a beautiful, grid-based image gallery.
- **Styling**: A new stylesheet, `css/custom-images.css`, was created to add styling for the new image containers, captions, and galleries. This was then linked in `_includes/head.html` to apply the styles globally.

---

## Part 2: How to Create New Content

This is the exciting part. Here’s how to use everything we just added.

### Enhanced Markdown Features

#### Task Lists
You can now create GitHub-style task lists, and they will render as checkboxes.
```markdown
- [x] Complete Phase One
- [x] Implement Enhanced Markdown
- [ ] Write a post about the new features
