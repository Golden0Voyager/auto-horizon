---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 28 条内容中筛选出 5 条重要资讯。

---

**科技新闻**
1. [OpenAI 提出困惑度作为模型智能的代理指标](#item-tech-news-1) ⭐️ 8.0/10
2. [奥莱利：硅谷与机制设计](#item-tech-news-2) ⭐️ 7.0/10

**科技博客**
1. [不确定时，不妨乱试](#item-tech-blog-1) ⭐️ 7.0/10

**财经新闻**
1. [美股 AI 科技股遭抛售，亚洲多地紧急稳定市场](#item-finance-news-1) ⭐️ 8.0/10
2. [蚂蚁集团领投具身智能公司 Simplexity Robotics 1 亿美元](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenAI 提出困惑度作为模型智能的代理指标](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI 发布文章，提出困惑度（perplexity）可作为衡量大模型智能的简单而有效的代理指标。文章将困惑度呈现为一个简洁的基准，用于追踪模型能力的进展，并认为这一指标与智能之间存在清晰对应关系。该论点属于观点性主张，而非已独立验证的突破，但为评估模型能力提供了一个比日益复杂的基准更简单的替代方案。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「背景」** 困惑度（perplexity）是语言模型在给定前文时预测下一个 token 的不确定程度，通常由固定留出集上的交叉熵损失计算而来；数值越低，表示模型对数据的压缩和预测越好。OpenAI 首席科学家 Jakub Pachocki 在 11 月 22 日发布的文章中提出，预训练交叉熵（以困惑度或对数困惑度衡量）是衡量语言模型底层智能进展的一致指标，并呼吁前沿实验室采用同一指标进行安全节奏管理。

**「对开发者的影响」** 微软已公开承诺在共同保留的评估集上分享其预训练进展，并报告 MAI-2 Base 的对数困惑度为 0.819，与 GPT-5.6 Sol 基础模型处于同一水平；由于使用相同分词器，数字可直接比较，这为开发者跨厂商比较基础模型困惑度提供了实际参照。

**「社区讨论」** 评论中，d\_burfoot 提出，困惑度与智能的对应关系初看令人惊讶，但回顾来看别无他途——智能的“魔力”在于从大量原始传感器数据中提取复杂世界模型，而原始数据流上的预测（即压缩）率正是衡量这一进展的指标。另有评论指出微软已加入这一努力，Mustafa Suleyman 在推文中将 MAI-2 Base 加入图表，其 log-perplexity 为 0.819。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence - OpenAI</a></li>
<li><a href="https://community.openai.com/t/perplexity-and-intelligence/1419510">Perplexity and Intelligence - Community - OpenAI Developer ...</a></li>
<li><a href="https://www.explainx.ai/blog/openai-pachocki-perplexity-intelligence-pacing-safety-november-2026">OpenAI Perplexity Metric: GPT Log-Loss Curve (Nov 2026 ...</a></li>
<li><a href="https://x.com/mustafasuleyman/status/2124663594449318173">Mustafa Suleyman on X: &quot;We fully support OpenAI&#x27;s ...</a></li>
<li><a href="https://www.techtwitter.com/tweet/86327c55-7454-4d6c-a5cb-1fe8f0cee796">Microsoft&#x27;s MAI-2 Base scores near GPT-5.6 Sol on perplexity</a></li>

</ul>
</details>

**标签**: `#perplexity`, `#large language models`, `#evaluation`, `#intelligence`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [奥莱利：硅谷与机制设计](https://www.oreilly.com/radar/what-happened-to-silicon-valley/) ⭐️ 7.0/10

对科技行业和 AI 从业者而言，蒂姆·奥莱利在《What Happened to Silicon Valley?》一文中提出，硅谷的演变反映的是资本主义作为优化引擎的运作方式，而非单纯的技术进步或市场失灵。他主张用机制设计——即逆向博弈论——来重新定义游戏规则，把目标从股东价值转向人类繁荣。文章是分析性评论，不是新闻事件或技术发布，未提供具体数据或可执行方案。

hackernews · greenyouse · 11月22日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50602947)

**「背景」** Tim O&\#x27;Reilly 在文中将机制设计描述为逆向博弈论：不是追问当前游戏的规则，而是追问“我们应该玩什么游戏”。这一概念构成了他将资本主义重新导向人类繁荣这一主张的基础。

**「社区讨论」** 评论中，Animats 和 michalsustr 赞同奥莱利的核心论点，认为应重新设计机制以人类繁荣为目标；CoolestBeans 则补充更直接的原因——零利率时代让科技公司过度扩张，如今利率回升后它们正借 AI 蚕食自身核心业务。这些是评论者观点，并非文章已证实的事实。

**标签**: `#Silicon Valley`, `#mechanism design`, `#capitalism`, `#AI`, `#tech industry`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [不确定时，不妨乱试](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 7.0/10

rss · Sean Goedecke · 11月23日 00:00

**「背景」** 在缺乏明确指引、看不清方向的局面下，作者认为最有效的做法往往是主动尝试多种方案——即“乱试”。这听起来反直觉，且确实有风险：乱试不当会损害技术人的声誉。

**「方案」** 作者给出三条原则：多尝试不同做法，以便接触更多现实；密切关注反馈，因为多数计划会失败；无情放弃没有正面反馈的方案，避免过度投入。他区分了三种乱试：产品上，在未找到产品市场契合时，围绕核心想法试探边缘，例如他在 GitHub Models 时做的许多集成并不成功，但让 AI 推理通过 GitHub Actions token 运行的那一个却意外成为“Continuous AI”的种子；工程上，面对过于复杂或已优化的系统，与其通读全貌，不如做一批推测性改动并快速评估；组织上，当团队间失联或士气低落时，主动尝试自动化、接手任务、提出长期计划，多数无效，但至少表明在努力。作者提醒，组织乱试中最需敏锐反馈，及时止损能建立信任，忽视反馈则会招致怨气。

**「启示」** 作者认为，乱试之所以叫“乱试”，是因为从内部看它确实像反复失败，但这种不适感是正常且必须忽略的。只要保持对反馈敏感并果断放弃失败方案，乱试就是应对不确定性的最快路径，也是许多工程与组织问题的有效解法。

**标签**: `#software engineering`, `#experimentation`, `#uncertainty`, `#organizational dynamics`, `#product development`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美股 AI 科技股遭抛售，亚洲多地紧急稳定市场](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

美国 AI 科技股周五遭遇大规模抛售，纳斯达克单日下跌 5.28%，费城半导体指数重挫近 11%。中国内地、韩国及中国台湾地区随即出台紧急措施稳定市场，包括下调融资保证金比例、放宽回购限制及禁止平盘以下卖空。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 恐慌情绪从美股蔓延至亚洲市场，多地监管机构紧急出台措施，以稳定投资者信心。

**「影响」** 新规直接影响相关市场的投资者和上市公司：中国内地融资交易门槛降低，韩国企业回购限制放宽，中国台湾地区卖空操作明显收紧。

**标签**: `#US tech stocks`, `#Nasdaq`, `#market selloff`, `#Asian markets`, `#policy response`

---

<a id="item-finance-news-2"></a>
### [蚂蚁集团领投具身智能公司 Simplexity Robotics 1 亿美元](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

据彭博报道，蚂蚁集团领投中国具身智能公司 Simplexity Robotics 1 亿美元 pre-A 轮融资，投后估值 16 亿美元，老股东阿里巴巴、腾讯、红杉中国和蓝驰创投跟投。

telegram · zaihuapd · 11月23日 02:02

**「背景」** 公司 2025 年 7 月成立于杭州，核心团队来自理想汽车；今年 3 月曾披露成立半年内完成五轮融资、累计 20 亿元人民币，当时投后估值已超 10 亿美元。彭博称中国人形机器人产业占全球出货量约 97%。

**「影响」** 这笔资金将用于与宇树、优必选等更成熟厂商争夺市场。

**标签**: `#venture capital`, `#humanoid robotics`, `#Ant Group`, `#China tech`, `#private equity`

---