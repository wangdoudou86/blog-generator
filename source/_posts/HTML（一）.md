---
title: HTML（一）
date: 2017-10-20 23:19:55
tags:
---
这篇博客主要为了巩固一下`<iframe>、<a>、<form>、<input>、<select>、<textarea>、<table>`这几个标签的常见用法。
一、 iframe
iframe 表示嵌套的浏览上下文，有效地将另一个HTML页面嵌入到当前页面中。说白点就是一个大的页面窗口里套一个小的页面窗口，这个小的页面窗口就是由iframe控制的。
1. `<iframe src="https://www.baidu.com" name="xxx"></iframe>`如下所示<br>
<iframe src="https://www.baidu.com" name="xxx"></iframe>


- **src** 属性规定在 iframe 中显示的文档的 URL；
可能的值：
  **绝对 URL** - 指向其他站点（比如 src="www.example.com/index.html"）
**相对 URL** - 指向站点内的文件（比如 src="index.html"）
2. `<iframe>`的name配合`<a>`标签的target使用

`<iframe name="xxx" src="#" frameborder="0"></iframe>`
`<a target="xxx" href="http://baidu.com">link</a>`

- 这样`<a>`的网址会在name为xxx的`<iframe>`中打开
- **frameborder=0**：不显示iframe的边框，一般都写上
- iframe的**src**支持相对路径；
二、 `<a>`
1. &lt;a&gt;标签的功能是**页面的跳转**，它发起的是**GET请求**，动作是**获取页面**
2. **target**属性，该属性指定在何处显示链接的资源
- target的四个值分别是**_blank**，**_self**，**_parent**，**_top**；
- **target =_blank**代表在新的窗口打开链接；
- **target =_self**代表在当前页面打开链接，**如果没有指定属性的话，默认为此值**；
- **target =_parent**代表加载响应到当前框架的父框架，如果没有parent框架或者浏览上下文，此选项的行为方式相同_self；
- **target =_top**代表加载到顶级窗口（浏览器上的那个窗口），如果没有parent框架或者浏览上下文，此选项的行为方式相同_self；
>注意：使用target时，考虑添加 rel="noopener norefferrer" 以防止针对 window.opener API 的恶意行为。
