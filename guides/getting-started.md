---
layout: base
title: Getting Starting with GitHub Pages
subtitle: A preliminary guide to sustainable and extensible digital history websites
author: Fred Gibbs
date: 2019-10-03
---

* TOC
{:toc}


## What is GitHub Pages?
- Makes static site pages

## Why GitHub Pages?
- free, accessible, stable, version control, transparency


## Build a website in 10 minutes

### First steps
- Create an account at [GitHub](http://github.com/register)
- Rather than create everything from scratch, start with a basic set of core files. Use jekylton as a template.
- Go to the [jekylton repository](http://github.com/fredgibbs/jekylton).
- Click the green "Use this Template" button
- Name your repository. I'd recommend `jekylton` for now. You can always rename it later or delete it and start over.
- Go into the settings menu (the gear menu on the right of the top nav bar)
- Scroll down to section titled GitHub Pages (the penultimate section)
  - Select / from master branch
  - Note the URL that appears there in the form of http://USERNAME.github.io/jekylton. Replace USERNAME with whatever your GitHub username is, like http://fwgibbs.github.io/jeklyton
  - Go to that URL, and you'll probably get a Page Not Found error.
  - Wait a minute for GitHub to build your site, and refresh the page.

You've made a website!


## Basic Site Components
Let's see what's in the repository

### `_includes` directory
This directory hold files that are typically small bits of code that appear on more than one page, like a nav bar or footer. This way, if you want to change the footer on all your site pages, you can change it in just one spot.

### `_layouts` directory
This directory

### `essays` directory
This directory could be named anything--it's just a place to put separate essays. You might have many of these directories for essays on different topics, like `ads`, `newspapers`, `historic sites`, `campus-buildings`, etc.

### credits.md page
A place to list all your contributors. Or you can delete it and take all the credit.

### directory.md page
This is a special page

### index page
This is the homepage of your site.

---

## Page components

### YAML headers
All essays must have the following metadata at the top of the page, with the values customized to your own page. **Be sure you have the 3 hyphens `---` before and after your metadata on their own lines**. The top of your essay page should look like:

``` markdown
---
title: Mesa Vista Hall
author: Fred Gibbs
date: 2019-09-13
---
```

### Markdown
One of the great features of GitHub Pages is that it allows you to write pages in Markdown rather than HTML. If you are new to Markdown, complete this [Markdown tutorial](https://www.markdowntutorial.com/). If you need syntax help, check out this [cheat sheet](https://www.markdownguide.org/cheat-sheet).

#### Dillinger
If you want to write online and preview your Markdown text as you write, use [Dillinger](https://dillinger.io/). It saves your work as you go. When you are done writing, you can get your post into GitHub in two ways:

One is as described above (Writing on GitHub), but you'll simply copy and paste your text from Dillinger into the edit window on GitHub.


---

## Editing your site

### Edit your homepage
- Go to your repository homepage
- Click on the `index.md` file.
- Click on the edit icon (looks like a pencil)
- Make some change to the text.
- Hit the green Commit button near the bottom of the page
- Wait a few minutes and refresh your webpage.

### Add a new page
- Click the Add file button
- Type in the filename, including a `.md` extension
- Hit the green Commit button near the bottom of the page

---

## Edit the top nav bar
- Click on the `_includes` directory
- Click on `nav.html`
- Click on the edit icon (looks like a pencil)
- Duplicate (via copy and paste) on of the lines that contains a link to a page on your site
- Replace the old link with the name of the page you just created but WITHOUT the `.md` extension
- Hit the green Commit button near the bottom of the page




## Edit the base template
Jekyll uses layouts and includes to reuse common components across your site
You'll notice in the YAML header for the index page, there is a line layout: base
Let's look at the base template, which of course is in the templates directory

This is the template for all your pages. Once you're more comfortable with templates, you can write your own, or find someone else's and modify it.


## Including Images
Images instructions are on [their own page](loading-images).


## Other typographic features
Look in the `_includes` folder and you'll see a number of code snippets. These are all small chunks of code of HTML and the special language that Jekyll uses to help make pages more flexible. These make it easy to embed other things on your pages, like videos and pull quotes. They work the same way as do including images, although the parameters you'll set in the code snippets are naturally a little different.

All the include files that you might want to use are explained on the [code examples page](code).


---

## Testing your site locally (without GitHub pages)
Waiting for your changes to show up on the live, public website can be annoying, to say the least. It works fine for small, infrequent updates, but any kind of testing or experimentation requires you to run your website on your computer. In other words, to run it locally (as opposed to remotely on the GitHub servers).

There are a number of independent software applications that work together. They all do one thing very well, which makes installation a bit more work than just having everything bundled together, but it also makes everything work more effectively in the long run. You don't need to understand how all these work, and once they are installed you don't need to think about them very much.

These instructions outline exactly what to do. It looks like a lot of steps, but they are all simple and go quickly.

### Using the Command Line


#### Mac
These instructions are based on [these]()
- `xcode-select --install`

- `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
A program called Homebrew helps us install some required software very easily.

- `brew install ruby`
GitHub pages uses an application called Jekyll to build websites. Jekyll is written in the Ruby programming language (which you don't need to know anything about), so it is necessary to install the Ruby language for Jekyll to run.

- `gem install jekyll`
Install the Jekyll applciation that turns our Markdown files and templates into a website.

- `gem install bundler`
This application called [Bundler](http://bundler.io) helps keep all the code required to run your website locally in sync with how it runs on GitHub. This prevents issues where your pages might appear a little differently or not at all as the code used at GitHub starts to differ from what you're running on your computer. It might be a long time before you notice any difference, but you will eventually. So it's worth taking a few minutes to avoid a very confusing problem later.

To tie your website to your GitHub website, we'll need the application that helps run GitHub, called git.
Install Git: https://git-scm.com/download/mac.


#### Windows
These instructions are based on [these](https://jekyllrb.com/docs/installation/windows/)
