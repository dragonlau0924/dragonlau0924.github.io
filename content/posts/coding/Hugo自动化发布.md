---
publish: true
aliases: 
title: "Hugo自动化发布"
date: 2023-05-03T14:35:33+08:00
tags: [折腾]
feature: 
published: true
hideInList: false
isTop: false
margin: 0
width: 1920
height: 1200
transition: slide
center: true
bg: '#2e3440'
created: 2023-05-03 14:35:33
updated: 2023-05-03 16:11:33
---

把博客发布系统植入 Ob，打造输入 & 输出的流水线。

<!--more-->

Ob 的发布分享一直都是一个蛋疼问题，官方的发布太贵，插件



## git
- [git 下载](https://git-scm.com/)
- git 仓库创建
---

### git 基础命令
- ssh key 获取

`ssh-keygen` + 三次**回车**
- 公钥查看

`cat ~/.ssh/id_rsa.pub`
- 公钥添加

![image.png](https://s1.vika.cn/space/2023/05/02/e8e568e5f63440c5a1f428ebd78c2371)

- git 上传
	- `git config --global user.email "<你的邮箱>"`
	- `git config --global user.name "<你的用户名>"`
	- `git init`
	- `git add .`
	- `git commit -m "first push"`
	- `git remote add origin <你复制的HTTPS>`
	- `git push -u origin master`
	- `git push`

![image.png](https://s1.vika.cn/space/2023/05/02/1ed1d5cbb34344f4838c03ee5935d31d)

- token 获取

![image.png](https://s1.vika.cn/space/2023/05/02/965656c721f34261a9926286f7c2f4a2)

- github actions

```
# Sample workflow for building and deploying a Hugo site to GitHub Pages
name: Deploy Hugo site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["master"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

# Default to bash
defaults:
  run:
    shell: bash

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.108.0
    steps:
      - name: Install Hugo CLI
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb
      - name: Install Dart Sass Embedded
        run: sudo snap install dart-sass-embedded
      - name: Checkout
        uses: actions/checkout@v3
        with:
          submodules: recursive
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v3
      - name: Install Node.js dependencies
        run: "[[ -f package-lock.json || -f npm-shrinkwrap.json ]] && npm ci || true"
      - name: Build with Hugo
        env:
          # For maximum backward compatibility with Hugo modules
          HUGO_ENVIRONMENT: production
          HUGO_ENV: production
        run: |
          hugo \
            --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v1
        with:
          path: ./public

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v2
```

---

## hugo
- 框架了解
	- archetypes
	- content
	- data
	- static
	- themes
	- config.toml

---

## obsidian
- Image auto upload Plugin
	- 丝滑的复制、粘贴体验
- 图床
- templeter
	- 文章撰写、yaml 区字段生成
- obsidian git
	- 自动提交
---

## quicker
- [智能备份](https://getquicker.net/Sharedaction?code=8dfe1e68-33f0-4329-14ae-08da4a84097c)
