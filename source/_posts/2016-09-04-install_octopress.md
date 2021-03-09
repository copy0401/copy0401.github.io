---
layout: post
title: "Install Octopress"
date: 2016-09-04 01:56:05 +0800
comments: true
categories: octopress
---

```
cd ~/
git clone git://github.com/imathis/octopress.git octopress
cd octopress
gem install bundler
bundle install
rake install
rake preview
```

http://localhost:4000/

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
rake preview
rake deploy
```

---

新的頁面

```
rake new_page["title"] # for zsh, use: rake new_page\["title"\]
```

or

```
rake new_page[about/index.html] # for zsh, use: rake new_page\[about/index.html\]
```


再去 `source/_includes/custom/navigation.html` 新增連結

```
<ul class="main-navigation">
  <li><a href="{{ root_url }}/">Blog</a></li>
  <li><a href="{{ root_url }}/blog/categories/octopress/">Octopress</a></li>
  <li><a href="{{ root_url }}/blog/archives">Archives</a></li>
  <li><a href="{{ root_url }}/about">About</a></li>
</ul>
```

---

撰寫文章

```
rake new_post["title"]
```

產生新的檔案 `YYYY-MM-DD-title.markdown` 到 `source/_posts/`

如果 `.markdown` 要改成 `.md` 可以到修改 `Rakefile`

```
new_post_ext    = "md"
new_page_ext    = "md"
```

---


Push to Github

```
git add .
git commit -m "some commit"
git push origin source
```