---
title: "从 Prompt 到 Harness"
date: 2026-04-05T12:00:00+08:00
categories: ["技术"]
tags: ["AI", "Claude", "开发工具"]
---

# 从 Prompt 到 Harness

从 deepseek，豆包网页端，app 端，到 windsurf IDE 内置 ai agent（此时我还没有发现后者有多大的优势），到 vscode 内置 agent（可以试用 Claude Haiku），再到 Claude code 插件，我说 ai cli，或者说 agent 真好用，claude 牛逼。学到了 api 的调用方法，token 数量的大小概念（一百万十分钟就用完哦！），顺便了解了 api 调用具有最大长度（几百 k），输入和输出是分开的，输入时还分有没有命中缓存区。所谓缓存区就是你之前问过类似的问题，那么 ai 就能直接照抄之前的回答，不需要重新思考。deepseek 真便宜，deepseek 牛逼。然后相同的模型不同的 cli 真的会有区别，而且还不小，比如 trae 和 Claude code 和 openclaw，都用同一个模型的 api，但是表现出来的效果不一样，这归功于 harness enginnering（怎么拼的？）。而我的认知还停留在 prompt engineering（孩子们我去查了词典了，上面那个错的就不管了）。

## 三个工程阶段

prompt enginneering -> context engineering -> harness engineering

context engineering，主要加强了上下文回顾的功能。就是不容易忘记前面的嘛。

## 马具（Harness）的比喻

harness，意思是“马具”，我觉得这个比喻非常形象。ai 就是马，人就是骑手，而马具的好坏是十分重要的。此处引申为“智能马具”，比如人发出要转向的需求，马具可以灵活调整让马知道这个转向的力度具体多大，效果才最好。

具体来说，以 Claude code 为例（Claude 牛逼），其 cli 将模型分为三个角色：planner，generater，reviewer，字面意思，非常形象。而这样的好处就是思路非常清晰，to do list 做的赏心悦目，每做完一项还会暂停，打勾，并提醒自己接下来的任务。属于是苦口婆心照顾容易半路出家的 generater 了。generater 没啥好说的。

至于 reviewer，一个很有趣的点是 reviewer 与 generater 是“独立的人格”，可以看作两个 ai（当然实际上还是调用的同一个模型同一个 session，但是具体的技术细节就不管了），因为 ai 对于自己生成的代码通常“过于自信”，确实，我也深有体会（“我已经完成了你的要求，具体亮点有：1，.... 2，.....”实际上就是一坨屎）。reviewer 包括测试，打回，评价等操作。而对于这三个角色，每一个都有大量的 prompt 去指导提示。所以现在理解了，harness 确实没有虚假宣传，而且 claude 真牛逼。

## 一点感悟

另外有一点，适当的限制 ai 比给他充分的自由有时候更好。因为 ai 太乖了。对。给他大量的工具，包，之类的，他只会感到困惑，尝试尽量把给他的东西全部都用到，尽管他的工作并不需要用到这么多。

## 题外话

还有，前两天 Claude code 的部分源码意外泄露，又养活了很多营销号，当然也肯定有很多有水平的人在学习的。用 claude 模型去研究 Claudecode 代码，原汤化原食。本是同根生...饿啊！