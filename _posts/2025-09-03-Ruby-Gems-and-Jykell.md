---
layout:     post
title:      Ruby, Gems, and Jekyll
subtitle:   Descriptions and How to Install
date:       2025-09-03
author:     Jason-json
header-img: img/futuristic-spaceport.webp
catalog: true
tags:
    - Ruby
    - Jekyll
    - Gems
    - Notes
---

# Ruby, Gems, and Jekyll

## Ruby
- **What**: Open-source programming language.
- **Use**: Powers Jekyll; general-purpose scripting, web development.
- **Install**:
  - Download: [ruby-lang.org](https://www.ruby-lang.org/en/downloads/)
  - Verify: `ruby -v`

## Gems
- **What**: Ruby package manager (libraries/tools).
- **Use**: Add features to Ruby; manage project dependencies.
- **Install**:
  - Comes with Ruby.
  - Update: `gem update --system`
  - Install a gem: `gem install [gem-name]`

## Jekyll
- **What**: Static site generator (Ruby-based).
- **Use**: Build blogs/websites from Markdown/HTML templates.
- **Install**:
  ```bash
  gem install bundler jekyll
  ```
- **Create site**:
  ```bash
  jekyll new [site-name]
  cd [site-name]
  ```
- **Run locally**:
  ```bash
  bundle exec jekyll serve
  ```
- **Deploy**: Push to GitHub repo; enable GitHub Pages in settings.
```