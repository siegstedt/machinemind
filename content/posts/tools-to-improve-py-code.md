---
title: "Tools to improve Python code"
subtitle: "Sort of the things that you can always run when issuing a new piece of code"
date: 2021-02-25T18:39:51+01:00
lastmod: 2021-02-25T18:39:51+01:00
draft: true
author: "siegstedt"
authorLink: ""
description: ""

tags: [programming, Python]
categories: []

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

Maintenance is important. Because crafting code takes time. Therefore, your invested time should turn into a reliable product. There are some tools that can help you maintain your code base programmatically.

<!--more-->

Help to **improve this post** on [GitHub](https://github.com/siegstedt/machinemind/blob/main/content/posts/tools-to-improve-py-code.md). Thank you for your contribution.

**PEP 8 Style**

Keep your code to the agreed style guide PEP 8. Exemplary tools can be [pycodestyle](https://pypi.org/project/pycodestyle/), [black](https://pypi.org/project/black/) or [flake8](https://flake8.pycqa.org/en/latest/).

**Code Climate**

[Code Climate](https://codeclimate.com/) indicates how well you've defined your function's and variable's names. Analyze your code for improvements in readability.

**Sphinx**

[Sphinx](https://pypi.org/project/Sphinx/) let's you easily generate beautiful documentation - for instance as a HTML output ready to be hosted on pypi.

**Codecov**

[Codecov](https://about.codecov.io/) shows you what parts of your code are covered with tests - and which parts are not. So, it allows you to discover where to improve your project's tests.

**GitHub / GitLab**

Host your projects with git and allow your fellow coders to review, post an issue and request changes.

**Travis CI**

With [Travis CI](https://travis-ci.org/) you can continuously test your code. It can be integrated with other tools as well, e.g. GitHub.