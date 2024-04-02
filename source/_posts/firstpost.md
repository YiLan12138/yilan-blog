---
title: 第一篇博客——博客网站搭建学习笔记
date: 2024-03-30 15:48:02
tags:
- 笔记 
- 工具
category: work
timeline: work
toc: true
abstract: markdown语法和博客网站搭建过程中遇到的一些困难和解决办法
---


# Hi这是我的第一条博客
### ——首先当然是记录一下此次的博客网站搭建过程啦

###  第一章 mardown语法

虽然是今天最后学的 但应该之后会经常用就放到前面了

1. 引用块
“>引用”
>引用
>>套娃
>>>俄罗斯套娃说是

2. 代码段
``   <——这个东西是键盘上方数字键左边的“丶”
`hexo server`

3. 代码块
```c
#include<stdio.h>
int main()
{
    printf("hello world\n");
    return 0;
}
```
(好久之前写过 我居然还记得这种语言 神奇)
三个`加上语言类型c\python\Java\如然后再加三个丶

4. 公式块（latex语言）

$$\beta \times x \geq 30$$   
美元美元\beta \times x \geq 30美元美元


$$
\int_{1}^{4\alpha^2}dx\text{注释}
$$
美元美元
\int_{1}^ {4\alpha^2}dx\text{注释}
美元美元

5. *斜体* **粗体**
星号 斜体 星号  
星号星号 粗体 星号星号

6. 分隔符
---三个减号

---



7. 表格

在线表格生成https://tableconvert.com/zh-cn/

| A | B | C | D | E | F | 
|---|---|---|---|---|---|
| 1 | 2 | 3 | 4 | 5 | 6 | 

8. 分点 1. 2. 3. 4.
- 第一 
    -  第二
        - 第三


9. 图片插入HTML

<img src="/images/firstpost/life.jpg" width=200 heigth=200>    <img src="/images/firstpost/life.jpg" style="zoom:50%">

小于号img src="life.jpg" width=200 heigth=200大于号 
小于号img src="life.jpg" style="zoom:50%"大于号

10. 链接
`![图片](地址)`   `[文字](地址)`

![图片](/images/firstpost/yilan.jpg)

>[参考视频1](https://www.bilibili.com/video/BV1aU421o7yv/?spm_id_from=333.880.my_history.page.click)
[参考视频2](https://www.bilibili.com/video/BV1HP4y1P76Y/?spm_id_from=333.880.my_history.page.click&vd_source=f18e8748005694e44438cbc695c9bcc7)

11. 文章摘要
在 markdown 文件中使用 `<!--more-->` 可以截断文章，使得在这之前的内容可以作为 excerpt 显示在文章列表页。另外，也可以在Front-matter中设置 abstract 字段来设置隐藏式摘要。abstract 的设置不同于通过在正文使用 隔断的节录（excerpt）。abstract 的内容不会再出现在正文中，并且设置 abstrct 后会覆盖 excerpt 在文章列表的中的展示。

```
---
title: 隐藏式摘要测试
date: 2024-01-27 11:58:32
tags: text
category: featTest
cover: assets/hozen-durdledoor.jpg
abstract: "该文章测试隐藏式摘要功能，此文本只会在文章列表展示，文章正文中不再出现。"
---
```

---
### 第二章 博客搭建

博客网站的搭建是看的另一名博主的图文教程的，他的文章写的很完备
所以博客网站搭建的详细内容请看[原文](https://blog.cuijiacai.com/blog-building/#post-comment)，这里我只讲一下我在博客搭建中的经验和问题

 - **ChatGPT帮了我大忙**

从git bash反馈给我第一条日志开始，我就一直在问gpt发生了什么和我该怎么操作 ，你可以看到我问gpt问的多傻多业余而gpt给我的回答多么专业准确详细，以至于我几乎是复制粘贴着就完成了此次博客网站的搭建。

所以说GPT真好用吧，把专业的壁垒又打破了些，把困住我们的格子间又扩大了些。把由各种不同的语言，包括不同民族的不同专业的抽象的象形的语言，不断发展过程中建立起来的壁垒打碎然后还原成最纯粹的最原始的每个人都能懂的语言。真的牛逼 [原文](https://www.bilibili.com/video/BV1sM411V7MG/?spm_id_from=333.337.search-card.all.click&vd_source=f18e8748005694e44438cbc695c9bcc7)

- **博客的美化**

感谢原博主分享的[致远主题](https://github.com/hooozen/hexo-theme-tranquility)

- **Git 更新**
```
git add .
git commit -m "Update"
git push origin main
```