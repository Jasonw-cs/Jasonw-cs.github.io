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
    - Liquid
    - Fix
    - Notes
---

# Jekyll Liquid Syntax Fix

## The Problem
- Jekyll processes all curly braces `{{ }}` and percent tags as template code
- This breaks when you try to show code examples containing these characters
- Results in "Liquid syntax error" and failed builds

## The Solution
Wrap any problematic code in raw tags:

```
{% raw %}
Your code with {{ }} or {% %} here
{% endraw %}
```

## How to Apply the Fix

### For Inline Code
Wrap with raw tags:
```
{% raw %}`{{ your.code.here }}`{% endraw %}
```

### For Code Blocks
Wrap the entire block:
```
{% raw %}
```javascript
const obj = {{ key: 'value' }};
```
{% endraw %}
```

## Common Triggers
- JavaScript template literals with `${ }`
- Vue.js or Angular syntax with `{{ }}`
- Any code showing Jekyll/Liquid examples
- Handlebars templates

## Quick Fix Steps
1. Find the line causing the error
2. Wrap the problematic code with `{% raw %}` and `{% endraw %}`
3. Commit and push
4. Build should succeed

## Prevention
- Always use raw tags when documenting template syntax
- Test locally with `bundle exec jekyll serve` before pushing
- Keep code examples in separate files when possible
