---
layout:     post
title:      Jekyll-Specific Markdown
subtitle:   Resolving Liquid Syntax Error
date:       2025-09-04
author:     Jason-json
header-img: img/elden-ring.JPG
catalog: true
tags:
    - Markdown
    - Liquid
    - Notes
---

# Jekyll-Specific Markdown
Front Matter
Every Jekyll post or page must start with YAML Front Matter, enclosed by triple-dashed lines. This defines metadata like layout, title, date, categories, and tags.

Using Liquid in Markdown
Jekyll processes Liquid tags and objects within our Markdown files before converting them to HTML. This allows for dynamic content.

# Resolving the "Liquid Syntax Error: 'for' tag was never closed"
 
I encountered this error because 1 included examples of Liquid syntax (specifically {% for ... %}) directly in a Markdown list without escaping them. Jekyll attempted to parse these incomplete for tags, leading to a build failure.
The Solution:
{% raw %}
Always remember this rule when documenting Liquid or Jekyll syntax in Markdown:
For inline examples: Use "{% raw %}" and "{% endraw %}" around the Liquid tags.
For multi-line code blocks: Use fenced code blocks (```liquid) as this implicitly treats the content as code and prevents Liquid processing.
Understanding this distinction is key to smooth Jekyll development when sharing code examples.
{% endraw %} 
