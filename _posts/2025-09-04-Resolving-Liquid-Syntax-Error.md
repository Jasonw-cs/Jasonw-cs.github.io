---
layout:     post
title:      Jekyll-Specific Markdown Interactions
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

# Jekyll-Specific Markdown Interactions
Front Matter
Every Jekyll post or page must start with YAML Front Matter, enclosed by triple-dashed lines. This defines metadata like layout, title, date, categories, and tags.

---
layout: post
title: My First Jekyll Post
date: 2025-01-01 10:00:00 +0000
categories: [Jekyll, Markdown]
tags: [static site, blog]
---
Using Liquid in Markdown
Jekyll processes Liquid tags and objects within our Markdown files before converting them to HTML. This allows for dynamic content.

 {% raw %} 
Variables: {{ site.title }}, {{ page.title }}
Conditionals: {% if page.tags contains 'Jekyll' %} ... {% endif %}
Loops: {% for post in site.posts limit: 5 %} ... {% endfor %}
Crucial Note: Liquid syntax is processed by Jekyll. If we want to display Liquid syntax as literal text (e.g., in a code example within our post) instead of having Jekyll interpret it, we must escape it.

# Resolving the "Liquid Syntax Error: 'for' tag was never closed"

I encountered this error because 1 included examples of Liquid syntax (specifically {% for ... %}) directly in a Markdown list without escaping them. Jekyll attempted to parse these incomplete for tags, leading to a build failure.
Our mistake was similar to this:

*   **Loops:** `{% for post in site.posts %}` for iterating through posts.
    *   This would cause an error because `{% endfor %}` is missing.
The Solution:
To prevent Jekyll from interpreting Liquid code examples, we must wrap them in {% raw %}...{% endraw %} tags. This tells Jekyll to treat everything between raw and endraw as plain text, passing it directly to the output without processing.
The Fix in our Markdown file:
We changed lines like:

*   **Liquid Templating Language:** While not Ruby itself, Liquid is a templating language written in Ruby and used by Jekyll. We'll use Liquid syntax (e.g., `{{ page.title }}`, `{% for post in site.posts %}`) extensively for dynamic content in our Jekyll templates.
to:
*   **Liquid Templating Language:** While not Ruby itself, Liquid is a templating language written in Ruby and used by Jekyll. We'll use Liquid syntax (e.g., {% raw %}`{{ page.title }}`{% endraw %}, {% raw %}`{% for post in site.posts %}`{% endraw %}) extensively for dynamic content in our Jekyll templates.
By adding {% raw %} and {% endraw %} around the Liquid examples, Jekyll no longer tried to parse them, and the build succeeded.

Prevention Tip:
Always remember this rule when documenting Liquid or Jekyll syntax in Markdown:
For inline examples: Use {% raw %} and {% endraw %} around the Liquid tags.
For multi-line code blocks: Use fenced code blocks (```liquid) as this implicitly treats the content as code and prevents Liquid processing.
Understanding this distinction is key to smooth Jekyll development when sharing code examples.
{% endraw %} 
