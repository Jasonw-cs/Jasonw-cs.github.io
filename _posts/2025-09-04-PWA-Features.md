---
layout: post
title: "Using PWA Features in Jykell Blog"
subtitle: "Progressive Web App features to load faster and feel like a native app."
date: 2025-09-04
author: "Jason-json"
catalog: true
header-img: "img/posts/legacys-dawn.png"
tags:
    - PWA
    - Tutorial
---

I'd like to build **Progressive Web App (PWA)** features right out of the box. Below is what I have done by now.

---

## The Core PWA Features in This Template

### 1. "Add to Home Screen" Capability

On supported browsers (like Chrome and Safari on mobile), users who visit your site frequently may get a prompt to "Add to Home Screen."

If they accept, your blog's icon will be added to their phone's home screen or their computer's desktop, just like a native app. When they launch it, it opens in its own window without the browser's address bar, providing a clean, focused reading experience.

### 2. Full Offline Access

Ever been on a subway or a plane with no internet and wished you could read a blog post? This template solves that.

The first time a user visits your site, a "Service Worker" script in the background automatically starts saving the pages they visit. If they later try to access your site while offline, two things can happen:

*   If they try to open a page they've **already visited**, it will load instantly from their device's storage.
*   If they try to open a **new page**, instead of an ugly browser error, they will see your site's custom, branded `offline.html` page.

### 3. Blazing-Fast Loading on Repeat Visits

The Service Worker uses **"Stale-While-Revalidate."**  When a user returns to a page they've already visited, the site will **instantly load the saved version** from their device (making it feel incredibly fast).

Meanwhile, in the background, it checks the server for any new content. If it finds an updated version of the page, it will quietly download it and update the cache for the *next* time the user visits. This gives you the perfect balance of speed and freshness.

---

## A Peek Under the Hood

The files to get the PWA features:

*   `pwa/manifest.json`: This is the "ID card" for your web app. It tells the browser the app's name, description, icon, and theme color.
*   `sw.js`: This is the **Service Worker**, the engine that powers everything. It's the script that intercepts network requests, manages the cache, and enables offline access.
*   `offline.html`: This is the custom page that is displayed when a user is offline and tries to access a page that hasn't been saved to their device.

---

## What You Need to Do: A 2-Step Customization Guide

To make the PWA features truly your own, you only need to customize two things.

#### Step 1: Customize the `manifest.json` File

Open `pwa/manifest.json` and edit the following fields to match your own blog:

```json
{
  "name": "Your Full Blog Name",
  "short_name": "Your Short Name",
  "description": "A great description of your blog.",
  "icons": [...],
  ...
}
```

#### Step 2: Create Your Own Icons

Your PWA needs icons to be displayed on the user's home screen. You'll need to create your own icon images and replace the placeholder ones. The two most important sizes are:

1.  **192x192 pixels:** A standard size for app icons.
2.  **512x512 pixels:** Used for the splash screen when your app loads.

Create your icons (PNG format is best) and replace the following files in the `/img/` directory:

*   `/img/android-chrome-192x192.png`
*   `/img/android-chrome-512x512.png`

```
