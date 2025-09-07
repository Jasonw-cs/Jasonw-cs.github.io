---
layout: post
title: Enhanced Content Creation
subtitle: New Markdown and image features
date: 2025-09-05
author: Jason-json
catalog: true
header-img: img/posts/elden-ring.jpg
tags: 
    - Log
    - Updates
---

## The Refactoring Log

## 1. Configuration (`_config.yml`)
- **GFM Enabled**: We configured the `kramdown` markdown processor to use GitHub Flavored Markdown (`GFM`). This instantly enables features like task lists and better table handling.
- **Code Highlighting**: Settings for the `rouge` syntax highlighter were refined to enable line numbers on code blocks by default.

## 2. Layout (`_includes/head.html`)
- **Math & Diagram Support**: We added CDN links for **MathJax** and **Mermaid.js**. This allows the browser to render complex math equations and flowcharts without requiring any special Jekyll plugins, ensuring full compatibility with GitHub Pages.

## 3. New Image System
- **Reusable Components**: Two new include files were created:
  - `_includes/responsive-image.html`: For embedding a single, responsive image with an optional caption.
  - `_includes/image-gallery.html`: For creating a beautiful, grid-based image gallery.
- **Styling**: A new stylesheet, `css/custom-images.css`, was created to add styling for the new image containers, captions, and galleries. This was then linked in `_includes/head.html` to apply the styles globally.
