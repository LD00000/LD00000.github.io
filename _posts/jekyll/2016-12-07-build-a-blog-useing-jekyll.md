---
layout: article
title:  "搭建一个基于 github 和 jekyll 的免费博客"
date:   2016-12-07
categories: jekyll
---

# 申请 github-pages
---
> 源地址 https://pages.github.com/

1. 创建一个仓库
在 github 建立一个新仓库，命名为 `username.github.io`，用自己的用户名替换 `username`。**note: 如果用户名不匹配，将会不起作用。**

2. clone 项目 `git clone https://github.com/username/username.github.io`

3. 创建 hello world。`cd username.github.io && echo "Hello World" > index.html`

4. push 项目。`git add --all && git commit -m "Initial commit" && git push -u origin master`

5. 访问 `http://username.github.io`，就能看到刚刚创建的网站了。

# 搭建 jekyll 环境
---

输入 `ruby --version` 验证是否安装了 `ruby`（Mac 已经预装了）
![](../../images/jekyll/2016-12-08-00.30.35.png)

安装 jekyll，输入 `gem install jekyll`

删除之前的 `index.html`，运行 `jekyll new .`，jekyll 就会自动生成一些博客的基础文件和目录。输入 `jekyll serve`，就可以访问了。默认地址 `http://127.0.0.1:4000/`。

还可以在 `_config.yml` 中进行一些个性化配置。
