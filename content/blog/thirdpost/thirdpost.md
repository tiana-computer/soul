---
title: 4 | Personalize Your Blog
permalink: "/blog/personalize/"
description: Add your own flare.
date: 2026-09-22
day: Day 2
tags: ["day 2", "personalize"]
heroImage: "./assets/Cat_using_computer.jpg"
draft : false
---

<img src="/assets/Cat_using_computer.jpg" alt="A sitting on a desk with a laptop and monitor."/>


What makes your blog your own?

What's on your blog wish list? Experiment with adding features and content to your website.

Some ideas if you're stuck...
- [Image hover effects](https://www.w3schools.com/howto/howto_css_image_overlay.asp)
- [Image gallery](https://www.w3schools.com/css/css_image_gallery.asp)
- [Custom domain](https://docs.netlify.com/manage/domains/get-started-with-domains/)
- [Custom cursor](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/cursor)
- Animations (with CSS or GIFs)
    * [GifCities](https://gifcities.org/)
    * [Glitter Graphics](https://www.glitter-graphics.com/)
    * [My Smilies](http://mysmilies.com/)
    * [3D GIF Maker](https://www.3dgifmaker.com/)
- Other fun things
    * [Frutiger Aero Archive](https://frutigeraeroarchive.org/)
    * [Chatango](https://www.chatango.com/)
- Want more than 1 collection of posts? [See 11ty docs.](https://www.11ty.dev/docs/collections/)
- Add JavaScript, CSS, Fonts, Favicon / Background Images... [See 11ty docs.](https://www.11ty.dev/docs/assets/)
    * You need to tell 11ty to "pass through" global files like these.
    * [Try Are.na](https://www.are.na/search?q=%7B%22term%22:%7B%22facet%22:%22free%20fonts%22%7D%7D) for finding free fonts. I love [Velvetyne Type Foundry](https://velvetyne.fr/).

Recall key user tips from the <a href="https://bloggingforthesoul.netlify.app/blog/homework/">Homework page</a>.
- Keep your index.css organzied. Using <code>/* comments */</code> can help. Since 11ty needs a bunch of instructions for passing files to the main build, I'd suggest leaving as much as you can just in <code>/css/index.css</code>, or even in your template is fine for now. You can use css <span style="color:blue;">inline</span> or in a <span class="exampleClass">style</span> <span id="exampleID">block</span> on your templates.
- Edit layouts in the <code>/_includes</code> folder.
- Edit pages in <code>/content</code> folder.
- Add all images/videos for posts and pages in the <code>/content/assets</code> folder.
- Edit posts in <code>/content/blog</code> folder. **Number your posts:**
    * ✅ <code>/blog/1_mypost.md</code> or <code>/blog/1_mypost/1_mypost.md</code> (keeps files in order, can be hard to change later)
    * ❌ NOT <code>/blog/mypost.md</code> or <code>/blog/mypost/mypost.md</code>
    * Add custom permalinks at the top of your /blog/post files under <code>title:</code> line. 
		<br>Like <code>permalink: "/blog/post-name/"</code>

We'll do a show & tell at the end of class. Share your site with your friends. 

Email Tiana with your site url & add this icon to your site to join our class webring!


[![Alt Text](/assets/webring-blogging4soul.png)](https://bloggingforthesoul.netlify.app/)


---

## Class notes...

### Class Wishlist | Sept, 2026
- [Staggering CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Selectors/:nth-child)
    * <code>li:nth-child(odd) { margin-left: 10px; } <br> li:nth-child(even) { margin-left: 0px; }</code>

- [Easy Custom Forms](https://web3forms.com/)
    * Copy their [example](https://docs.web3forms.com/getting-started/examples/basic-html-contact-form).
- [Vote/Like Embed](https://likebtn.com/en/)
- [Object-fit](https://www.w3schools.com/css/css3_object-fit.asp) an image to a div.
- [Compress your images so they load quickly.](https://tinypng.com/) 
    * Make sure crop is true to how you want it to appear on your site.
- [Background Image](https://www.w3schools.com/cssref/pr_background-image.php) / <code>&lt;main&gt;</code> [Background Colour](https://www.w3schools.com/cssref/pr_background-color.php)
    * For an all over background image, add one to the body (for one on each page, do this on the page with a <code>&lt;style&gt;</code> element).
    * For the content container (<code>&lt;main&gt;</code> element in your html & css), give it a background colour.

---

## Our Class Webring
- [scaraby](https://scaraby.netlify.app/)
- more soon.

[![blogging for the soul webring](/assets/webring-blogging4soul.png)](https://bloggingforthesoul.netlify.app/)

