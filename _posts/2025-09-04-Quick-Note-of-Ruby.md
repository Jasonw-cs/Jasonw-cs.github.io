---
layout:     post
title:      Quick Note of Ruby
subtitle:   for Jekyll & GitHub Pages
date:       2025-09-04
author:     Jason-json
header-img: img/yukihiro-matsumoto-ruby.jpg
catalog: true
tags:
    - Ruby
    - Notes
---

# Ruby: A Brief Introduction for Jekyll & GitHub Pages

## What is Ruby?
Ruby is an open-source, dynamic, object-oriented programming language designed for programmer productivity and enjoyment. It was created by Yukihiro "Matz" Matsumoto in the mid-1990s (specifically, December 21, 1995).

## Strength and Challenges
**Strength:**
*   **Developer Friendly:** Emphasizes simplicity and productivity with a focus on human-friendly syntax.
*   **Object-Oriented:** Everything in Ruby is an object, promoting a clear and consistent programming paradigm.
*   **Strong Community & Ecosystem:** Particularly with Ruby on Rails, there's a vast collection of libraries (gems) and a supportive community.

**Challenges:**
*   **Performance:** Can be slower than some other languages (like Python, Java, or C++) for CPU-intensive tasks.
*   **Memory Consumption:** Ruby applications can sometimes consume more memory compared to those written in other languages.
*   **Steep Learning Curve :** While basic syntax is easy, mastering the nuances of Ruby and its ecosystem can take time. I think I will prioritize js, and recently I'm working on a React project which is really fast.

## Use Cases
Ruby is widely used for web development, especially with its Ruby on Rails framework, as well as for scripting, data processing, and automation.
*   **Shopify:** A leading e-commerce platform.
*   **GitHub:** The world's largest platform for software development.
*   **Airbnb:** A popular online marketplace for lodging.
*   **Basecamp:** A project management and team communication tool.
*   **SoundCloud:** An online audio distribution platform.

## First Ruby project for GitHub Users: Build GitHub Pages with Jekyll
For many GitHub users, our first practical encounter with Ruby is through Jekyll. Jekyll is a static site generator built with Ruby that takes plain text files (Markdown, Liquid) and renders them into static websites or blogs. GitHub Pages, GitHub's free static site hosting service, is powered by Jekyll. This allows us to easily publish websites directly from our GitHub repositories.

## Minimal Ruby Knowledge for a Jekyll Project
While we don't need to be a Ruby expert to use Jekyll, understanding a few core concepts will significantly help:
{% raw %}
1.  **Ruby Installation:**
    *   We need a working Ruby environment on our machine.
    *   Tools like `rbenv` or `RVM` (Ruby Version Manager) are often used by developers to manage multiple Ruby versions, but for a simple Jekyll project, a direct system installation might suffice depending on our OS.
    *   Verify our installation by running `ruby -v` in our terminal.

2.  **Gems and Gem Installation:**
    *   Ruby libraries are called "gems." Jekyll itself is a gem.
    *   We install gems using the `gem install` command, e.g., `gem install jekyll bundler`.
    *   `Bundler` is a gem that manages other gems and their dependencies for our project, ensuring consistent environments.

3.  **Using Bundler:**
    *   After installing `bundler`, we'll typically have a `Gemfile` in our Jekyll project. This file lists all the gems our project needs.
    *   Run `bundle install` in our project's root directory to install all dependencies specified in the `Gemfile`.
    *   Always run Jekyll commands using `bundle exec`. For example, instead of `jekyll serve`, use `bundle exec jekyll serve`. This ensures that Jekyll runs with the exact gem versions defined in our project's `Gemfile.lock`, preventing conflicts.

4.  **Basic Ruby Syntax (for Configuration and Templating):**
    *   **YAML:** Jekyll configuration files (`_config.yml`) are written in YAML, which maps easily to Ruby hashes. Understanding key-value pairs and basic indentation is crucial.
    *   **Variables:** Ruby uses `variable_name = value` for assignment.
    *   **Hashes (Dictionaries):** Ruby hashes store key-value pairs (e.g., `{ key: "value" }`). In YAML, `key: value` is directly interpreted into a Ruby hash when Jekyll processes it.
    *   **Arrays:** Ordered lists of items, e.g., `["item1", "item2"]`.
    *   **Liquid Templating Language:** While not Ruby itself, Liquid is a templating language written in Ruby and used by Jekyll. We'll use Liquid syntax (e.g., `{{ page.title }}`, `{% for post in site.posts %}`) extensively for dynamic content in our Jekyll templates. Understanding how Liquid accesses Jekyll's site, page, and post data (which are Ruby objects/hashes) is key.
{% endraw %}


### Installation Considerations
For Windows users, native Ruby installations can sometimes present challenges with certain gems that have native extensions. 
This is not mandatory but recommanded: We can use the Windows Subsystem for Linux (WSL), which provides a Linux environment where Ruby and Jekyll can be installed and run more smoothly, mirroring a typical development setup on Linux or macOS. 

## Ruby Resources for Beginners
*   **Official Ruby Website:** [ruby-lang.org](https://www.ruby-lang.org/en/)
*   **Try Ruby:** [try.ruby-lang.org](https://try.ruby-lang.org/)
*   **Ruby Koans:** [rubykoans.com](http://rubykoans.com/)
*   **Learn Ruby the Hard Way:** [learnrubythehardway.org](https://learnrubythehardway.org/)
*   **Codecademy Ruby:** [codecademy.com/learn/learn-ruby](https://www.codecademy.com/learn/learn-ruby)
*   **freeCodeCamp Ruby:** [freecodecamp.org/news/tag/ruby/](https://www.freecodecamp.org/news/tag/ruby/)
*   **Jekyll Docs:** [jekyllrb.com/docs/](https://jekyllrb.com/docs/)
