# Jekyll Blog Starter for GitHub Pages

This project is my attempt to build an easy-to-use Jekyll blog template. It began as a fork of the excellent [Hux Blog theme](https://github.com/Huxpro/huxpro.github.io) and has been heavily refactored to fit the beginners as myself.

It's designed to be forked and deployed on GitHub Pages with minimal setup, making it a great starting point for a personal blog or project site. This is still a work in progress.

**[Live Demo](https://jasonw-cs.github.io/)**

---

## Key Features

This template comes with a number of features built-in:

*   **Enhanced Markdown Support**: Go beyond basic Markdown with support for:
    *   Math Equations (via MathJax)
    *   Diagrams and Flowcharts (via Mermaid.js)
    *   Task Lists (`- [x]`)
*   **Image Galleries**: A simple-to-use include for creating responsive image galleries in your posts.
*   **Progressive Web App (PWA) Features**:
    *   Offline access for visited pages.
    *   A custom "offline" page.
    *   "Add to Home Screen" capability on mobile devices.
*   **Automatic Table of Contents**: For long posts, an auto-generating catalog appears on the side to help with navigation. Just set `catalog: true` in your post's front matter.
*   **SEO Ready**:
    *   Uses the `jekyll-seo-tag` plugin for optimized meta tags.
    *   Simple setup for a default social preview (Open Graph) image for your entire site and for individual posts.
*   **Clean & Responsive Design**: A minimalist design that looks great on both desktop and mobile devices.

---

## Getting Started

Getting your own copy of this blog up and running is simple.

#### 1. Fork the Repository
Click the "Fork" button at the top right of this page to create a copy of this project in your own GitHub account.

#### 2. Enable GitHub Pages
Go to your new repository's settings page (`Settings` > `Pages`). Under "Build and deployment," select the following:
*   **Source**: `Deploy from a branch`
*   **Branch**: `main` and `/ (root)`
GitHub will then build and deploy your site. It will be available at `https://your-username.github.io/your-repository-name/`.

#### 3. Configure `_config.yml`
This is the main control panel for your site. Open the `_config.yml` file and edit the main settings to match your own details:
*   `title:`
*   `SEOTitle:`
*   `description:`
*   `url:` 
*   `github_username:`

#### 4. Start Writing!
You can now create your own posts.
*   Add new Markdown files (`.md`) to the `_posts` directory.
*   Make sure to follow the naming convention: `YYYY-MM-DD-your-post-title.md`.
*   Copy the front matter (the block between the `---` lines) from an existing post to get started.

---

## Customization

*   **Navigation Links:** The links in the main navigation bar are controlled by the `navigation:` list in `_config.yml`.
*   **Social Preview Image:**
    *   To set the default image for your entire site, create a 1200x630 pixel image and link to it in the `logo:` variable in `_config.yml`.
    *   To set the image for your repository link, go to the repository settings page and upload an image under "Social preview."

## Acknowledgements

This theme would not be possible without the foundational work done by **Huxpro** on the original Hux Blog theme. This project is a refactor and evolution of that excellent starting point.

## License

This project is open source and available under the [MIT License](LICENSE).
```
