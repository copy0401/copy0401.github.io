---
layout: post
title: "Set Octopress Theme"
date: 2016-09-05 01:56:05 +0800
comments: true
categories: octopress
---

```
cd ~/octopress
git clone git://github.com/lucaslew/whitespace.git .themes/whitespace
rake install['whitespace'] # for zsh, use: rake install\['whitespace'\]
rake generate
rake preview
```

```
rake setup_github_pages
```

git@github.com:[your_username]/[your_username].github.io.git

例如輸入 

```
git@github.com:copy0401/copy0401.github.io
```

```
rake generate
rake deploy
```


