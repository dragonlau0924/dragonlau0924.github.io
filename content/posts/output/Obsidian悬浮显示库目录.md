---
title: Obsidian悬浮显示库目录
date: 2024-06-09T19:47:14+08:00
tags:
  - 教程
feature: 
published: true
---

Obsidian更新后左下角太碍眼，在我使用的时候还会分散我的注意力，且占据了不少空间，作为一个强迫症患者，绝不允许这种事情发生。

<!--more-->

1. 首先我们需要找到库目录的 css 选择器：
	- 在任意obsidian界面按住 `ctrl+shift+i` ，进入检查模式，之后点击左上角箭头选择我们想要修改的部分，以便我们找到对应的选择器。

![image.png](https://s1.vika.cn/space/2024/06/09/7afa65ddcff04b709c5cad958387aac4)

2. 点击左下角的部分，以检查其选择器。

![image.png](https://s1.vika.cn/space/2024/06/09/8c0c492b0d584a3aae4fce7137245188)

3. 我们在右侧检查发现它的选择器是 `body:not(.is-mobile) .workspace-split.mod-left-split .workspace-sidedock-vault-profile`

![image.png](https://s1.vika.cn/space/2024/06/09/3bdedffd4cb7497d905150582fc8d79f)

4. 在我们未移入目标范围内时让它的不透明为0，当我们移入目标范围内时将其透明改为1，然后再添加缓动动画。
	- 具体的代码实现如下：

```css
/* 悬浮显示库目录 */

body:not(.is-mobile) .workspace-split.mod-left-split .workspace-sidedock-vault-profile{
    opacity: 0;
    transition:all .3s ease-out .2s;
}

body:not(.is-mobile) .workspace-split.mod-left-split .workspace-sidedock-vault-profile:hover {
    opacity: 1;
    transition:all .3s ease-out .2s;
} 
```

5. 最终效果图预览：

![GIF 2024-6-9 19-20-25.gif](https://s1.vika.cn/space/2024/06/09/3bc9f891de194438a2e594adfbb5efcf)
