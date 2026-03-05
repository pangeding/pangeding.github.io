---
layout: post
title: "Claude Code 使用指南"
date: 2026-03-01
categories: [AI, 工具]
tags: [claude, deepseek, 编程工具]
---

作为古法编程者，终于是用上了超强的 Claude code 啦！

## 1. 安装 Claude code
![Claude Code安装界面]({{ site.baseurl }}/assets/images/posts/2026-03-01-use-claude-code/1.png)

出现以上界面就可以了，直接连 Anthropic 是没法连的

## 2. 系统变量更新 （重点）
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

 `DEEPSEEK_API_KEY` 替换为您自己的 DeepSeek API 密钥。

## 3. VSCode 插件安装（可选）
我自己是直接使用命令行的

plugin 存在的问题是会强制你官方登录，由于我也不是一个重度用户，所以暂时没有寻找到可行的解决方案

根据这篇文章，
https://www.cnblogs.com/yangykaifa/p/19672410 \
修改 claude.json
改了不行就用 cc-switch，一个github仓库来换模型。

我比较习惯用命令行，就懒得换了，还有别的事情要做或者学习。

## 4. 使用体验
我尝试让 Claude code 生成一个 CLAUDE.md

- 花了 10w tokens
- 进行了 68 轮对话
- 感觉有点贵

后续考虑使用 codex 代替

![使用效果]({{ site.baseurl }}/assets/images/posts/2026-03-01-use-claude-code/2.png)

再更：发现claude code 用 deepseek 的 api，真的不贵了，第一次任务是因为上下文太长了才比较贵。

后面搞完整项目也就花了1块左右，很划算了。

再报：codex 的换模型太差了，只能用 GPT，我哪里用得起。