---
title: "LaTex公式入门"
date: 2023-02-04
tags: [折腾]
feature: https://s1.vika.cn/space/2023/02/04/a83a8827894f455ba62493a161d59c7a
published: true
hideInList: false
isTop: false
---

- 建立在Tex式上的格式，用于排版。
- 内置了大量的公式，为用户提供了极大便利。
- 命令以 `\` 开头，用 `$` 符号括起。

<!--more-->

## 希腊字母

### 小写字母

- 按照**希腊字母对照表**。  

### 大写字母

- 只需将对应**小写字母的首字母大写**。  
![普通运算符.png](https://s1.vika.cn/space/2023/02/02/ea59026d8d6a4f3783285161c53f9ef1)

## 上下标

### 下标

- 使用下划线 `-`

### 上标

- 使用 `^`

> [!Tips]  
>当上下标多于一个字符时，需要用**大括号括起**。

- `$x^2$`  
	- $x^2$
- `$x_i$`  
	- $x_i$
- `$e^{x+y+z}$`
	- $e^{x+y+z}$

## 分式与根式

### 分式

- 采用 `\frac{}{}` 来表示，其中第一个 `{}` 为分子，第二个 `{}` 为分母。

### 根式

- 采用 `\sqrt[]{}` 表示，其中第一个 `[]` 表示开几次方根，第二个 `{}` 表示被开方数。

`$\frac{ a }{ b }$`  
$\frac{ a }{ b }$  
`$\sqrt{ 2 }$`  
$\sqrt{ 2 }$  
`$\sqrt[ 3 ]{ 4 }$`  
$\sqrt[ 3 ]{ 4 }$

## 普通运算符

### 二元关系符

- 所有的二元关系符都可以加`\not`前缀得到相反意义的关系符，例如`\not=`就得到不等号(同`\ne` ）。  
![image.png](https://s1.vika.cn/space/2023/02/04/282afcddc60343719e1baf1e0a7b449b)

### 二元运算符

![image.png](https://s1.vika.cn/space/2023/02/04/0141a23336034042a189538e8ba0ea6a)

## 大型运算符

- 注意，通常情况下，求和 `/` 求积符号的上下界条件显示在符号的右侧如果想让其显示在下侧，需要在求和号后加 `\limits` 做限制。  
`$\sum_{i=O}^{n}x_i$`渲染后的结果为$\sum_{i=O}^{n}x_i$

`$\sum\limits_{i=O}^{n}x_i$`渲染后的结果为$\sum\limits_{i=O}^{n}x_i$  
![image.png](https://s1.vika.cn/space/2023/02/04/c5f7a5ce4f0f40e1834a0a28ad2dd921)

## 标注符号

### 数学重音符号

![image.png](https://s1.vika.cn/space/2023/02/04/de953ccde1df4a468b0682995543ac7b)

### 作为重音的箭头符号

## 箭头

![image.png](https://s1.vika.cn/space/2023/02/04/83e9098745f447f1908206c2541f3283)

## 矩阵

`$$\begin{括号类型} 值 & 值 & 值\\ 值 & 值 & 值 \end{矩阵类型}$$`  

实例

```
$$\begin{equation}
	\begin{gathered}
	\begin{matrix} 0 & 1 \\ 1 & 0 \end{matrix}
	\quad
	\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}
	\quad
	\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}
	\quad
	\begin{Bmatrix} 1 & 0 \\ 0 & -1 \end{Bmatrix}
	\quad
	\begin{vmatrix} a & b \\ c & d \end{vmatrix}
	\quad
	\begin{Vmatrix} i & 0 \\ 0 & -i \end{Vmatrix}
	\end{gathered}
\end{equation}$$
```

$$\begin{equation}
	\begin{gathered}
	\begin{matrix} 0 & 1 \\ 1 & 0 \end{matrix}
	\quad
	\begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}
	\quad
	\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}
	\quad
	\begin{Bmatrix} 1 & 0 \\ 0 & -1 \end{Bmatrix}
	\quad
	\begin{vmatrix} a & b \\ c & d \end{vmatrix}
	\quad
	\begin{Vmatrix} i & 0 \\ 0 & -i \end{Vmatrix}
	\end{gathered}
\end{equation}$$
