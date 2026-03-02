---
layout: home
title: pangeding web3 AI
---

# 欢迎来到我的技术博客

专注于区块链开发

github: pangeding \
blog: pangeding.github.io \
公众号: pangeding \
博客园: pangeding \
小红薯: pangeding 95581589128

## 文章分类
<div class="categories">
  <a href="/category/ai">AI</a>
  <a href="/category/web3">Web3</a>
  <a href="/category/区块链">区块链</a>
</div>

## 最新文章

<ul>
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <small>发布于 {{ post.date | date: "%Y年%m月%d日" }}</small>
      {% if post.categories %}
        <div class="post-categories">
          分类：
          {% for category in post.categories %}
            <a href="/category/{{ category | slugify }}" class="category">{{ category }}</a>
          {% endfor %}
        </div>
      {% endif %}
    </li>
  {% endfor %}
</ul>