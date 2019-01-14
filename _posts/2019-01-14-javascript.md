---
layout: post
title: "java script"
date: 2014-07-22 16:25:06 -0700
comments: true
categories: web javascript
tags: #javascript
---
JavaScript 是Web的编程语言。[学习网址](http://www.runoob.com/js/js-tutorial.html)
所有现代的HTML页面都使用JavaScript。

1. HTML 定义了网页的内容
2. CSS 描述了网页的布局
3. JavaScript 网页的行为

    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8">
    <title>菜鸟教程(runoob.com)</title>
    <script>
    function displayDate(){
        document.getElementById("demo").innerHTML=Date();
    }
    </script>
    </head>
    <body>

    <h1>我的第一个 JavaScript 程序</h1>
    <p id="demo">这是一个段落</p>

    <button type="button" onclick="displayDate()">显示日期</button>

    </body>
    </html>
