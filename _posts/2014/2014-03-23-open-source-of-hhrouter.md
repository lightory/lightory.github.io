---
layout: post  
title: HHRouter 开源后日谈
---

这周二，[火花](http://huohua.in)开源了一个小项目 [HHRouter](https://github.com/Huohua/HHRouter)，不到一周，已经获得不少关注。并且在 GitHub 的本日热门 Objective-C 项目榜中占据榜首连续两天，目前也在本周热门排列第四。尤其值得一提的是，关注者不仅有国内一线开发者，还包括 Twitter, Groupon, Airbnb 这类硅谷热门公司的工程师。

颇有成就感，撰文一篇纪念，也顺便聊聊 HHRouter 开源前后的一些事儿。

### URL Router

HHRouter 背后的理念是 URL Router，这并不是新鲜的理念，早在数年前 Facebook 的 Three20 中就有类似的实现。但在 HHRouter 的传播过程中，我注意到还是有许多人对此并不了解。

一言以蔽之，URL Router 即将 UIViewController 映射成 URL，从而支持通过 URL 进行界面跳转。是的，就和 Web 一样。当然，这并不是 Web Developer 转职为 iOS Developer 后所做的无聊玩具。URL Router 有着许多切实的好处。

首先，这能够减少 UIViewController 之间的耦合。在没有 URL Router 的世界，如果 aViewController 需要跳转到 bViewController，就必须依赖于后者，这很容易就造成错综复杂的依赖链。引入 URL Router 后，这些链条自然就被斩断。

其次，当每个界面都拥有唯一且不重复的 URL ，将带来额外的好处。譬如，你将更容易实现这些需求：Push 打开指定的界面、追踪用户浏览记录、开放 URL Scheme。

再次，当你尝试引入 Hybrid 架构时，你会发现用统一语言描述 Web View 和 Native View 多么幸福。

### HHRouter

刚才也有提到，URL Router 并不是新鲜的理念，那我们为什么重造一个轮子呢？

答案自然是对于现在的轮子不够满意。Three20 太臃肿自然不必再提，而其他 Router 也在设计或实现上有着不自然之处。

HHRouter 的设计哲学是 Clean, Fast & Flexible。

HHRouter 不依赖于其他库，自己实现了一套简单的 Mapping 算法，核心代码只有 60 行。算法虽简单，但也做过专门优化，不像某些 Router，每次寻址就是做一次完整的遍历...

HHRouter 避免做太多事情，譬如对于界面跳转的控制，每个 App 都可能存在差异，HHRouter 就干脆放手不管。正因为心无旁骛，只做 URL Mapping，才能专心把这件事做好，做到极致。譬如对 [URL Query Params](https://github.com/Huohua/HHRouter#url-query-params) 的支持，以及对 [App 自定义 URL Scheme](https://github.com/Huohua/HHRouter#one-more-thing) 的支持。

### Marketing

一些同学关心的问题是，HHRouter 是如何获得这么多关注的？

我在 Reddit, V2EX, Weibo, Twitter 上公布了 HHRouter 开源的消息，这带来了第一批的流量，让 HHRouter 进入了 GitHub Trending 页面，这又带来了后续的流量。

仅此而已，并非特地做过什么推广。问题的答案其实在前文就已提到。比起关心推广，不如将更多精力花在产品的定位与打磨。

### Open Source

事实上，HHRouter 的主要代码都是在一年多前写的。此番只不过是做些整理。这不是单一的事件，而会是[火花](http://huohua.in)拥抱开源的一个开始。

为什么要拥抱开源？推荐阅读这篇《[Open Source (Almost) Everything](http://tom.preston-werner.com/2011/11/22/open-source-everything.html)》，作者 Tom Preston-Werner 是 GitHub Co-Founder。

引用文中我特别青睐的一段:

> When I start a new project, I assume it will eventually be open sourced (even if it's unlikely). This mindset leads to effortless modularization. If you think about how other people outside your company might use your code, you become much less likely to bake in proprietary configuration details or tightly coupled interfaces. This, in turn, leads to cleaner, more maintainable code. Even internal code should pretend to be open source code.

无论如何，请期待火花的更多开源作品 :)