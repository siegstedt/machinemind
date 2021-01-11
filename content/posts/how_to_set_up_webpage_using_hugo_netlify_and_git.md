---
title: "How to set up a webpage using HUGO, Netlify, and Git"
subtitle: "An introduction to static website hosting with open and free resources"
date: 2021-01-03T12:29:51+01:00
lastmod: 2021-01-11T18:21:23+01:00
draft: false
author: "siegstedt"
authorLink: ""
description: "How to set up a webpage using HUGO, Netlify, and Git"

tags: [hugo,git,web dev]
categories: [Projects]

hiddenFromHomePage: false
hiddenFromSearch: false

featuredImage: ""
featuredImagePreview: ""

toc:
  enable: true
math:
  enable: false
lightgallery: false
license: ""
---

This is my **first time** using a static website builder. So far, I have used to built pages with WordPress. But I have never truly made friends with the UI and got a confused too easily with the many additional plugins it required to get up something nice.

So, as a I thought about setting up a new site, I followed the recommendation of a friend to check out Hugo. The promise of a simple to use and shiny new open-source tool got hooked up. And so I'm sitting here and start with **Hugo, Netlify and Git**.

<!--more-->

Help to **improve this post** on [GitHub](https://github.com/siegstedt/machinemind/blob/main/content/posts/how_to_set_up_webpage_using_hugo_netlify_and_git.md). Thank you for your contribution.

## setup a hugo site with a theme

Now, let's get the party started and set up our site. 

To **install Hugo** on your machine, follow the instruction on the following link: https://gohugo.io/getting-started/installing/

Now the playing begins. For getting started, it actually only takes a hand full of commands in your terminal.

Again, Hugo really works most efficiently when used straight from the terminal. Here are the two (!) commands for **creating a new site** and navigating into its directory.

```
hugo new site machinemind
cd machinemind
```

The site for sure still needs a bit more love and style. Let's choose a theme.

Hugo offers a big a variety of themes that you can download, apply on your site and change as you wish. Here is an overview: https://themes.gohugo.io/

For my site, I want to go with the LoveIt. Check out the documentation of the theme of your choice to make sure that you configure it correctly.

For me, **installing the theme** is done with two git commands.

```
git init
git submodule add https://github.com/dillonzq/LoveIt.git themes/LoveIt
```

Again, I want to highlight that the theme of your choice may require some changes to the config file of your site. For the basic setup of my site, I followed the instructions of the LoveIt documentation: https://hugoloveit.com/theme-documentation-basics/

So far, the page is free of any content. Here is the command to **create a new post**.

```
hugo new posts/new-post.md
```

The quickest way to edit the content of the post is for sure to simply open the markdown file in a text editor of your choice and hit some keys.

## launch the page

Alright. There is the site. There is a first post. You must be getting curious and want to inspect the results of your work.

**Launch the website** with the following command. Then, go to http://localhost:1313 in your browser and see.

```
hugo serve --disableFastRender -D
```

The "-D" is required to get the drafted post produced. Alternatively, you can change the "draft" variable inside the post's md file from true to false.

Good! We're really making progress here. As soon as you want to **publish** the site, we only need to hit one word into terminal. 

```
hugo
```
Now, check your directory structure. A public folder will be generated, containing all static content and assets for your website. 

## host and maintain site

I love this. Thus far, we were working with lightning speed to get up a themed site, a post, and publish all the content inside the site's directory.

Okay. I want to have all changes to website tracked by Git. I will use GitHub and continue with **creating en empty repository** on GutHub that I call just the same name as my webpage.

Once that is successful, **push all content** from the local directory on the  created it GitHub repository.

```
git remote add origin https://github.com/siegstedt/machinemind.git
git branch -M main
git push -u origin main
```

Brilliant work. This GitHub repository will be our backbone for deploying the site through Netlify. Clearly, there are other means to host your site. Choose what feels right with you: https://gohugo.io/hosting-and-deployment/

Still, I will **host the site with Netlify** and make use of its GitHub interface for continuous deployment. Find the instructions for the setup here: https://gohugo.io/hosting-and-deployment/hosting-on-netlify

I grant you some time for getting that up. With Netlify, it's described very well in their docs. And I trust you being a smart cookie. It will go smoothly.

Once your site is hosted, you want to continue adding and pushing content on it. For this maintenance work, use the following commands for **updating GitHub repo** with the new content.

```
git add .
git commit -m 'message'
git push
```

## checklist

And that is it really. Enjoy building and playing with your site.

For your reference, find below a little checklist of action steps and related links.

- [ ] Install Hugo: https://gohugo.io/getting-started/installing/
- [ ] Hugo Quick start: https://gohugo.io/getting-started/quick-start/
- [ ] LoveIt theme basics: https://hugoloveit.com/theme-documentation-basics/
- [ ] Host page no Netlify: https://gohugo.io/hosting-and-deployment/hosting-on-netlify/