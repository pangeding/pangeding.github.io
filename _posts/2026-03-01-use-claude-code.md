```
---
layout: post
title: "Claude Code 使用指南"
date: 2026-03-01
---

专注于区块链开发

github: pangeding \
blog: pangeding.github.io \
公众号: pangeding \
（暂时未同步）博客园: pangeding \
（暂时未开发）小红薯

```


作为古法编程者，终于是用上了超强的 Claude code 啦！
# 1. 安装 Claude code
![1](.assets/260301-use-claude-code/1.png)
出现以上界面就可以了，直接连 Anthropic 是没法连的
# 2. 系统变量更新 （重点）
Claude code 相当与一个身体，而 ai model 相当于其大脑，我需要更换的就是把 Anthropic 大脑更换掉，变成 Deepseek

具体过程参考这篇文章
https://zhuanlan.zhihu.com/p/1985832650116715724

我将关键代码列出
```bash
export ANTHROPIC_BASE_URL=https://api.deepseek.com/anthropic
export ANTHROPIC_AUTH_TOKEN=DEEPSEEK_API_KEY
export API_TIMEOUT_MS=600000
export ANTHROPIC_MODEL=deepseek-chat
export ANTHROPIC_SMALL_FAST_MODEL=deepseek-chat
export CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1
```

DEEPSEEK_API_KEY 替换为自己的 sk- key

# 3. 安装 Claude code for vscode （可选）
我自己是直接使用命令行的

plugin 存在的问题是会强制你官方登录，由于我也不是一个重度用户，所以暂时没有寻找到可行的解决方案

根据这篇文章，修改一行 .claude.json 的配置是可行的，但是我的字段一开始就是对的，仍然无法连接，于是作罢。

我尝试让 Claude code 生成一个 CLAUDE.md

花了 10w tokens，进行了 68 轮对话，感觉有点贵

后续考虑使用 codex 代替
![2](.assets/260301-use-claude-code/2.png)

