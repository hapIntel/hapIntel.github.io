---
layout: post
title: "site generator"
date: 2019-01-11
author: hapIntel
tag: #jekyll
---


近年来，作为传统动态网站基础架构的替代方案，现代静态网站生成器日渐盛行。在 StaticGen 上有一个关于静态站点生成器的开源目录，2017 年该网站追踪了超过一百个生成器，并见证了这些生成器在这一年的流行趋势。本文整理了 StaticGen 目录中排名前 20 的静态网站生成器，排名顺序依据 Github 上的 Star 数。

# 静态站点生成器 Jekyll


Jekyll 是一个简单的免费的Blog生成工具，类似WordPress。但是和WordPress又有很大的不同，原因是jekyll只是一个生成静态网页的工具，不需要数据库支持。但是可以配合第三方服务,例如discuz。最关键的是jekyll可以免费部署在Github上，而且可以绑定自己的域名。

# Go 编写的静态网站生成器 Hugo
Hugo

Hugo 是 Go 编写的静态网站生成器，速度快，易用，可配置。Hugo 有一个内容和模板目录，把他们渲染到完全的 HTML 网站。Hugo 依赖于 Markdown 文件，元数据字体 。用户可以从任意的目录中运行 Hugo，支持共享主机和其他系统

# 静态博客网站生成器 Hexo


Hexo 是一个基于nodejs 的静态博客网站生成器，作者是来自台湾的 Tommy Chen。

特点：

不可思议的快速 ─ 只要一眨眼静态文件即生成完成

支持 Markdown

仅需一道指令即可部署到 GitHub Pages 和 Heroku

已移植 Octopress 插件

高扩展性、自订性

兼容于 Windows, Mac & Linux

# 基于 Git 制作电子书 GitBook
GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书，GitBook 并非关于 Git 的教程。



使用GitBook生成的电子书

GitBook支持输出多种文档格式：

静态站点：GitBook默认输出该种格式，生成的静态站点可直接托管搭载Github Pages服务上；

PDF：需要安装gitbook-pdf依赖；

eBook：需要安装ebook-convert；

单HTML网页：支持将内容输出为单页的HTML，不过一般用在将电子书格式转换为PDF或eBook的中间过程；

JSON：一般用于电子书的调试或元数据提取。

# ReactJS 静态网站生成器 Gatsby 
live-reloading example

Gatsby 可以使用 React.js 把纯文本转换到动态博客或者网站上。

特点：

无需重载页面转换

热重载编辑

为构建静态网站创建 React.js 组件模型和生态系统 

直观的基于目录的 URLs

支持 "Starters"

# Vue.js 后端渲染开源库 Nuxt.js


Nuxt.js 是一个通过 Vue 用于服务端渲染的简单框架，灵感来自 Next.js。 Nuxt 基于 ES2015，这使得代码有着更愉快，更整洁的阅读体验。它不使用任何转换器，并取决于 Core V8 实现的功能。

# 静态页面生成程序 Pelican
Pelican 是一个法国人用 python 写的用于生成静态页面的程序，支持：

博客文章和页面

使用外部服务 Disqus 实现的评论功能

支持主题

可对文章生成 PDF 文档

支持多语言发布文章

Atom/RSS feeds

代码着色

使用 LESS CSS (optional)

可导入 WordPress, Dotclear 或者 RSS feeds

集成外部功能 Twitter, Google Analytics, etc. (optional)

# 静态网站生成器 Metalsmith


一个非常简单，可插拔的静态网站生成器。在 Metalsmith 中，所有的逻辑都是由插件来处理的。 你只需将它们链接在一起。

# 前端 Web 应用程序构建工具 Brunch


Brunch 是一个轻量级的、优雅和简单的方法构建 HTML5 应用程序的框架，快速的前端 Web 应用程序构建工具，具有简单的声明性配置，用于快速开发的无缝增量编译。

# Ruby 编写的静态网站生成器 Middleman


Middleman 是一个 Ruby 编写的静态网站生成器，他可以让你使用几乎所有在Ruby Web开发中所使用的技术和工具来构建各种类型的静态网站。比如：在 Ruby on Rails 经常用到的 Sass、CoffeeScript、Sprockets、Erb & Haml 等，都可以在 Middleman 里使用。

11、静态网站生成器 MkDocs
Screenshot

MkDocs 可以同时编译多个markdown文件，形成书籍一样的文件。有多种主题供你选择，很适合项目使用。

MkDocs 是快速，简单和华丽的静态网站生成器，可以构建项目文档。文档源文件在 Markdown 编写，使用单个 YAML 配置文件配置。

# 静态网站生成器 Expose


Expose 是一个帮助图配文生成的静态网站生成器。

# 静态网页生成系统 Assemble


Assemble 是一个使用 Node.js，Grunt.js，Gulp，Yeoman 等来实现的静态网页生成系统。已被 Zurb Foundation, Zurb Ink, H5BP/Effeckt, Less.js / lesscss.org, Topcoat, Web Experience Toolkit 等数百个项目用来生成项目网站、主题、组件、文档、博客和 github 页面。

# 静态站点生成器 Wintersmith


Wintersmith 是一款静态站点生成器。它包括了内容（markdown，less，script 等），使用插件和输出静态网页（html，css，image 等等）来转换。它附带有 markdown 插件和 jade 模版。

# 静态网页生成器 Cactus
Cactus 是一个简单而强大的静态网页生成器程序，它使用 Python 和 Django 的模板系统。它的本地开发和在S3 上的部署都非常的简单。

因为目前的动态网站大部分都可以使用 JavaScript 来完成，这样实际上网页完全可以是静态的，而且静态网页速度非常快并且容易管理。所以才有了这个项目。

作者开发 Cactus 的目的是为了给设计师们提供一个标准而简单的系统，让他们能够快速的构建和部署一个速度很快的网站。

# React 的渐进式静态网站生成器 React Static


React Static 是一个 React 的渐进式静态网站生成器。它也是一个服务端渲染 React 应用的简约框架，旨在构建一个满足 SEO，网站性能和用户/开发人员使用体验的标准，帮助每个人无痛地构建下一代、高性能的网站。

功能特性

100% React。

快速运行，高性能构建。

数据平台不可知论者（Data Agnostic），可从任何地方提供你的网站数据。

为 ** SEO ** 而生。

React 优先的开发体验。

无痛的项目设置和迁移。

100％ 支持 React 生态系统。 包括 CSS-in-JS 库，自定义 Query 层（如 GraphQL），甚至 Redux。

# 静态网站生成器 DocPad 


DocPad  可以帮助生成具有布局，元数据，预处理器（markdown，jade，coffeescript 等等），部分，骨架，文件查看器，查询和完美的插件系统的网站前端。这大大减少了有经验开发者和初学者开发网站之间的不同，帮助用户更快速的建立自己的网站。

# JavaScript 编写的静态网站生成器 HubPress


HubPress 是一个由  JavaScript 编写的静态网站生成器，使博客维护更加简单。

主要特性：

提供 WYSIWYG 编辑器撰写博客
支持 AsciiDoc 标记功能，将内容按照用户需求呈现

管理控制台可以自定义博客内容的许多方面

Disqus 整合博客评论

利用Google Analytics 集成来跟踪访问者活动

附带多种主题，随时可以使用

# 模块化网站编译器 Phenomic


Phenomic 是一个模块化网站编译器，让网站构建更快、更简单。

# 静态网站生成器 Lektor


Lektor 是静态网站生成器，也是平面文件内容管理系统。Lektor 从静态文件的大量独立 HTML 页面构建出一个完整的项目，同时内置管理 UI 和极小的桌面应用。