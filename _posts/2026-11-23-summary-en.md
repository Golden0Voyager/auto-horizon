---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 28 items, 5 important content pieces were selected

---

**Technology News**
1. [OpenAI argues perplexity is a simple, effective proxy for model intelligence](#item-tech-news-1) ⭐️ 8.0/10
2. [O&\#x27;Reilly: Silicon Valley&\#x27;s capitalism needs mechanism design for human flourishing](#item-tech-news-2) ⭐️ 7.0/10

**Technology Blog**
1. [When in doubt, flail about](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [US tech selloff triggers emergency measures in Asian markets](#item-finance-news-1) ⭐️ 8.0/10
2. [Ant Group Leads $100 Million Round in Humanoid Robot Startup Simplexity](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI argues perplexity is a simple, effective proxy for model intelligence](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI published a post arguing that perplexity—a model&\#x27;s average surprise when predicting the next token, ranging from 1 \(perfect prediction\) to vocabulary size \(random guessing\)—serves as a simple, effective proxy for model intelligence, with lower log-perplexity on a held-out evaluation set tracking stronger reasoning performance. The post presents a benchmark chart showing a clear downward trend across model generations, and Microsoft has joined the effort: Mustafa Suleyman reported MAI-2 Base&\#x27;s log-perplexity as 0.819 on OpenAI&\#x27;s evaluation set, with OpenAI&\#x27;s permission. The claim is a vendor argument rather than an independently measured result, and commenters note the trend persists even as models shift toward reinforcement learning.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**「Background」** Perplexity is a long-standing language-modeling metric: the exponentiated average cross-entropy loss on a held-out token sequence, where lower values mean the model assigns higher probability to the actual next tokens. OpenAI chief scientist Jakub Pachocki&\#x27;s November 22, 2026 post argues that this pretraining compression measure is a consistent proxy for the &\#x27;intelligence substrate&\#x27; behind models like ChatGPT and reasoning systems, and calls on frontier labs to report log-perplexity on a common held-out set for shared safety pacing. The community post and third-party analysis both frame the article as a proposal to standardize this metric across labs rather than a new benchmark release.

**「Shared benchmark adoption」** Microsoft has committed to reporting pre-training progress on OpenAI&\#x27;s shared held-out evaluation set, with MAI-2 Base scoring a log-perplexity of 0.819, directly comparable to GPT-5.6 Sol because both models use the same tokenizer. This gives developers and labs a common, simple metric for comparing base-model intelligence across vendors.

**「Community Discussion」** Commenter d\_burfoot argues the perplexity–intelligence correspondence is &quot;surprising at first, but in retrospect could not work any other way,&quot; because prediction \(compression\) rate on raw data is exactly the metric that captures progress in extracting world models—a point he made in a 2008 paper. Commenter jrflo says the clear trend is &quot;pretty shocking&quot; given the increasing use of reinforcement learning, and commenter tintor asks whether GPT 5 has higher perplexity than GPT 4.5, a question the supplied comments do not answer.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence - OpenAI</a></li>
<li><a href="https://community.openai.com/t/perplexity-and-intelligence/1419510">Perplexity and Intelligence - Community - OpenAI Developer ...</a></li>
<li><a href="https://www.explainx.ai/blog/openai-pachocki-perplexity-intelligence-pacing-safety-november-2026">OpenAI Perplexity Metric: GPT Log-Loss Curve (Nov 2026 ...</a></li>
<li><a href="https://x.com/mustafasuleyman/status/2124663594449318173">Mustafa Suleyman on X: &quot;We fully support OpenAI&#x27;s ...</a></li>
<li><a href="https://www.techtwitter.com/tweet/86327c55-7454-4d6c-a5cb-1fe8f0cee796">Microsoft&#x27;s MAI-2 Base scores near GPT-5.6 Sol on perplexity</a></li>

</ul>
</details>

**Tags**: `#perplexity`, `#large language models`, `#evaluation`, `#intelligence`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [O&\#x27;Reilly: Silicon Valley&\#x27;s capitalism needs mechanism design for human flourishing](https://www.oreilly.com/radar/what-happened-to-silicon-valley/) ⭐️ 7.0/10

In a long-form essay on O&\#x27;Reilly Radar, Tim O&\#x27;Reilly argues that Silicon Valley&\#x27;s evolution reflects capitalism as an optimization engine, and calls for mechanism design—reverse game theory—to reorient the system toward human flourishing rather than shareholder value. The piece frames the tech industry&\#x27;s trajectory as a product of the rules of the game, and asks what game ought to be played.

hackernews · greenyouse · Nov 22, 19:20 · [Discussion](https://news.ycombinator.com/item?id=50602947)

**「Background」** Mechanism design, also called reverse game theory, inverts the usual question: instead of asking what game we are currently playing, it asks what game we ought to be playing. Tim O&\#x27;Reilly applies this lens to Silicon Valley, treating capitalism as an optimization engine whose target is set by its rules rather than by any natural law. His essay argues that those rules can be redesigned so the system optimizes for human flourishing instead of shareholder value.

**「Community Discussion」** Commenters largely agree with O&\#x27;Reilly&\#x27;s framing: michalsustr highlights the mechanism design idea as the key takeaway, while Animats argues that governance is futile until we recognize the machine we have built and reprogram it for human flourishing. CoolestBeans offers a dissenting proximate cause, attributing the current situation to the ZIRP era that allowed tech companies to grow grotesquely, and notes that with higher interest rates they are now cannibalizing core competencies on AI.

**Tags**: `#Silicon Valley`, `#mechanism design`, `#capitalism`, `#AI`, `#tech industry`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [When in doubt, flail about](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 7.0/10

rss · Sean Goedecke · Nov 23, 00:00

**「Background」** In unclear situations—no clear guidance, no known fix—caution and waiting often fail. Sean Goedecke argues that deliberate experimentation, or &quot;flailing,&quot; is the fastest route to understanding, even though it feels risky and can damage your reputation if done badly.

**「Solution」** Flailing well means trying many different things, attending carefully to feedback, and ruthlessly dropping anything that isn&\#x27;t getting positive response. Trying many things is key: it maximizes contact with reality, increases the odds that one plan works, and prevents over-investment in doomed ideas. Goedecke identifies three types. Product flailing applies when a feature lacks product-market fit; on GitHub Models, most integrations failed, but one—running AI inference from a GitHub Actions token—stuck and seeded &quot;Continuous AI.&quot; Engineering flailing suits tangled, optimized, or huge systems where full analysis is impractical; he recommends speculative changes, dropping those that don&\#x27;t improve things, and digging into the ones that do. Organizational flailing, most relevant to senior engineers, means trying plausible interventions—automating manual work, volunteering, proposing long-term plans—when teams are misaligned or unhappy. Most won&\#x27;t help, but showing effort builds trust, and dropping failing plans quickly is critical. The name matters: it feels like flailing from the inside, but that feeling is a normal psychological barrier to push through, not a warning sign.

**「Takeaway」** When uncertainty blocks progress, deliberate, feedback-sensitive experimentation beats cautious waiting. The key is to treat the uncomfortable feeling of flailing as a positive signal and stay ready to abandon plans that aren&\#x27;t working.

**Tags**: `#software engineering`, `#experimentation`, `#uncertainty`, `#organizational dynamics`, `#product development`

---

## Financial News

<a id="item-finance-news-1"></a>
### [US tech selloff triggers emergency measures in Asian markets](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

US tech stocks suffered a severe selloff on Friday, with the Nasdaq falling 5.28% and the Philadelphia Semiconductor Index plunging nearly 11%, prompting China, South Korea, and Taiwan to announce emergency market stabilization measures.

telegram · zaihuapd · Nov 22, 13:24

**「Background」** The selloff in US AI-related tech stocks spread panic to Asian markets, leading authorities to intervene.

**「Impact」** Investors in the three markets face new trading rules: China lowered its margin financing ratio to 80%, South Korea relaxed daily buyback order limits for three months, and Taiwan banned short selling below the previous close and raised margin requirements.

**Tags**: `#US tech stocks`, `#Nasdaq`, `#market selloff`, `#Asian markets`, `#policy response`

---

<a id="item-finance-news-2"></a>
### [Ant Group Leads $100 Million Round in Humanoid Robot Startup Simplexity](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

Ant Group led a $100 million pre-A funding round in Simplexity Robotics, valuing the Chinese humanoid-robot startup at $1.6 billion post-money, chairman and co-founder Wang Kai told Bloomberg. Alibaba, Tencent, HongShan, and BlueRun Ventures also participated.

telegram · zaihuapd · Nov 23, 02:02

**「Background」** Simplexity, founded in Hangzhou in July 2025 by former Li Auto executives, had raised about 2 billion yuan across five rounds by March 2026; Bloomberg notes China accounts for about 97% of global humanoid-robot shipments.

**Tags**: `#venture capital`, `#humanoid robotics`, `#Ant Group`, `#China tech`, `#private equity`

---