---
title: typora主题修改
date: 2024-11-04T17:59:00
tags:
  - 教程
feature: 
published: true
---
typora的主题字体颜色不太醒目，于是我把里面的`github主题`做了一些修改，最终效果如下：

<!--more-->

![image.png](https://s1.vika.cn/space/2024/11/04/631e7f0c2d6b4957a07c20055ca81edf)

```css
body {
    font-family: "LXGW WenKai","PingFangSC-Regular","Helvetica Neue",Helvetica,Arial,sans-serif;
    color: rgb(51, 51, 51);
    line-height: 1.6;
}
/* 只用替换body中的字体 其他不用动 */
h1 {
    font-size: 1.402em;
    line-height: 1.2;
    border-bottom: 1px solid #eee;
    color: #bf616a;
}
h2 {
    font-size: 1.302em;
    line-height: 1.225;
    border-bottom: 1px solid #eee;
    color: #ebcb8b;
}
h3 {
    font-size: 1.224em;
    color: #a3be8c;
}
h4 {
    font-size: 1.106em;
    color: #b48ead;
}
h5 {
    font-size: 1.025em;
    color: #8fbcbb;
}
h6 {
   font-size: 1em;
   color: #81a1c1;
}

code {
    color: #8fbcbb;
    font-size: 0.9em;
}
mark {
    background: #8fbcbb;
}

strong {
    color: #bf616a;
}

em {
    color: #a3be8c;
}

```
typora用来批量上传一些本地图片还是很好使的，简洁的UI页面偶尔用来写作也不错，配合Ob也可以用来快速打开单个文件。强推！！！
