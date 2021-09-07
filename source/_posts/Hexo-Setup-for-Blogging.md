---
title: Hexo Setup for Blogging
date: 2021-09-06 22:40:23
tags:
mathjax: true
---

## Setup Hexo for Static Blog
Just follow the awesome [Deploy Doc](https://hexo.io/docs/github-pages.html). There are a few things..
* Node version needs to be bumped to v12 (LTS),
* Make sure the dev/deploy branch names are correct.

## Setup Theme
The theme setup was mostly for MathJax to jot down equations. Next theme has a good support for this.

```
git submodule add https://github.com/theme-next/hexo-theme-next.git next
```

And then set `next` in `_config.yml`.

# Setup MathJax
Change the rendering engine
```
npm uninstall hexo-renderer-marked --save 
npm install hexo-renderer-pandoc --save
```

Change the config in `next/_config.yml` (note, math settings are not set in `root/_config.yml` for next theme) and profit! Of course, the first equation should be the Kelly bet 

$$ f^{*}={\frac{bp-q}{b}}={\frac{p(b+1)-1}{b}} $$
