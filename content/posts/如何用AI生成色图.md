---
title:  如何用AI生成色图
date: 2024-12-08
cover: /img/如何用AI生成色图.png
---

自己动手 丰衣足食
<!--more-->

ComfyUI 很简单，体积也很小，直接从github下载就行了，不用什么秋叶整合包。

Tag 的写法要经常查看 Danbooru，这就是字典，需要反复看。

如果是想模仿Pixiv上那些卖AI套图的人的投稿，那么这个问题我研究过。我自己的结论是这种套图色图就是八股文，可以有随机tag组合，但大部分还是需要自己写定义的。几个原因：
  1. 人们的性癖是自由的，但是每种性癖的表现方式却相当保守。某些姿势就是要配合某个视角，随机组合roll不到这个组合就没那味。某个背景就是要配合某种服装，穿着比基尼在赌场做总感觉不得劲。而从效率上来说，虽然某些姿势可能已经有自己的关键词了，但单独用总是会崩(有可能因为这个姿势超级小众或包含容易引起歧义的词汇)，非得要和某些其他tag一起同时出现才可以保证大部分出图都是正常的。
  2. 这些套图是设计过的，而不仅仅是关键词随机组合出来的。一般来说，画面的主题顺序是：
  全年龄的角色展示 -> 全年龄的两性接触 -> 即将前戏 -> 前戏 -> 激烈的前戏描述 -> 即将上垒 -> 上垒 -> 激烈的上垒描述 -> 事后。 这是一套相当俗套且固定的流程，你应该也已经发现每个阶段其实都要一组tag需要使用，更换这组tag可以对同一阶段有不同程度的描述。
  3. 这些卖图的人基本都是靠用户投票来决定下次做什么主题(主要是服装和角色)的，也就是说你只要实现一套随机的姿势库就可以了，服装和角色最好还是人工定下来，我们要保证套图里的角色具有一致的表现。

如果你使用的是comfyui，那么你可以试试这个 https://github.com/dannyliuuu/Easy_AI_Hentai 这个项目基本实现了我上面描述的流程。如果你只是想手工生成一些图，也可以用这个项目的配置文件做参考，这就是楼上说的”提前写一套提示词“。你设置好角色后，点击执行，它就会通过API向你本地部署的comfyui发送一大堆色色prompt，等上个把钟头，就可以回来人工筛选、打码、卖钱了(雾，我想要做的是让人人都有大量产套图的能力，这样Pixiv上的卖图仔就会消失了)。它的缺点是姿势库还很不完善，你可以帮忙测试添加。