---
layout: home
title: 首页
---

# 欢迎来到我的技术博客

专注于区块链开发

github: pangeding \
blog: pangeding.github.io \
公众号: pangeding \
（暂时未同步）博客园: pangeding \
（暂时未开发）小红薯

## 最新文章

<ul>
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt }}</p>
      <small>发布于 {{ post.date | date: "%Y年%m月%d日" }}</small>
    </li>
  {% endfor %}
</ul>