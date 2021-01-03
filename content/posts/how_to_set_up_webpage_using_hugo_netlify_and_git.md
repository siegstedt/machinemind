---
title: "How_to_set_up_webpage_using_hugo_netlify_and_git"
date: 2021-01-03T12:29:51+01:00
draft: false
---

**I am setting up my first webpage with Hugo and Netlify**

This is my first time using a static website builder. So far I have used to built pages with WordPress. I followed the recommendation of a friend and the promise of a simple to use and shiny new open-source tool to set up this site.

For getting you started, it actually only takes a hand full of commands in your terminal. Easy!

Links for getting started:
- Hugo Quick start: https://gohugo.io/getting-started/quick-start/
- LoveIt theme basics: https://hugoloveit.com/theme-documentation-basics/
- Host page no Netlify: https://gohugo.io/hosting-and-deployment/hosting-on-netlify/

**Create site and install theme**

```
hugo new site machinemind
cd machinemind
```

**Install LoveIt theme**

```
git init
git submodule add https://github.com/dillonzq/LoveIt.git themes/LoveIt
```

Set up the config.toml file as recommdeted and do changes later on.

**Create a new post**

```
hugo new posts/new-post.md
```

**Launch website**

```
hugo serve --disableFastRender
```
Go to http://localhost:1313

```
hugo
```
A public folder will be generated, containing all static content and assets for your website.

**Push created repository on GitHub**

```
git remote add origin git@github.com:siegstedt/machinemind.git
git branch -M main
git push -u origin main
```
