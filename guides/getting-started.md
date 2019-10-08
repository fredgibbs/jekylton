---
layout: base
title: Getting Starting with GitHub Pages
subtitle: A preliminary guide to sustainable and extensible digital history websites
author: Fred Gibbs
date: 2019-10-03
---

* TOC
{:toc}


<a name="what-is-github"/>
## What is GitHub Pages?
Makes static site pages

## Why GitHub Pages?
free, accessible, stable
version control
transparency
One huge advantage of using GitHub Pages to hose your site is that you can ~steal~ borrow from anyone else using it, too. This is especially when taking code from a project that is set up similarly to yours.


## How do I try it out?


## First steps
Create an account at github.com

Create a repository (repo for short)
Use jekyton as a template

Go into the settings menu, scroll down to GitHub Pages
Select / from master branch

Wait a few minutes, and you will see your site at
github.io/USERNMAE/REPO

You've made a website!


## Let's see what a basic page looks like
### YAML headers
### Markdown



## Editing your site

### Edit your homepage
Click on the index.html file.
Click on the edit icon
Make some change to the text.
Hit the green Commit button
Wait a few minutes and refresh your webpage.

### Add a new page
Click the Add file button
type in the filename, including paths
Click the commit button


### Edit the top nav bar

## Edit the base template
Jekyll uses layouts and includes to reuse common components across your site
You'll notice in the YAML header for the index page, there is a line layout: base
Let's look at the base template, which of course is in the templates directory

This is the template for all your pages. Once you're more comfortable with templates, you can write your own, or find someone else's and modify it.

## Edit the top nav bar
It call a few other include files, including `nav.html`

To change the nav bar, click on `nav.html`


## Including Images

Two fundamental ways of loading images, Markdown and raw HTML.

The problem is that standardizing captions and so on would be very difficult across pages. EXAMPLE

This problem is solved through a layer of abstraction. We use some very general code to write more specific code for us. To be concrete:

The Jekylton template comes with code snippets to help with this.

Load up the sample page. Notice the code to load the image.
[figure code]

This calls `figure.html` from our `_includes` directory. We don't need to understand that code right now, so we'll leave it aside for the moment. We just need to note what parameters you can set, namely the width, position, caption, and source---all ing addition to the original file name.

Documentation for loading images is already part of your website, since it's useful to anyone who is using the web framework.
[adopt loading images for docs?]


## Other snippets
Look in the `_includes` folder and you'll see a number of code snippets that help you embed other things on your pages, like videos and pullquotes and big images that span the screen width (called jumbotrons). They work the same way as do including images, although the parameters you'll set in the code snippets are naturally a little different.



## Testing your site locally (without GitHub pages)
Waiting for your changes to show up on the live, public website can be annoying, to say the least. It works fine for small, infrequent updates, but any kind of testing or experimentation requires you to run your website on your computer. In other words, to run it locally (as opposed to remotely on the GitHub servers).

There are a number of independent software applications that work together. They all do one thing very well, which makes installation a bit more work than just having everything bundled together, but it also makes everything work more effectively in the long run. You don't need to understand how all these work, and once they are installed you don't need to think about them very much.

These instructions outline exactly what to do. It looks like a lot of steps, but they are all simple and go quickly.

### Command Line (a separate tutorial)


### Ruby
GitHub pages uses an application called Jekyll to run, which is written in and therefore requires the Ruby programming language.
install ruby (use rvm?)

### Git
To tie your website to your GitHub website, we'll need the application that helps run GitHub, called git.
Install Git: https://git-scm.com/download/mac.

### Bundler
This helps keep all the code required to run your website locally in sync with how it runs on GitHub. This prevents issues where your pages might appear a little differently or not at all as the code used at GitHub starts to differ from what you're running on your computer. It might be a long time before you notice any difference, but you will eventually. So it's worth taking a few minutes to avoid a very confusing problem later.

https://bundler.io -> Getting started
