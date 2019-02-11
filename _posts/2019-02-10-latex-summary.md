---
layout: post
title: "latex summary"
date: 2019-02-10 
comments: false
categories: latex
tags: #latex 
---
[使用latex撰写elsevier论文，latex表格，插图以及调用的安装包](http://www.voidcn.com/article/p-wfcwlvtp-dx.html)

最近尝试用latex书写elsevier的论文，因为word的公式排版太难看了，但elsevier给出的latex模板十分简单，很多地方还需要自己去调整，对于latex的新手来说，还是有点吃力。自己先慢慢总结，然后将使用心得和技巧撰写在博客上。


推荐使用 www.overleaf.com 在线latex网站编辑，可以在上面找到elsevier的模板。 


1. 首先设置使用的模板

elsevier 给出了下列选项，选择其中之一。这些模板设置了页边距，是否分栏，默认的字体类型及大小。


\documentclass[preprint,review,12pt]{elsarticle}
\documentclass[final,1p,times]{elsarticle}
\documentclass[final,1p,times,twocolumn]{elsarticle}
\documentclass[final,3p,times]{elsarticle}
\documentclass[final,3p,times,twocolumn]{elsarticle}
\documentclass[final,5p,times]{elsarticle}
\documentclass[final,5p,times,twocolumn]{elsarticle}

投稿时我选择的是 \documentclass[final,1p,times]{elsarticle}



2. 使用的安装包，导言区添加命令

根据需要，调用不同的安装包，我列出了以下安装包，并有中文注释。


\usepackage{graphicx}%插入图片

\usepackage{amssymb}%数学符号

\usepackage{amsthm}%数学定理

\usepackage{amsmath}%数学公式、矩阵、积分求和等

\usepackage{lineno}%显示行号

\usepackage{txfonts} %默认字体times new roman

\usepackage{enumitem}%项目编号

\usepackage{multirow} %多行合并

\usepackage{caption} %改变图表标题

\usepackage{txfonts} %默认字体times new roman

\usepackage{array} %\调用公式宏包的命令应放在调用定理宏包命令之前，也能控制表格

\usepackage{booktabs} %调整表格线与上下内容的间隔

\usepackage{longtable}%调用跨页表格

\usepackage{bm}%数学字体加粗

\usepackage{setspace} %调整一段文字的行间距

\usepackage{natbib} %参考文献管理包


导言区命令：


\biboptions{sort&compress}%参考文献可以压缩显示例如1-3

\allowdisplaybreaks[4] %允许公式跨页

\captionsetup[figure]{font=small,labelfont=bf,labelsep=period}%修改标题文字格式

\renewcommand{\figurename}{Fig.} %修改标题样式

\newcommand{\tabincell}[2]{\begin{tabular} {@{ }#1@{ }}#2\end{tabular}}   

%让表格内容自动换行，但仍然需要用到换行\\

2. 表格与图片

表格有两种，一种是普通表格，另一种是长表格

代码：

\begin{table}[ht]
\centering\small
\begin{tabular}[b]{*{9}{p{0.8cm}<{\raggedright}}}
\multicolumn{9}{l}{\small{\textbf{Table 4}}}\\
\multicolumn{9}{l}{\small{Solution of our algorithm without trade credit}}\\\specialrule{0.05em}{3pt}{3pt}
$X_{t}$  &9  &18  &0 &0  &0  &0   &0  &25\\\specialrule{0.05em}{2pt}{2pt}
$y_{t}$  &1   &1  &0  &0 &0  &0  &0  &1\\
$w_{t}$  &0 &0   &0   &0   &0   &20   &20   &0 \\
$z_{t}$  &0 &0 &0 &0 &0 &0 &0 &0\\
$I_{t}$  &0 &9  &0 &9  &0  &0  &0  &0\\
$B_{t}$  &280 &153  &531 &531 &531  &531  &531  &1181\\
\specialrule{0.05em}{2pt}{0pt}
\end{tabular}
\end{table}
\normalsize

显示效果如下：



长表格（可以跨页）

代码：

\small
\begin{longtable}{m{2.8cm}m{2.8cm}m{5cm}}
\multicolumn{3}{l}{\small{\textbf{Table 7}}}\\
\multicolumn{3}{l}{\small{Randomized generation scheme for the test problems}}\\\specialrule{0.05em}{3pt}{3pt}
Parameter  &No.  &Values\\\specialrule{0.05em}{2pt}{2pt}
$T$  &7 & 12,18,24,36,48,60,72\\
&&\\
\multirow{4}*{\emph{pdf} of $d_{t}$} &\multirow{4}*{4} &1. \emph{Exponential} with $\mu=150$ \\
                &          &2. \emph{Normal} with $\mu=150$, $\sigma^{2}=2500$\\
                &          &3. \emph{Normal} with $\mu=150$, $\sigma^{2}=900$\\
                &          &4. \emph{Normal} with $\mu=150$, $\sigma^{2}=100$\\
&&\\
\multirow{3}*{$c_{t}$ and $h_{t}$} &\multirow{3}*{2} &1. Both constant: $c_{t}=13$ and $h_{t}=1$\\
                &          &2. $c_{t}$ seasonally varying in [12 13 11 10]\\
                &          &~~~~$h_{t}$ seasonally varying in [0.5 1 1.5 1]\\ 
&&\\
\multirow{2}*{$p_{t}$}  &\multirow{2}*{2} &1. Uniformly distributed in [15 25]\\   
&                   &2. Seasonally varying in [15 25 16 18]\\
&&\\
\multirow{3}*{$B_{c}$}  &\multirow{3}*{3} &1. $B_{c}=s_{index}+c_{index}\max\{d_{t}\}$\\   
&                   &2. $B_{c}=s_{1}+c_{1}(d_{1}+d_{2})$\\
&                   &2. $B_{c}=s_{1}+c_{1}(d_{1}+d_{2}+d_{3})$\\
&&\\
\multirow{4}*{$\beta$} &\multirow{4}*{4} &1. $\beta=0.5$ \\
                &          &2. $\beta=0.3$\\
                &          &3. $\beta=0.1$\\
                &          &4. $\beta=0$\\
&&\\                
$s_{t}$  &1 &Constant: $s_{t}=1000$\\
\specialrule{0.05em}{2pt}{0pt} 
\end{longtable}\label{tab7}



显示效果如下：



 

插入图片就没有表格那么复杂了，没有那么多需要修改的地方，直接改动模板对应文字：

\begin{figure}[ht]  %插入图形时用latex编译[h]使图表不浮动
\centering\includegraphics[scale=1,trim=0 0 0 0]{1-1.eps}
\caption{Sketch of the production arrangement}
\end{figure}

显示效果：


3. 参考文献

用latex的 natbib 包管理参考文献比较好，将用到的参考文献复制到 那个bib 文件里。



elsevier 自带的模板格式有时候不符合特定杂志要求，需要修改 那个 bst 文件，推荐一个博客：http://blog.csdn.net/tinkle181129/article/details/49822171，修改后替换原 bst文件就行。