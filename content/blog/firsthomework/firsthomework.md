---
title: 3 | Homework
permalink: "/blog/homework/"
description: What to work on.
date: 2026-09-17
day: Day 1
tags: ["day 1", "homework"]
heroImage: "./assets/catkeyboard.jpg"
draft : false
---

<style>
    /* style block example */
    .exampleClass {
        color: purple
    }
    #exampleID {
        color: green;
    }
</style>

<img src="/assets/catkeyboard.jpg" alt="A cat asleep on a keyboard."/>

Before you get to your homework it's good to know the term...

## Computational Thinking

Knowing how to break down your ideas/challenges/bugs into essential steps is key to bringing them to life computationally. We need to think like a computer.

1. **Decomposition**
    * Breakdown your goals/challenges into smaller parts. Simplify the challenge to make it more manageable.
        + "My custom font isn't working. This one is pretty simple but I need to think about how 11ty uses custom fonts. It will involve the location of my font in my /font folder, CSS file, and elevent.config.js file."
2. **Pattern recognition**
    * Have you experienced something similar before?
    * How does each smaller part of the challenge connect to other parts of the whole?
        + "I know I have to define it in my CSS, and I might have to update my 11ty config file. I can check what fonts are in my /font folder."
3. **Abstraction**
    * Extract the most relevant information form each decomposed challenge to simplify the process further.
        + "The computer needs to know where to find the font file (form my /fonts folder) in my css file, then what elements should use it in my css file, and finally it needs to be told to carry the file (from its location) through to the site build in my config."
4. **Algorithms**
    * Define a step-by-step solution to the challenge. What steps do you need to communicate to the computer?
        1. Call to the font location (@font-face) in my CSS. 
        2. Use the font on an element (font-family) in my CSS. 
        3. Pass the font file through to my site build (.addPassthroughCopy("./fonts/font.woff2")).

## Your Homework

1. **Surf the web.** Note your favourite websites. Inspect the code (right click, inspect) to see how they've coded the elements you like. Copy and paste elements you like into notes.
2. **Ideas come first.** Think about what elements you might want to add to your website. Keep it simple for now. What do you want to see on your blog? Write a list of up to 5 things.
    * 11ty can do a lot. Keep to HTML/CSS for now (if you want to use JavaScript on a post/page, make your file .html instead of .md — [Try this?](https://www.w3schools.com/howto/howto_js_slideshow.asp)). If you're up for the challenge, give things like *Shortcodes* a go. I can't promise to be able to help you with deep 11ty dives. But we can try!
    * It can be overwhelming to learn how to code. Just start with what you need to know for the project at hand. We're having fun here.
3. **Work through your wish list!** Use the resources provided to edit your website as you wish.
    * Keep your index.css organzied. Using <code>/* comments */</code> can help. Since 11ty needs a bunch of instructions for passing files to the main build, I'd suggest leaving as much as you can just in <code>/css/index.css</code>, or even in your template is fine for now. You can use css <span style="color:blue;">inline</span> or in a <span class="exampleClass">style</span> <span id="exampleID">block</span> on your templates.
    * Edit layouts in the <code>/_includes</code> folder.
    * Edit pages in <code>/content</code> folder.
    * Add all images/videos for posts and pages in the <code>/content/assets</code> folder.
    * Edit posts in <code>/content/blog</code> folder. **Number your posts:**
        + ✅ <code>/blog/1_mypost.md</code> or <code>/blog/1_mypost/1_mypost.md</code> (keeps files in order)
        + ❌ NOT <code>/blog/mypost.md</code> or <code>/blog/mypost/mypost.md</code>
        + Add custom permalinks at the top of your /blog/post files under <code>title:</code> line. 
		<br>Like <code>permalink: "/blog/post-name/"</code>

---

## Helpful Documents for Coding

- [W3 Schools](https://www.w3schools.com/) | Learn HTML, CSS, Javascript, great for image slideshows, etc.
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/) | Write your blogs in Markdown for formatting.
- [Nunjucks](https://www.11ty.dev/docs/languages/nunjucks/) | Used for 11ty functions. Usually you can find what you need in docs to copy & paste.
- [11ty Docs](https://www.11ty.dev/docs/) ([this one on assets is helpful](https://www.11ty.dev/docs/assets/))
- [Netlify Docs](https://docs.netlify.com/)
- [Github Desktop Docs](https://docs.github.com/en/desktop)
- [VS Code Docs](https://code.visualstudio.com/docs)
- [Codecademy](https://www.codecademy.com/) | Free coding modules

