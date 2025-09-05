---
layout:     post
title:      Jekyll Markdown & Liquid Syntax
subtitle:   Quick Guide to Avoid Syntax Errors
date:       2025-09-05
author:     Jason-json
header-img: img/Victorious-Knight.jpg
catalog: true
tags:
    - Jekyll
    - Markdown
    - Liquid
    - Notes
---

# Jekyll Markdown & Liquid Syntax

## Markdown Basics
- **Headings**: Use `#` for H1, `##` for H2, etc.
- **Emphasis**: `*italic*` and `**bold**`
- **Lists**: `*` for bullets, `1.` for numbers
- **Links**: `[text](url)`
- **Code**: `` `inline` `` or fenced blocks with ``` 

## Jekyll Front Matter
- **What**: YAML metadata at top of every post/page.
- **Format**:
  ```yaml
  ---
  layout: post
  title: My Post
  date: 2025-01-01
  tags: [jekyll, markdown]
  ---
  ```

## Liquid Templating
- **Variables**: {% raw %}`{{ site.title }}`{% endraw %}, {% raw %}`{{ page.title }}`{% endraw %}
- **Conditionals**: {% raw %}`{% if condition %} ... {% endif %}`{% endraw %}
- **Loops**: {% raw %}`{% for item in collection %} ... {% endfor %}`{% endraw %}

## Critical: Liquid Syntax Errors
- **Problem**: Jekyll processes `{{ }}` and `{% %}` as template code
- **Error**: "Liquid syntax error: 'for' tag was never closed"
- **Solution**: Wrap examples in {% raw %}`{% raw %}`{% endraw %} tags

## Fix Examples
- **Wrong**: `Use` {% raw %}`{{ page.title }}`{% endraw %} `for titles` (without raw tags)
- **Correct**: `Use` {% raw %}`{{ page.title }}`{% endraw %} `for titles` (with raw tags)
- **Code blocks**:
  {% raw %}
  ```
  {% raw %}
  ```liquid
  {% for post in site.posts %}
    {{ post.title }}
  {% endfor %}
  ```
  {% endraw %}
  ```
  {% endraw %}

## Quick Reference
- **Inline Liquid**: Wrap with `raw` and `endraw` tags
- **Code blocks**: Use `raw` tags around entire block
- **Regular code**: Standard ``` blocks work fine
- **Rule**: Always escape Liquid examples to prevent build errors
