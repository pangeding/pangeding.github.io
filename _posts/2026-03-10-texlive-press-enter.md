---
layout: post
title: "wsl安装texlive-full卡在Pregenerating ConTeXt MarkIV format. This may take some time..."
date: 2026-03-10
categories: [环境]
---

如题所示，我卡了很久，吃完饭回来发现都没有安装成功。

问 Gemini，先 kill 了进程，但最后又回到了没有完成的任务

`sudo kill 64247` \

`sudo dpkg --configure -a` \

然后又回到了熟悉的

Pregenerating ConTeXt MarkIV format. This may take some time...

Gemini 给出一个搞笑一样的建议，连续按 enter。

结果就真的安装成功了。

pdflatex --version 显示版本成功。

我觉得这太可笑了，问问 Gemini，他给我的解释是：

1. WSL 和 windows 的交互是非同步的

2. 任务已经完成，但输出还卡在管道里

3. 通过按 enter 键，输入 stdin，最终使管道畅通。
