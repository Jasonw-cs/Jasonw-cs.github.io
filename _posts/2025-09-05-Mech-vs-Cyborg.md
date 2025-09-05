---
layout:     post
title:      How to Create Gallery
subtitle:   "Battle in a futuristic city"
date:       2025-09-05
author:     Jason-json
header-img: "img/futuristic-spaceport.webp"
catalog: true
tags:
    - Gallery
gallery_items:
  - name: "cyborg-vs-mech-1.jpg"
    alt: "A dynamic close-up of the cyborg wizard deflecting a laser blast from the mech."
    caption: "Dynamic Close-Up"
  - name: "cyborg-vs-mech-2.jpg"
    alt: "A wide cityscape shot showing the massive scale of the mech warrior battling the wizard among skyscrapers."
    caption: "Epic Cityscape Battle"
  - name: "cyborg-vs-mech-3.jpg"
    alt: "A dramatic low-angle view looking up at the towering mech as it prepares to strike."
    caption: "Dramatic Low Angle"
  - name: "cyborg-vs-mech-4.jpg"
    alt: "An intense mid-action shot of both the mech and cyborg charging their energy weapons."
    caption: "Intense Mid-Action"
---

This a template of galley:

{% include image-gallery.html images=page.gallery_items path="/img/gallery/cyborg-vs-mech/" %}

You can write the text of your blog post, paragraphs like normal, before and/or after the gallery.

### How to Create an Image Gallery

**Step 1: Prepare & Upload Images**

1.  Create a new folder for your gallery (e.g., `/img/gallery/my-new-gallery/`).
2.  Optimize your images (use lowercase `.jpg` or `.png` files).
3.  Upload the images to the new folder.

**Step 2: Add Image List to Post Front Matter**

In the YAML front matter (between the `---` lines) of your `.md` post file, add a `gallery_items` list:

```
gallery_items:
  - name: "image-1.jpg"
    alt: "A descriptive alt text for the first image."
    caption: "Optional caption for image one"
  - name: "image-2.jpg"
    alt: "A descriptive alt text for the second image."
    caption: "Optional caption for image two"
```
**Step 3: Place the Gallery in Your Post**

In the body of your post, add the following line where you want the gallery to appear. **Remember to update the `path`!**

```
{% raw %}{% include image-gallery.html images=page.gallery_items path="/img/gallery/my-new-gallery/" %}{% endraw %}
```
