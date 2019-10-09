---
layout: base
title: Getting Starting with GitHub Pages
subtitle: A preliminary guide to sustainable and extensible project websites
author: Fred Gibbs
date: 2019-10-03
---

# {{page.title}}

## {{page.subtitle}}

<!--
### Table of Contents
* TOC
{:toc}
-->

## What is GitHub Pages?
- GitHub Pages is basically a free service that takes a set of files and makes them into a website. It does this with an application called Jekyll. Etc.

## Why GitHub Pages?
- free, accessible, stable, version control, transparency

## How to use this guide
These instructions explain how a GitHub Pages site works. It describes files and folders in your repository as well as how individual files work. It will be useful to have these instructions open in a separate browser window as you view and edit files on your website.

## Build a website in 10 minutes
- Create an account at [GitHub](http://github.com/register)
- Rather than create everything from scratch, start with a basic set of core files. Use Jekylton (this site) as a template. Go to the [jekylton repository](http://github.com/fredgibbs/jekylton)
- Click the green "Use this Template" button
- Name your repository. I'd recommend `jekylton` for now. You can always rename it later or delete it and start over
- Go into the settings menu (the gear menu on the right of the top nav bar)
- Scroll down to section titled "GitHub Pages" (the penultimate section)
- Select / from master branch
- Note the URL that appears there in the form of http://USERNAME.github.io/jekylton. Replace USERNAME with  your GitHub username, like http://fwgibbs.github.io/jeklyton
- Click on that URL, and you'll likely get a Page Not Found error.
- Wait a minute for GitHub to build your site, and refresh the page (Ctrl or Cmd R).

You've made a website!

---

## Anatomy of a Page
To understand the basics of how pages work, let's investigate the `index.md` file.

### YAML headers
The top of the page looks like:

``` markdown
---
title: Getting Started
layout: base
date: 2019-10-03
---
```

All pages must have a similar metadata block at the very top, with the title customized for each page. This is called a YAML header. For now, it is enough to know that this block of metadata tells GitHub Pages that it should be part of your website. **Be sure you have the 3 hyphens `---` before and after your metadata on their own lines**.

The index page uses the `base` layout, as do all pages except the directory page; layouts will be discussed in the next section.

You'll notice that you have a few pages in the root directory of your repository, like `credits` and `directory`. They work the same way.

### Markdown
One of the great features of GitHub Pages is that it allows you to write pages in Markdown rather than HTML.

<<comparison>>

If you are new to Markdown, complete this [Markdown tutorial](https://www.markdowntutorial.com/). If you need syntax help, check out this [cheat sheet](https://www.markdownguide.org/cheat-sheet).

#### Previewing Markdown
If you want to write online and preview your Markdown text as you write, use [Dillinger](https://dillinger.io/). It saves your work as you go. When you are done writing, you can simply copy and paste your text from Dillinger into the edit window on GitHub.

---

## Basic Site Components
Now that we've looked at a page, let's see what else is in the repository. Go to your own Jeklyton repository at http://USERNAME.github.io/jekylton (again, replacing USERNAME with your GitHub username). All of the files are important in their own way, but we're going to focus on the folders and files that most directly create our website.

### `_includes` directory
This directory hold files that are typically small bits of code that appear on more than one page, like a nav bar or footer. This way, if you want to change the footer on all your site pages, you can change it in just one spot.

### `_layouts` directory
This directory provides the basic layouts for different kinds of pages. We want all our pages to have well-formed HTML, which means they need to start with `<!DOCTYPE html>`. So you see that's the first line of code on the

These pages will include bits of code from the `_includes` directory to assemble a complete webpage.  


### `essays` directory
This directory could be named anything--it's just a place to put separate essays. You might have many of these directories for essays on different topics, like `ads`, `newspapers`, `historic sites`, `campus buildings`, etc.

###


---




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
```xcode-select --install```

```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```
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
