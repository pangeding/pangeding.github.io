---
layout: home
title: 首页
---

# 欢迎来到我的技术博客

这里记录我在编程和技术探索过程中的心得体会。

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