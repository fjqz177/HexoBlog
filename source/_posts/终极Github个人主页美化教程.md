---
title: 终极Github个人主页美化教程
date: 2023-01-01 23:10:26
categories:
  - 笔记
tags:
  - Markdown
mathjax: true
abbrlink: 7
---
先带大家看一下我的[Github首页](https://github.com/fjqz177)
![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301012334640.gif)
酷吧，虽然咱代码不会写，但气势绝对不能输，逼格总是要先装起来的，装着装着，说不定，就会写代码了呢！！！（大误 😄）

接下来就教你们如何装逼

<!--more-->

# 0.准备工作

首先需要新建一个和 Github 用户名相同的仓库
![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301012343960.jpg)
记得勾选`Add a README file`这个选项
接下来在自己电脑上创建一个`.md`后缀的文件，名称随意，并用支持`Markdown`语法的编辑器编辑，当然嫌麻烦可以用[https://md.mzr.me](https://md.mzr.me/)或者其他你喜欢的在线编辑器编辑

# 1.带有打字特效的文字

打字特效生成网站：[Readme Typing SVG - Demo Site](https://readme-typing-svg.herokuapp.com/demo/)
![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301012350411.jpg)
里面有很多自定义选项，大家可以根据自己喜好进行调整
调整完以后点击`Markdown`下的`Copy To Clipboard`，然后粘贴进刚才的`.md`编辑器里
效果图
<p align="center">
    <a href="https://fjqz177.github.io"><img src="https://readme-typing-svg.herokuapp.com?font=consolas&weight=100&size=45&duration=4000&pause=4000&center=%E7%9C%9F%E7%9A%84&vCenter=%E7%9C%9F%E7%9A%84&multiline=true&width=420&height=70&lines=fjqz177.github.io" alt="Typing SVG" /></a>
</p>

# 2.社交关注者数目小牌子

用 Substats 配合[shields.io](https://www.shields.io)制作动态小牌子  


  
动态图标  
  
创建动态图标方法：点击进入这个网页 [shields.io dynamic-badge](https://shields.io/#dynamic-badge)  
  
> `data type`选择`json`
> `label`写上数据牌左侧你想展示的文字，比如我想展示的是`GitHub`
> `data url`，找到自己想展示的`API URL`，比如我的`GitHub URL`就是：`https://api.spencerwoo.com/substats/?source=github&queryKey=fjqz177`。一般都只需要修改`source`后面的目标服务器以及`queryKey`后面的请求数据标签，前者一般都是平台名，后者一般都是用户名
> `query`填：`$.data.totalSubs`
> `color`填写一个十六进制的颜色代码，前面不加#
> 剩下两个分别是数据牌右侧展示数据的前缀和后缀，前缀可以不填，后缀可选填`followers`

![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301020010223.png)
然后点击`Make Badge`即可生成
以如下格式填入刚才生成的链接，并把它粘贴进`.md`编辑器内
```
![](https://img.shields.io/badge/dynamic/json?color=272626&label=Github&query=%24.data.totalSubs&suffix=%20followers&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3Dfjqz177)
```
效果如下
![](https://img.shields.io/badge/dynamic/json?color=272626&label=Github&query=%24.data.totalSubs&suffix=%20followers&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3Dfjqz177)
大家可以查阅`Substats API`的文档：[Home | Substats Docs (spencerwoo.com)](https://substats.spencerwoo.com/)看看支持哪些平台以及`source`后面的目标服务器的关键字，举一反三即可生成你想要的小牌子
给大家附上我自己带图标的小牌子
```html
<p align="center">
<a title="github" target="_blank" href="https://github.com/fjqz177"><img src="https://img.shields.io/badge/dynamic/json?label=GitHub&suffix=%20followers&query=%24.data.totalSubs&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3Dfjqz177&labelColor=282c34&color=353940&logo=github&longCache=true" ></a>
<a title="weibo" target="_blank" href="https://weibo.com/5862441076/profile"><img src="https://img.shields.io/badge/dynamic/json?labelColor=e71f19&color=353940&label=Weibo&suffix=%20followers&query=%24.data.totalSubs&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dweibo%26queryKey%3D5862441076&logo=sina-weibo&longCache=true" ></a>
<a title="zhihu" target="_blank" href="https://www.zhihu.com/people/fjqz177"><img src="https://img.shields.io/badge/dynamic/json?color=353940&labelColor=0084ff&label=Zhihu&suffix=%20followers&query=%24.data.totalSubs&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dzhihu%26queryKey%3Dfjqz177&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBzdGFuZGFsb25lPSJubyI/PjwhRE9DVFlQRSBzdmcgUFVCTElDICItLy9XM0MvL0RURCBTVkcgMS4xLy9FTiIgImh0dHA6Ly93d3cudzMub3JnL0dyYXBoaWNzL1NWRy8xLjEvRFREL3N2ZzExLmR0ZCI+PHN2ZyB0PSIxNjMzMjY1Mzc4NzU2IiBjbGFzcz0iaWNvbiIgdmlld0JveD0iMCAwIDEwMjQgMTAyNCIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHAtaWQ9IjUxNTMiIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCI+PGRlZnM+PHN0eWxlIHR5cGU9InRleHQvY3NzIj48L3N0eWxlPjwvZGVmcz48cGF0aCBkPSJNNTc2LjggODA3LjUyaDU3LjI4bDIwLjggNzIuNDggMTAwLjgtNzIuNDhoMTQxLjkyVjIyOS4yOEg1NzYuOHogbTY3Ljg0LTUxMy45Mkg4MzJ2NDQ4aC02Ni4yNGwtODUuMTIgNjQuOTYtMTguNTYtNjQuOTZoLTE3LjQ0ek0xMjYuNCA4ODQuNDhhMTQ5LjQ0IDE0OS40NCAwIDAgMCAxMjMuODQtMTAuNGM2MC45Ni0zNiAxMDUuOTItMTk0LjU2IDEwNS45Mi0xOTQuNTZsMTQ0IDE3Ny40NHMxMy4xMi04NC40OC0yLjI0LTEwOC4zMi05OS4wNC0xMTkuODQtOTkuMDQtMTE5Ljg0bC0zNi42NCAzMiAyNi4wOC0xMDQuOTZINTQ0czAtNjEuNzYtMzAuNTYtNjUuMjgtMTI1LjQ0IDAtMTI1LjQ0IDB2LTE5Mkg1MjhzLTEuNi02NC0yOC44LTY0SDI3MC41NmwzNS41Mi0xMDQuNjRzLTU3LjYgMy4zNi03Ny45MiAzOS4zNi04Ni40IDIyMS42LTg2LjQgMjIxLjYgMjEuOTIgMTAuMjQgNTkuMi0xNy4yOGExNDcuNjggMTQ3LjY4IDAgMCAwIDQ5LjI4LTc1LjUybDY3Ljg0LTMuMzZMMzIwIDQ5MS4ycy0xMTYuOTYtMS43Ni0xNDAuNjQgMC0zNy4yOCA2NS4yOC0zNy4yOCA2NS4yOEgzMjBzLTE1LjIgMTA4LjE2LTYwLjk2IDE4Ny4yLTEzMi42NCAxNDAuOC0xMzIuNjQgMTQwLjh6IiBmaWxsPSIjZmZmZmZmIiBwLWlkPSI1MTU0Ij48L3BhdGg+PC9zdmc+&longCache=true" ></a>
<a title="bilibili" target="_blank" href="https://space.bilibili.com/436591517"><img src="https://img.shields.io/badge/dynamic/json?color=353940&labelColor=f27596&label=Bilibili&suffix=%20followers&query=%24.data.totalSubs&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dbilibili%26queryKey%3D436591517&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAD7ElEQVR4nO2dW9WrMBCFK6ESkFAJSKiESqgEHCABCZWAhEpAAhL2ecik5dDc/pXLBDLfWnlqy0xmJ5BMQnq5CIIgCIIgCIIgCIIgCEIBAHQAemYfrgCunD6wAKAHsEKxALgx+bCQD8/S9tmgVqeDr1lLigDgZvDhXso+K9TyTBQRwRJ8AHjntl0Flh5QRAQK/mKxPeayWx2OXpBNBKiHvi34b7T2MC4pAvW6twR/RwkRKPizBN8CgEcuESj4Lwm+BwBjahEk+H8EwJRKhOaCDzW8e1JLfkUUH1NgmR3XmHffHR1l+72BSs8d7w8U+JDAnZERQMcV+CtUi7dNqFqibB4J7vtrq7xKCuAasbTMXCL4T+5aVk6+2xHUrWdhruAR6HIJcOeu2UHI8zyAe2ytWfEdWz9PVvQ8YAmIQ5dDAB9LFsMVAv8oMO2zAGrC5WNIarRiAuKR9jYEd9pY08aa6uUzIHGRdkgKd8pY0yc1WjEBAqypDYoAG0QAZkQAZkQAZkQAZk4vANQenjsSzS3I/wcSbXU5jQBUkRtdf4Rar90v8kSv3+I3ffCCSpk8I/w+lgDkdI/v2rEp2CaiWm1AsDQLlDAD+dlFXLMeAaCSeLZdaSFE5VUQNot38cKuEeBgAsSuG0flVZBmEanbXfNQAsS0fgBYIn2fIu3/BBMHEyBmDXlFfA8IzeHb+Ems4WAChKykrVA9ZfsQTL57jXzRg4A5wC/A8N4ADiZAZwm2XjW75Qh2KOTfA0p4kygPw28OJcCVgn3nDnYo2EwEYRgGH0qAMyICMCMCMCMCMCMCMCMCMCMCfP3qwHDOQ4AAUekTk8FaBRihJnZdYbvtCGC7LvmkM63GjVDINPFrQgCq5ETXfmMzI90FXzPvfqt7x4rEu/ZaEcCUxFvgz2zO+BUn6UkoaEEAsptiMSX5e8FoRYCN7cVgb4Vq7U/H50Pq4JNP7Qiw8UFnJwcK+tXy+Wj6PLEvPgHSHv5UgwA1IQIwwyFAyLJin9RoxYgAzAQIkPwNmf26busC+OIx5TDqo5nDT+F/SS/9CYzwb+No49zNy2evkYv0LywGGAXUvp6eSneycqOic0w20k7CNgKE7jJunSGLACTCxF27ylmQc98T5MQUH49swd+I0HPXslLKnT0N+wnkrTKi9JZL/L9i1SorMmdeQ4TQQ7OFMxIMzGD45w8nUL1im7efENZLJpgPSw0pfz0cdt4U3230Td/Tvx2R6d2FrHhEWLkq5PELOMsRPHCPnAZGv1xJteL7jbJiaW3sB2nDvPC/osSYvjRQz4cJ6n7KO3rYQL7M+L6nVtfDVRAEQRAEQRAEQRAEIZ5/SAXmdfXaoQsAAAAASUVORK5CYII=&longCache=true" ></a>
<a title="coolapk" target="_blank" href="https://www.coolapk.com/u/3880429"><img src="https://img.shields.io/badge/dynamic/json?color=30343b&labelColor=17a15e&label=Coolapk&suffix=%20followers&query=%24.data.totalSubs&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dcoolapk%26queryKey%3D3880429&logo=data:image/svg+xml;base64,PHN2ZyBjbGFzcz0iaWNvbiIgdmlld0JveD0iMCAwIDEwMjQgMTAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB3aWR0aD0iNjQiIGhlaWdodD0iNjQiPjxkZWZzPjxzdHlsZS8+PC9kZWZzPjxwYXRoIGQ9Ik0xMjcuODkzIDQyNi42NjdjMjkuOTItNjYuOTg3IDk0LjUwNy0xMTYuNjk0IDE2Ni40LTEzMC4zNDcgNTUuNzg3LTkuNiAxMTIuOTYgNS4wNjcgMTYxLjkyIDMxLjk0N0M0OTcuNzYgMzQ5LjQ0IDUzNC40IDM3OC44OCA1NjcuOTQ3IDQxMS4wNGMtMTYuMTYgMTguNC0zOS4wOTQgMjguODUzLTU3LjQ5NCA0NC43NDctNDYuMTMzLTM4Ljg4LTk2LjY0LTc3LjcwNy0xNTcuOTczLTg3LjA5NC03OC45MzMtMTMuMTczLTE1OC41NiA0OS4yMjctMTcwLjUwNyAxMjcuMTQ3LTguNjkzIDQ1LjkyIDEwLjEzNCA5NC42NjcgNDUuMTc0IDEyNC45MDcgMzkuNjggMzQuOTg2IDk3LjIyNiA0NC41ODYgMTQ3LjYyNiAzMS4yNTMgNTcuNi0xMy45MiAxMDEuOTc0LTU3LjA2NyAxMzYuODU0LTEwMi43NzMgNTQuMDgtNzIuMTA3IDk5LjItMTUwLjQgMTQ3Ljg0LTIyNi4xMzQgMTMuOTItMTkuMTQ2IDQ3LjQxMy0xNy4yMjYgNTguNzIgMy44NCA2My42MjYgMTA5LjAxNCAxMjYuMDggMjE4LjcyIDE4OS42IDMyNy43ODcgNy41NzMgMTUuMDkzIDQuNDI2IDM1Ljc4Ny05LjYgNDYuMTMzLTEzLjA2NyAxMC42MTQtMzMuMzM0IDEwLjI0LTQ2LjEzNC0uNjkzYTk3MDY2LjU1OCA5NzA2Ni41NTggMCAwMS0yMjYuMTg2LTE2Mi43MmMxOC44OC0xNS4wNCAzOC40LTI5LjMzMyA1Ny45NzMtNDMuNDY3IDIzLjczMyAxMi45MDcgNDMuNzg3IDMzLjE3NCA2OS42IDQxLjY1NC0yMC4zNzMtMzkuNTc0LTQzLjYyNy03Ny43MDctNjYuMzQ3LTExNS45NDctNDIuNjY2IDU5LjE0Ny03Ny4wNjYgMTI0LjIxMy0xMjMuMTQ2IDE4MS4wNjdDNTE2IDY2My40NjcgNDQ4LjggNzE2Ljk2IDM2OC42NCA3MjguNDhjLTM4Ljg4IDMuNDEzLTc5LjMwNyA0LjIxMy0xMTYuMzczLTkuOTczLTUzLjQ5NC0xOS4xNDctMTAwLjMyLTU4LjcyLTEyNC41ODctMTEwLjU2LTI4LjIxMy01Ni4xMDctMjYuNzczLTEyNS4wMTQuMjEzLTE4MS4yOHoiIGZpbGw9IiNmZmYiLz48L3N2Zz4=&longCache=true" ></a>
</p>
```
只需将对应`title`后面的`href`里的链接替换成自己的，然后把`src`后面的链接里的`fjqz177`或者对应的`id`号改成自己的就可以了（`queryKey%3D`后面的那一串）
> 图标是使用 base64 将 svg 进行转码的，所以很长~~

# 3.贪吃蛇吃绿点

![](https://raw.githubusercontent.com/fjqz177/fjqz177/main/assets/github-contribution-grid-snake.svg)

在仓库里点击`Creat new file`
![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301020102436.jpg)
将`.github/workflows/generate_snake.yml`粘贴进图示框中
![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301020105189.jpg)
在底下的框中粘贴如下代码

```yml
# GitHub Action for generating a contribution graph with a snake eating your contributions.

name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v2.3.4
      
      - name: Generate Snake
        uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          gif_out_path: ./assets/github-contribution-grid-snake.gif
          svg_out_path: ./assets/github-contribution-grid-snake.svg

      - name: Push to GitHub
        uses: EndBug/add-and-commit@v7.2.1
        with:
          branch: main
          message: 'Generate Contribution Snake'
```
将如下粘贴进刚才的`.md`编辑器里
```
![](https://raw.githubusercontent.com/fjqz177/fjqz177/main/assets/github-contribution-grid-snake.svg)
```

# 4.GitHub Stats Card & Most used languages

效果如下

<div align="center">
<span>&emsp;&emsp;</span>
<img height="170px" src="https://github-readme-stats.vercel.app/api?username=fjqz177" /><span>&emsp;&emsp;</span><img height="170px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=fjqz177&layout=compact&langs_count=8" />
<span>&emsp;&emsp;</span>
</div>

代码放在这里了，只需将其中的`fjqz177`替换成你自己的`Github`名称即可

```html
<div align="center">
<span>&emsp;&emsp;</span>
<img height="170px" src="https://github-readme-stats.vercel.app/api?username=fjqz177" /><span>&emsp;&emsp;</span><img height="170px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=fjqz177&layout=compact&langs_count=8" />
<span>&emsp;&emsp;</span>
</div>
```

# 5.Github-Readme-Activity-Graph（GitHub 活动统计图）

[![Ashutosh's github activity graph](https://github-readme-activity-graph.cyclic.app/graph?username=fjqz177&theme=github-light)](https://github.com/ashutosh00710/github-readme-activity-graph)

将其中的`fjqz177`替换成你自己的`Github`名称即可

```
[![Ashutosh's github activity graph](https://github-readme-activity-graph.cyclic.app/graph?username=fjqz177&theme=github-light)](https://github.com/ashutosh00710/github-readme-activity-graph)
```

# 6.GitHub Streak（GitHub 连续打卡） & Github Trophy（Github 奖杯）

<div align="center">
    <img  src="https://github-readme-streak-stats.herokuapp.com/?user=fjqz177" />
    <img  src="https://github-profile-trophy.vercel.app/?username=fjqz177" />
</div>

将其中的`fjqz177`替换成你自己的`Github`名称即可

```html
<div align="center">
    <img  src="https://github-readme-streak-stats.herokuapp.com/?user=fjqz177" />
    <img  src="https://github-profile-trophy.vercel.app/?username=fjqz177" />
</div>
```

# 7.Logo小牌子

![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301020114512.jpg)
怎么样，这么多牌子挂出来是不是被吓到了呢
在这里需要用到[Simpleicons](https://simpleicons.org/)这个网站
以及如下模板
```
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=Git&logoColor=white)
```
![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301020123481.jpg)
> 1.不会显示在外面，建议写上想要显示的Logo名称，方便管理
> 2.小牌子右边显示的文字，建议写上想要显示的Logo名称
> 3.牌子的底色
> 4.显示的Logo

打开上面的Simpleicon的网址，找到你想要的Logo
![](https://img-1316367741.cos.ap-shanghai.myqcloud.com/img/202301020127540.jpg)
将（1）的文字复制，替换掉1. 2. 4.的原有内容
鼠标移到（2）上点一下即可复制，然后替换掉3.中原有内容，记得删除`#`号
举一反三，想加什么自己加就行

---
还没写完