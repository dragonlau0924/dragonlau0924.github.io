---
title: 用 Obsidian & Anki 实现渐进阅读的探索
date: 2023-04-13T22:12:11+08:00
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
---

如果想用 Anki 实现 SuperMemo 般的渐进阅读……

<!--more-->

---

## SuperMemo & Anki 的优缺点比较
| 软件      | 优点                 | 缺点                               |
| --------- | -------------------- | ---------------------------------- |
| SuperMemo | 算法先进，可渐进阅读 | 单平台，只有 PC 端                 |
| Anki      | 多平台               | 卡片大爆炸，算法落后，不可渐进阅读 |

---

## 最小的渐进阅读系统
+ 交叉
+ 摘录
+ 挖空/问答
+ 优先级排序
+ 间隔重复

---

## 用 Obsidian & Anki 实现渐进阅读的探索
+ 算法落后&卡片堆积的解决方案：
	+ [FSRS 算法](https://github.com/open-spaced-repetition/fsrs4anki)（*叶哥*）：更先进，可**提前**或**推迟**
+ 渐进阅读解决方案探索：
	+ [Spaced Repetition 插件](https://github.com/st3v3nmw/obsidian-spaced-repetition) ：文章的排期（*交叉*）
	+ [Anki](https://apps.ankiweb.net/) & [flashcards 插件](https://github.com/reuseman/flashcards+obsidian/wiki)：摘录、挖空/问答、 间隔重复
	+ Quicker 动作：[迭代改卡](https://getquicker.net/Sharedaction?code=48ac555e-fe67-44b7-8a38-08db25feb013)
	+ 文件夹结构：优先级排序（*相对的*）
