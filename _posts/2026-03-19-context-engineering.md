---
layout: post
title: "context engineering"
date: 2026-03-19
categories: [AI]
tags: [claude, deepseek]
---

# Context Engineering 

## 1. 什么是 context engineering
上下文工程是一个重要的议题。

chat 到 agent 到 multiagent 都需要

将重要的语境保留给模型节点，让模型节点了解目前处境，减少幻觉的产生和自由发挥的概率

## 2. 和 prompt engineering 以及 RAG 有什么区别

context engineering 比上面两者都复杂

prompt engineering 局限于一个 LLM 节点内部

RAG 是一种保留上下文的重要手段，但它无法解决很多问题：如于世界交互，编辑文档，实时查询数据

## 3. 