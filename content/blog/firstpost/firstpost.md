---
title: Setting Up Your Blog
description: How to make a blog with 11ty & Netlify.
date: 2026-09-15
day: Day 1
tags: ["day 1", "setting up"]
heroImage: "./assets/Dreysaczens_Antivir.jpg"
draft : false
---

<img src="/assets/Dreysaczens_Antivir.jpg" alt="A cat sitting in bed with a laptop, ready to start a blog."/>


Let's set up this blog!
We're using 11ty and Netlify to build a static site that allows us to play with templates, which is nice when developing a blog.
I like it because it feels like the next step up from just a simple HTML/CSS site.


- Edit <code>_data/metadata.js</code> with your blog’s information.
- (Optional) Edit <code>eleventy.config.js</code> with your <a href="https://www.11ty.dev/docs/config/">configuration preferences</a>.


## Getting Started

We're using a starter repository showing how to build a blog with the [Eleventy](https://www.11ty.dev/) site generator (using the [v3.0 release](https://github.com/11ty/eleventy/releases/tag/v3.0.0)).

[11ty's Guide](https://www.11ty.dev/docs/getting-started/) | [More resources](http://localhost:8080/blog/firstpost/#helpful-documents-for-coding)

Prerequisits: 
- [GitHub Account](https://github.com/) & [GitHub Desktop](https://desktop.github.com/download/)
- [Netlify Account](https://www.netlify.com/)
- [Visual Studio Code](https://code.visualstudio.com/) on your computer.

### 1 | Make Your Repository

- Fork Tiana or [Zachleat's](https://github.com/11ty/eleventy-base-blog) 11ty base blog repository.
- [Detach your fork from fork network](https://youtu.be/ItSfG4y2u5Y?si=hcjUU3sTwajrTR-a) in your repo's *Settings* under *Danger Zone*. Choose *"Leave fork network"* and follow confirmation steps.
- Also in *Danger Zone*, make your repository private if you prefer (nice for keeping post drafts private).
- Clone & open your forked repo through GitHub Desktop in Visual Studio Code.
	* It can be ideal to store your GitHub sites in a path like <code>/Documents/GitHub/ProjectName</code>

<details><summary>Or with code</summary>
<pre>
```
mkdir my-blog-name
cd my-blog-name
```
</pre>
Then clone the repository:
<pre>
```
git clone [insert base blog repo link]
```
</pre>
</details>

### 2 | Install Node.js

Do you have Node.js or npm?
<pre>
<code>node -v
npm -v</code>
</pre>

If not, download [Node.js](https://nodejs.org/en/download/) ([a helpful video](https://youtu.be/7pbQ4ZKPBiU?si=-H8bFiHdF1oSTnbE))
- Download includes npm. Go with the LTS version.
- Wondering which version to download? Info for [Mac](https://docs.cse.lehigh.edu/determine-mac-architecture/) and [PC](https://knowledgebase.vcu.edu/portal/app/portlets/results/viewsolution.jsp?solutionid=250925083200690).

Run the -v commands above to check that it installed.


### 2 | Install Dependencies

Open a terminal in Visual Studio Code with your project open.

```
npm install
```

### 3 | Run Eleventy


Generate a production-ready build to the `_site` folder:

```
npx @11ty/eleventy
```

Or build and host on a local development server:

```
npx @11ty/eleventy --serve
```
The above should throw a <code>http://localhost:8080/</code> link (run <code>npx @11ty/eleventy --serve</code> whenever you want to view your site locally).

Or you can run [debug mode](https://www.11ty.dev/docs/debugging/) to see all the internals.

### 4 | Commit Changes

- Edit locally with Visual Studio Code.
	* There should be a button in GitHub Desktop that opens the project in VS Code.
- Updates appear in GitHub Desktop. Check that all the highlighted changes look correct. 
- Check that your local development server (<code>http://localhost:8080/</code>) is working across all (edited) pages. Check your VS Code terminal for errors. We don't want to commit errors.
- Make some changes:
	* Delete all but one sample post in <code>content/blog</code>. Keep one, delete its content under the second <code>---</code>, just add *"Coming soon."* for now.
	* Update your About (<code>content/about.md</code>) page.
	* Edit <code>_data/metadata.js</code> with your blog’s information.
- Commit from GitHub Desktop (write a short summary, then click *"Commit X files to main"* button), then click the *"Push origin"* button.

Your repo on GitHub will now be populated!

Note: Do not edit files in <code>_site</code> folder.

### 5 | Deploying to [Netlify](https://www.netlify.com/)

- Login and select *"Add new project"*.
- Choose import from GitHub, give required permissions.
- Select your blog repository.
- Add *Project Name* (creates your URL).
	* In <code>eleventy.config.js</code>, find <code>metadata:</code> in the <code>feedPlugin</code> section. Update <code>base:</code> value with your base site URL (<code>https://example.netlify.app/</code>), so your RSS feed works.
- Leave build settings as is. 
- Click *deploy* button at the bottom of the page!
- Set website to public or private.
- Update your site with GitHub Desktop, commit and push your updates as they come.
	* Always review your updates and check for errors before committing/pushing.

Read more about [Deploying an Eleventy project](https://www.11ty.dev/docs/deployment/) to the web.

---

## Helpful Documents for Coding

- [W3 Schools](https://www.w3schools.com/) | Learn HTML, CSS, Javascript, great for image slideshows, etc.
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/) | Write your blogs in Markdown for formatting.
- [Nunjucks](https://www.11ty.dev/docs/languages/nunjucks/) | Used for 11ty functions. Usually you can find what you need in docs to copy & paste.
- [11ty Docs](https://www.11ty.dev/docs/)
- [Netlify Docs](https://docs.netlify.com/)
- [Github Desktop Docs](https://docs.github.com/en/desktop)
- [VS Code Docs](https://code.visualstudio.com/docs)
- [Codecademy](https://www.codecademy.com/) | Free coding modules


---

## Notes From the Base Blog

### Features

- Using [Eleventy v3](https://github.com/11ty/eleventy/releases/tag/v3.0.0) with zero-JavaScript output.
	- Content is exclusively pre-rendered (this is a static site).
	- Can easily [deploy to a subfolder without changing any content](https://www.11ty.dev/docs/plugins/html-base/)
	- All URLs are decoupled from the content’s location on the file system.
	- Configure templates via the [Eleventy Data Cascade](https://www.11ty.dev/docs/data-cascade/)
- **Performance focused**: four-hundos Lighthouse score out of the box!
	- _0 Cumulative Layout Shift_
	- _0ms Total Blocking Time_
- Local development live reload provided by [Eleventy Dev Server](https://www.11ty.dev/docs/dev-server/).
- Content-driven [navigation menu](https://www.11ty.dev/docs/plugins/navigation/)
- Fully automated [Image optimization](https://www.11ty.dev/docs/plugins/image/)
	- Zero-JavaScript output.
	- Support for modern image formats automatically (e.g. AVIF and WebP)
	- Processes images on-request during `--serve` for speedy local builds.
	- Prefers `<img>` markup if possible (single image format) but switches automatically to `<picture>` for multiple image formats.
	- Automated `<picture>` syntax markup with `srcset` and optional `sizes`
	- Includes `width`/`height` attributes to avoid [content layout shift](https://web.dev/cls/).
	- Includes `loading="lazy"` for native lazy loading without JavaScript.
	- Includes [`decoding="async"`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/decoding)
	- Images can be co-located with blog post files.
- Per page CSS bundles [via `eleventy-plugin-bundle`](https://github.com/11ty/eleventy-plugin-bundle).
- Built-in [syntax highlighter](https://www.11ty.dev/docs/plugins/syntaxhighlight/) (zero-JavaScript output).
- Draft content: use `draft: true` to mark any template as a draft. Drafts are **only** included during `--serve`/`--watch` and are excluded from full builds. This is driven by the `addPreprocessor` configuration API in `eleventy.config.js`. Schema validator will show an error if non-boolean value is set in data cascade.
- Blog Posts
	- Automated next/previous links
	- Accessible deep links to headings
- Generated Pages
	- Home, Archive, and About pages.
	- [Atom feed included (with easy one-line swap to use RSS or JSON)](https://www.11ty.dev/docs/plugins/rss/)
	- `sitemap.xml`
	- Zero-maintenance tag pages ([View on the Demo](https://eleventy-base-blog.netlify.app/tags/))
	- Content not found (404) page

### Implementation Notes

- `content/about/index.md` is an example of a content page.
- `content/blog/` has the blog posts but really they can live in any directory. They need only the `posts` tag to be included in the blog posts [collection](https://www.11ty.dev/docs/collections/).
- Use the `eleventyNavigation` key (via the [Eleventy Navigation plugin](https://www.11ty.dev/docs/plugins/navigation/)) in your front matter to add a template to the top level site navigation. This is in use on `content/index.njk` and `content/about/index.md`.
- Content can be in _any template format_ (blog posts needn’t exclusively be markdown, for example). Configure your project’s supported templates in `eleventy.config.js` -> `templateFormats`.
- The `public` folder in your input directory will be copied to the output folder (via `addPassthroughCopy` in the `eleventy.config.js` file). This means `./public/css/*` will live at `./_site/css/*` after your build completes.
- This project uses three [Eleventy Layouts](https://www.11ty.dev/docs/layouts/):
	- `_includes/layouts/base.njk`: the top level HTML structure
	- `_includes/layouts/home.njk`: the home page template (wrapped into `base.njk`)
	- `_includes/layouts/post.njk`: the blog post template (wrapped into `base.njk`)
- `_includes/postslist.njk` is a Nunjucks include and is a reusable component used to display a list of all the posts. `content/index.njk` has an example of how to use it.

[Thank you to the original base!](https://github.com/11ty/eleventy-base-blog) 
