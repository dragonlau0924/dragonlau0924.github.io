---
title: Hugo in Obsidian
date: 2023-04-12T21:06:56+08:00
tags:
  - 短文
feature: 
published: true
hideInList: false
isTop: false
---

尝试用 quicker 的**智能备份**推送 Hugo 文件到 github 并且利用 github action 自动构建 github page，效果还不错。


究其原因是 Hugo 的文件夹体系不太适合知识管理， obsidian git 我用来备份我的知识库了，直接用来 push Hugo 文件的话我的文件夹体系就破坏了，所以选择了将 Hugo 文件放到了 Calendar 文件夹里面，利用 quicker 的智能备份动作推送 Hugo 文件到 github ，速度也挺快的。

要是 obsidian git 插件可以同时提交两个 git 仓库就好了，那将绝杀，直接形成输入和输出的 pipline，实现**真 all in one**！

![图片](https://s1.vika.cn/space/2023/04/12/ed4dd1b558434b3f85f943c74e9bac4e)