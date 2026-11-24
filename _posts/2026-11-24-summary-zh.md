---
layout: default
title: "Horizon Summary: 2026-11-24 (ZH)"
date: 2026-11-24
lang: zh
---

> 从 38 条内容中筛选出 15 条重要资讯。

---

**科技新闻**
1. [Nvidia 董事会重新任命黄仁勋为 CEO](#item-tech-news-1) ⭐️ 8.0/10
2. [Ladybird 浏览器引擎发布首个 Alpha 版本](#item-tech-news-2) ⭐️ 8.0/10
3. [GLM-5.4 发布：智谱首款循环 Transformer 编码模型](#item-tech-news-3) ⭐️ 8.0/10
4. [ARM 文档站因商标与知识产权要求将于 2026 年 12 月 4 日关闭](#item-tech-news-4) ⭐️ 7.0/10
5. [NariQ：3-bit 量化 Qwen3.8-27B 声称近 BF16 性能](#item-tech-news-5) ⭐️ 7.0/10
6. [Codex2api 供应链投毒：后门版本 3.1.10–3.1.12 需回滚](#item-tech-news-6) ⭐️ 7.0/10
7. [黎曼猜想 AI 证明被指空转，作者承认代码满是垃圾](#item-tech-news-7) ⭐️ 7.0/10
8. [神舟二十四号 25 日发射，乘组首含巴基斯坦航天员](#item-tech-news-8) ⭐️ 7.0/10

**科技博客**
1. [ERNIE 5.5 Flash 的 vLLM Day-0 支持：插件部署与推理加速](#item-tech-blog-1) ⭐️ 7.0/10

**财经新闻**
1. [美联储威廉姆斯：利率或需进一步上调以抑制通胀](#item-finance-news-1) ⭐️ 7.0/10
2. [Anthropic 创纪录 IPO 引发 AI 股抛售，中国科技股蒸发 1.7 万亿美元](#item-finance-news-2) ⭐️ 7.0/10
3. [上海地铁票价时隔 21 年首次调整，12 月 1 日起实施](#item-finance-news-3) ⭐️ 7.0/10
4. [SpaceX 出租算力给 Anthropic 和 Google，月入数十亿美元](#item-finance-news-4) ⭐️ 7.0/10
5. [4.5 万家企业联名致信欧盟，要求对苹果 iPhone 浏览器限制立案](#item-finance-news-5) ⭐️ 7.0/10
6. [新加坡总理：不允许成为规避美国芯片管制的通道](#item-finance-news-6) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Nvidia 董事会重新任命黄仁勋为 CEO](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 8.0/10

Nvidia 董事会已重新任命黄仁勋（Jensen Huang）为 CEO，此前他刚被短暂免职。董事会声明称，在做出决定过程中收到了美国政府高级官员的意见，并基于这些意见确信黄仁勋的复职不构成国家安全风险。这一决定结束了围绕公司治理和 AI 芯片出口政策的一场快速动荡。

hackernews · jaz · 11月23日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50611576)

**「背景」** 此前，英伟达董事会曾短暂罢免黄仁勋的 CEO 职务，随后在不到两周内全票通过恢复其职务。据社区讨论中的观察，董事会做出罢免决定后迅速转向，且美国司法部表示不会就相关事项起诉；董事会最终依据美国政府高层提供的国家安全风险评估做出恢复决定。

**「对企业的实际影响」** 尽管黄仁勋复职可能缓解对 Nvidia 领导层的短期担忧，但企业客户仍应继续将替代方案纳入其 AI 基础设施战略，以降低对单一供应商的依赖。

**「社区讨论」** 评论中，有用户认为董事会声明中“收到美国政府高层意见”是最关键的部分；也有用户指出，董事会一致同意复职的决定与之前的迅速罢免形成鲜明对比，并援引特拉华州 Caremark 判例讨论董事责任。另有用户将此事与 2023 年 OpenAI 罢免 Altman 事件类比，认为公司名义治理结构未必是实际治理结构；还有用户认为目前没有证据表明存在犯罪行为，情报机构对相关指控持不确定态度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.yahoo.com/markets/stocks/live/nvidia-live-updates-jensen-huang-reinstated-as-ceo-trump-says-no-reason-to-believe-huang-a-national-security-risk-152429808.html">Nvidia live updates: Jensen Huang reinstated as CEO; Trump says...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#AI chips`, `#semiconductors`

---

<a id="item-tech-news-2"></a>
### [Ladybird 浏览器引擎发布首个 Alpha 版本](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird 于 2026 年 11 月 23 日发布首个 Alpha 版本，用户现可在 macOS 或 Linux 上直接安装，无需自行编译。该浏览器从零实现 HTML 解析、CSS 引擎、布局、JavaScript 和 WebAssembly，仅依赖 HarfBuzz、Skia、ffmpeg 和 SQLite 等外部组件。作者实测多数网站可正常渲染，包括运行 ffmpeg 和 Python 的 WebAssembly 应用，但 Datasette Lite 因 service worker 的 \`navigator.serviceWorker.startMessages\` 未实现而报错，已提交 issue \#15515。官方提醒这是 Alpha 版本，部分网站可能无法工作且偶尔会崩溃，并鼓励用户报告问题。

hackernews · janvdberg · 11月23日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50614249)

**「背景」** Ladybird 源自 SerenityOS 项目，目标是完全从零构建浏览器。2026 年 2 月，项目宣布采用 Rust 并借助 AI 编码代理，在两周内将 LibJS JavaScript 引擎的 2.5 万行 C++ 代码移植为 Rust。同年 10 月，项目在 web-platform-tests 套件中新增 75,650 个通过子测试，超过 Safari，其中大部分进展集中在 10 月 22 日至 27 日的五天，由 AI 编码代理完成。

**「影响」** 用户现在可以在 macOS 或 Linux 上直接安装体验，但需注意这是 Alpha 版本：部分网站无法工作、偶尔崩溃，且依赖 service worker 的应用（如 Datasette Lite）目前不兼容。

**「社区讨论」** 多位用户报告实测体验良好，包括复杂新闻网站和 ProxMox 的 NoVNC 界面，仅提到滚动略有迟滞；也有用户建议 Ladybird 应认真对待指纹识别防护，提供返回随机化值的非合规 JavaScript 模式。

**标签**: `#browser`, `#open source`, `#software engineering`, `#alpha release`, `#web standards`

---

<a id="item-tech-news-3"></a>
### [GLM-5.4 发布：智谱首款循环 Transformer 编码模型](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

智谱 AI 发布 GLM-5.4，这是其首个采用循环 Transformer（Loop Transformer）架构的模型：一组权重共享的层会在每次前向传播中迭代运行多次，从而在不增加参数量的前提下加深网络。该模型目前未开放权重，且无法通过常规 API 访问，需订阅 Coding Plan 才能通过 OpenAI 兼容的 Responses API（https://api.z.ai/api/v1）使用。Simon Willison 的鹈鹕绘图测试显示，5.4 与 5.3 的生成风格相近，均与 OpenAI/Anthropic 模型更接近，而 5.1 和 5.2 风格差异显著。这是继 Thinking Machines Lab 的 Inkling 2 Mini（11 月 20 日发布，中间层每 token 运行三次）之后，一周内第二款采用循环 Transformer 的模型。

hackernews · foohis · 11月23日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50609685)

**「背景」** 循环变压器（Loop Transformer）是一种让一组权重共享的层在每次前向传播中迭代运行多次的架构，从而在不增加参数量的前提下加深网络。此前一周，Thinking Machines Lab 于 11 月 20 日发布的 Inkling 2 Mini 已采用类似设计，GLM-5.4 是 Z.ai 首次引入该架构的模型。

**「GLM-5.4 仅限 Coding Plan 访问，循环 Transformer 提升推理深度但增加延迟」** 对 Z.ai API 开发者而言，GLM-5.4 目前只能通过 Coding Plan 订阅访问，常规 API 无法调用，且模型未开放权重；其循环 Transformer 架构通过将 28 层权重共享块运行两次，使 750B 参数模型声称达到 2T–3T 参数模型的推理深度，但社区反馈指出其“马拉松式思考”会显著拉长简单任务的完成时间。

**「社区讨论」** 评论中，aurareturn 解释了循环 Transformer 的动机：推理时每层权重需从 HBM 移入芯片，内存带宽是主要瓶颈，循环结构可优化这一开销；HarHarVeryFunny 则赞赏智谱公开技术细节的做法，并认为循环 Transformer 是明显方向，尽管仍有问题待解决。但 lnenad 报告了实际使用中的困扰：中国模型常出现“马拉松式思考”，即使简单任务也会反复自我怀疑，完成时间显著高于前沿模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.z.ai/guides/llm/glm-5.4">GLM - 5 . 4 - Overview - Z. AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://anyrouter.dev/model/z-ai/glm-5.4">GLM - 5 . 4 · Zhipu AI · pricing &amp; API · AnyRouter</a></li>
<li><a href="https://www.youtube.com/watch?v=G6-3js4jjTo">GLM - 5 . 4 Beat Opus 5.5? - YouTube</a></li>

</ul>
</details>

**标签**: `#GLM-5.4`, `#loop transformer`, `#Zhipu AI`, `#LLM architecture`, `#coding`

---

<a id="item-tech-news-4"></a>
### [ARM 文档站因商标与知识产权要求将于 2026 年 12 月 4 日关闭](https://arm.jonpalmisc.com/) ⭐️ 7.0/10

ARM 架构文档站 arm.jonpalmisc.com 应 Arm 公司要求，将于 2026 年 12 月 4 日停止运营。站主 jonpalmisc 表示，Arm 以使用其商标和知识产权为由要求移除该站托管的 ARM 文档，并称在保持站点实用性的同时规避这一要求似乎很难。目前站主正在考虑镜像托管、法律途径或发布去除 Arm 知识产权后的源码供个人使用等方案。

hackernews · tech234a · 11月23日 19:17 · [社区讨论](https://news.ycombinator.com/item?id=50617499)

**「背景」** Jon&\#x27;s Arm Reference 是一个社区维护的 AArch64 指令与系统寄存器参考站点，基于 Arm 公开文档整理而成。Arm 的法律团队以商标和知识产权为由要求其下架，站点宣布将于 2026 年 12 月 4 日关闭。

**「影响」** 依赖该站点查阅 ARM 文档的开发者将在 2026 年 12 月 4 日后失去这一资源；站主正在评估镜像托管和发布去知识产权化源码等替代方案，但截至发稿尚无确定结果。

**「社区讨论」** 评论者就 Arm 要求下架的法律依据展开争论：有用户指出 Arm 官方机器可读规范（MRAS）采用 BSD 风格许可证，质疑商标与知识产权主张的合理性；也有用户认为此举只会让为 Arm 创造价值的人更难工作，并建议法务应向工程师汇报。另有用户注意到该站与斯坦福大学托管的 arm64 文档高度相似，推测两者可能使用同一转换工具生成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arm.jonpalmisc.com/">Jon&#x27;s Arm Reference</a></li>
<li><a href="https://news.lavx.hu/article/jon-s-arm-reference-to-shut-down-dec-4-after-arm-legal-request">Jon&#x27;s Arm Reference to Shut Down Dec. 4 After Arm Legal ...</a></li>

</ul>
</details>

**标签**: `#ARM`, `#documentation`, `#trademark`, `#legal`, `#developer resources`

---

<a id="item-tech-news-5"></a>
### [NariQ：3-bit 量化 Qwen3.8-27B 声称近 BF16 性能](https://huggingface.co/nari-labs/Qwen3.8-27B-NariQ-GGUF) ⭐️ 7.0/10

NariQ 是面向 Qwen3.8-27B 的新型量化方法，提供 3-bit、2.5-bit 和 2-bit 权重文件，标题称 3-bit 版本约 10 GB。据模型卡，3-bit 版本在 DeepSWE 上得 41.0（BF16 为 39.8）、Terminal-Bench 2.1 上得 63.8（BF16 为 62.6）、AIME 25+26 上得 98.3（BF16 为 97.7），声称在长程智能体、数学、多语言和图像理解任务上接近 BF16 水平；2-bit 版本则明显下降（DeepSWE 28.6、Terminal-Bench 52.4、AIME 86.0）。这些结果来自 Nari 自己的基准测试，需使用其 llama.cpp 分支（nari-llama.cpp）才能运行；社区用户指出部分性能增益可能来自评测框架差异而非模型本身。

hackernews · toebee · 11月23日 13:42 · [社区讨论](https://news.ycombinator.com/item?id=50611402)

**「背景」** 量化通过降低模型权重的位宽来压缩体积并加速推理，但通常伴随质量损失；Qwen3.8-27B 是 27B 参数模型，此前 3-bit 或更低量化在长程智能体任务上难以保持 BF16 水平。NariQ 声称首次做到这一点。

**「影响」** 运行这些量化文件需要 Nari 的 llama.cpp 分支；社区用户 jedbrooke 报告称在 Apple M3 Pro（18 GB）上 3.0bpw 文件解码约 3.8 tok/s，远低于 CUDA，且 16GB Mac 能否运行尚未测试。

**「社区讨论」** 社区讨论中，用户 WithinReason 认为从图表看大部分性能提升来自评测框架差异而非模型本身；rao-v 虽认可项目做了多类长程任务和&\#x27;held out&\#x27;检查，仍担心高计算量 QAT 风格量化在真实使用中达不到基准声称的效果。

**标签**: `#quantization`, `#LLM`, `#Qwen`, `#agentic AI`, `#model compression`

---

<a id="item-tech-news-6"></a>
### [Codex2api 供应链投毒：后门版本 3.1.10–3.1.12 需回滚](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 7.0/10

Codex2api 作者账号被攻击者控制，攻击者绕过 main 分支直接推送 tag，使 Release 构建出带后门的版本 v3.1.10–3.1.12。其中 v3.1.11 移除了鉴权，导致无密码远程命令执行；同时一个 workflow 将仓库的 16 个 GitHub Actions secrets 外传，波及同账号下至少 21 个仓库。已安装或更新到这些版本的用户应立即停用、回滚到 3.1.9，并轮换 GitHub token、SSH key、数据库和 DeepSeek 等所有相关密钥。

telegram · zaihuapd · 11月23日 11:21

**「背景」** GitHub Actions workflow 是 CI/CD 供应链攻击的常见目标；2026 年 10 月以来的 GhostAction 活动已利用伪造的 workflow 文件入侵至少 772 个公共仓库，窃取 CI/CD 凭据。此次 Codex2api 事件中，攻击者同样通过 workflow 外传 Actions secrets，属于同一类攻击手法的延续。

**「影响与应对」** 受影响用户必须立即采取行动：停用当前版本、回滚到 3.1.9，并全面轮换所有可能泄露的凭据，包括 GitHub token、SSH key、数据库密码和 DeepSeek API 密钥，否则攻击者可能利用已获取的 secrets 持续访问相关仓库和外部服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/ghostaction-supply-chain-campaign/">GhostAction Supply Chain Campaign Uses Malicious GitHub ...</a></li>
<li><a href="https://aviatrix.ai/threat-research-center/ghostaction-github-actions-credential-theft-2026/">GhostAction GitHub Actions Supply Chain Attack Analysis 2026</a></li>

</ul>
</details>

**标签**: `#supply-chain-attack`, `#security`, `#codex2api`, `#github-actions`, `#incident-response`

---

<a id="item-tech-news-7"></a>
### [黎曼猜想 AI 证明被指空转，作者承认代码满是垃圾](https://x.com/i/web/status/2124987173439209561) ⭐️ 7.0/10

Alpöge 与 Claude 宣称的黎曼猜想及广义版本 Lean 证明被证实为空转：研究者指出关键定义被写成恒真式、几何条件形同虚设，且 17.5 万个文件、1700 万行代码中并无人类可读的证明。11 月 23 日，Alpöge 承认「25 万页是玩笑」、代码「满是垃圾但能编译」，并称批评完全合理。此前 Lean 与 Mathlib 社区曾表示对代码证明了该命题「有充分信心」，但这一判断未能经受住后续审查。

telegram · zaihuapd · 11月24日 01:29

**「背景」** 黎曼猜想是数论中一个长期未解决的重大开放问题。2026 年 11 月，数学家 Levent Alpöge 宣布与 AI 系统 Claude 合作发现了该猜想的证明，并以约 1700 万行 Lean 形式化代码的形式公开，但未提供人类可读的证明。这一背景解释了为何后续对代码的审查成为关键：形式化验证依赖机器检查，而社区最初对代码证明命题的“充分信心”建立在代码可编译的基础上。

**「影响」** 对依赖 AI 生成形式化证明的研究者和机构而言，这一事件表明：通过 Lean 内核检查并不能保证证明有意义。关键定义被写成恒真、几何条件形同虚设，说明即使代码能编译，形式化陈述本身也可能与原始命题脱节。因此，人工审查的重点应从“证明是否通过内核”转向“形式化陈述是否忠实于原意”，否则可能接受一个空洞的证明。

**「社区讨论」** 用户 levent 评论称「证明结果是真的，只是代码满是垃圾」，将结论真实性与其代码质量分开看待；该观点与 Alpöge 本人的承认形成对照，但未提供独立证据支持结论为真。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Riemann_hypothesis">Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://math.uwaterloo.ca/~mrubinst/alpoge_claude_grh/zeta-paper.pdf">The Alpoge - Claude proof of the Riemann hypothesis explained for...</a></li>
<li><a href="https://www.cryptopolitan.com/alpoge-claude-riemann-hypothesis-proof/">Anthropic&#x27;s Alpöge says Claude helped him prove the Riemann ...</a></li>
<li><a href="https://mathoverflow.net/questions/513540/should-we-trust-ai-generated-formal-proofs-in-lean-4">Should we trust AI-generated formal proofs in Lean 4?</a></li>
<li><a href="https://aitechmodel.com/ai-generated-lean-certified-math-proofs-the-risks-analysts-and-engineers-are-tracking/">AI-Generated Lean-Certified Math Proofs: The Risks Analysts ...</a></li>
<li><a href="https://gridthegrey.com/posts/openai-lean-proof-mistranslation-exposes-ai-verification-risk/">OpenAI Lean Proof Mistranslation Exposes AI Verification Risk</a></li>

</ul>
</details>

**标签**: `#AI proof`, `#Lean`, `#formal verification`, `#Riemann Hypothesis`, `#mathematics`

---

<a id="item-tech-news-8"></a>
### [神舟二十四号 25 日发射，乘组首含巴基斯坦航天员](https://www.news.cn/20261124/3b116eb35c404cd7b897b23a50099b5b/c.html) ⭐️ 7.0/10

神舟二十四号定于 11 月 25 日 8 时 18 分发射，乘组由指令长汤洪波、武毅和巴基斯坦航天员穆罕默德·齐尚·阿里组成，这是中国载人航天工程首个含外籍航天员的乘组。飞船将采用 3.5 小时自主快速交会对接，对接天和核心舱前向端口。阿里将成为首位到访“天宫”的外籍航天员，之后将随神舟二十三号返回。

telegram · zaihuapd · 11月24日 04:08

**「背景」** 神舟飞船系列任务承担天宫空间站的乘组轮换，此前历次乘组均由中方航天员组成。此次任务首次纳入外籍航天员，是中国载人航天工程国际合作的新进展。

**「影响」** 巴基斯坦成为首个有航天员进入天宫空间站的国家。阿里将随神舟二十三号返回，其跨乘组驻留安排为后续国际航天员参与中国空间站任务提供了操作参考。

**标签**: `#spaceflight`, `#aerospace`, `#China space program`, `#international cooperation`, `#Tiangong`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [ERNIE 5.5 Flash 的 vLLM Day-0 支持：插件部署与推理加速](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 7.0/10

rss · vLLM Blog · 11月24日 00:00

**「背景」** ERNIE 5.5 Flash Preview 是 280B 总参数、每 token 激活 14B 的稀疏 MoE 模型，支持 1M 上下文、思考与工具调用。百度 ERNIE 团队与 vLLM 合作，在发布当天通过独立插件 vLLM-ERNIE 提供支持，无需 fork 或等待 nightly 构建。

**「方案」** 模型从设计之初就以推理成本为目标，重构了注意力、MoE 与输出头：37 层用 HCA、6 层用 MLA-DSA，并引入低秩注意力门、Multi-Router Latent MoE、mHC 残差流与 MultiMax 输出头。针对这些新结构，团队设计了专用融合内核，将可预计算部分在加载时折叠进权重；融合内核比朴素实现快 1.55× 到 6.53×，部分结果与逐算子实现逐位一致。FlashIndexer 通过动态头路由与阈值预过滤降低稀疏索引开销，在 1M 上下文下带来 1.4× 加速。默认检查点将路由专家存为 MXFP4（W4A8 QAT），其余权重与 KV 缓存为 FP8。DSpark 草稿模型经中训、后训与在线策略蒸馏的多阶段训练，在真实编码与 Agent 负载上平均接受长度超过 4.0。插件通过 vllm.general\_plugins 入口点注册，仅在模型配置指定架构时才导入模型代码，因此不影响同环境中的其他模型。

**「启示」** 插件模式让模型按自身节奏发布修复与特性，同时复用 vLLM 核心的调度、并行与连接器能力；推理优先的架构设计与融合内核，为大型 MoE 模型的高效部署提供了可迁移的工程经验。

**标签**: `#vLLM plugin`, `#MoE inference`, `#kernel fusion`, `#quantization-aware training`, `#speculative decoding`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美联储威廉姆斯：利率或需进一步上调以抑制通胀](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

纽约联储主席约翰·威廉姆斯表示，为将通胀降至 2%目标，美联储“必须随着时间的推移采取行动”，市场已完全定价 12 月 8-9 日 FOMC 会议加息 25 个基点，当前联邦基金利率目标区间为 3.75%-4%。

rss · CNBC Finance · 11月23日 21:02

**「背景」** 威廉姆斯预计通胀将在 2027 年明显回落、2028 年达到目标；他未直接评论 12 月会议预期，而是援引 10 月 FOMC 声明称将依据“更多信息”决定政策路径，并将当前通胀压力归因于伊朗冲突、AI 建设需求和关税。

**「影响」** 若 12 月加息落地，将直接提高美国企业和家庭的借贷成本，影响抵押贷款、信用卡及企业融资利率。

**标签**: `#Federal Reserve`, `#Monetary Policy`, `#Inflation`, `#Interest Rates`, `#John Williams`

---

<a id="item-finance-news-2"></a>
### [Anthropic 创纪录 IPO 引发 AI 股抛售，中国科技股蒸发 1.7 万亿美元](https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo) ⭐️ 7.0/10

Anthropic 创纪录的 1195 亿美元 IPO 引发全球 AI 股抛售，中国科技股自 6 月底以来市值累计蒸发 1.7 万亿美元，DeepSeek、月之暗面、阶跃星辰的上市计划因此蒙上阴影。

telegram · zaihuapd · 11月23日 09:31

**「背景」** Anthropic 首日上涨 17%、市值达 1.8 万亿美元，次日即下跌 8.5%；智谱自 6 月高点跌超 85%，此前半年曾涨 2000%，MiniMax 本月跌破发行价。

**「影响」** 正在筹备或考虑上市的 DeepSeek、月之暗面、阶跃星辰等中国 AI 公司可能面临估值下调和发行窗口收窄的压力。

**标签**: `#AI stocks`, `#IPO`, `#market selloff`, `#Chinese tech`, `#Anthropic`

---

<a id="item-finance-news-3"></a>
### [上海地铁票价时隔 21 年首次调整，12 月 1 日起实施](https://weibo.com/1699432410/5368461393397183) ⭐️ 7.0/10

上海地铁票价时隔 21 年首次调整，12 月 1 日起实施：起乘价 3 元，可乘 0-4 公里，之后按里程分段加价，50 公里以上每 15 公里加 1 元；同时推出 35 次、45 次、60 次、90 次四档计次票，定价 190 元、210 元、270 元、390 元，11 月 26 日开售，同一支付渠道当月累计满 90 元后享 9 折。

telegram · zaihuapd · 11月23日 10:45

**「背景」** 这是上海地铁票价 21 年来首次调整，此前票价结构长期未变；本次调价在改为按里程计价的同时，同步推出计次票和满额优惠，以缓解对高频通勤人群的影响。

**「影响」** 新票价和优惠主要影响上海高频通勤的地铁乘客，计次票和满额折扣旨在减少调价对这部分人群的影响。

**标签**: `#Shanghai`, `#subway fare`, `#public transport`, `#cost of living`, `#policy`

---

<a id="item-finance-news-4"></a>
### [SpaceX 出租算力给 Anthropic 和 Google，月入数十亿美元](https://www.nytimes.com/2026/11/23/business/elon-musk-ai-anthropic-google.html) ⭐️ 7.0/10

据《纽约时报》11 月 23 日报道，SpaceX 自今年 5 月起向 Anthropic、Google 等公司出租数据中心算力，月入数十亿美元。三名知情人士称，马斯克向员工表示 SpaceX 在 AI 上落后，出租算力比自用更赚钱。

telegram · zaihuapd · 11月24日 02:06

**「背景」** SpaceX 此前为自研 AI 在密西西比州绍萨文等地建设数据中心，但马斯克承认其 AI 能力落后，转而将算力出租给 Anthropic、Google 等竞争对手；据《纽约时报》援引三名知情人士，出租比自用更赚钱。

**「影响」** 对谷歌而言，这笔每月约 9.2 亿美元、为期 33 个月的租约（约 11 万块英伟达 GPU）是其 Gemini Enterprise 需求激增下的临时扩容；对 SpaceX 而言，算力租赁成为新的经常性收入来源，使其从航天公司转向 AI 基础设施供应商。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/23/business/elon-musk-ai-anthropic-google.html">Elon Musk Faces an A . I . Dilemma at SpaceX - The New York Times</a></li>
<li><a href="https://www.linkedin.com/posts/abhinav-pabba-b383312a0_ai-genai-agenticai-activity-7469101321921634305-Arq6">Google pays SpaceX $920M/month for GPU access | LinkedIn</a></li>
<li><a href="https://theagenttimes.com/articles/google-commits-920-million-monthly-to-rent-spacex-gpu-capaci-0e9b00b9">Google Commits $920 Million Monthly to Rent SpaceX GPU Capacity...</a></li>
<li><a href="https://getaibook.com/news/gemini-enterprise-demand-drives-30b-spacex-gpu-contract/">Gemini Enterprise Demand Drives $30B SpaceX GPU Contract | News</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#AI compute`, `#Elon Musk`, `#Anthropic`, `#Google`

---

<a id="item-finance-news-5"></a>
### [4.5 万家企业联名致信欧盟，要求对苹果 iPhone 浏览器限制立案](https://appleinsider.com/articles/26/11/23/eu-urges-to-challenge-apples-grip-on-iphone-browsers?utm_source=rss) ⭐️ 7.0/10

包括 Mozilla 和 Shopify 在内的企业及民间组织联名致信欧盟委员会，要求对苹果 iPhone 浏览器限制立案，署名方合计代表约 4.5 万至 5.5 万家欧盟企业组织。联名方测算，若半数原生 iOS 应用转 Web，欧盟企业每年可省 110 亿欧元开发成本和 13 亿欧元 App Store 费用。

telegram · zaihuapd · 11月24日 03:02

**「背景」** 《数字市场法》生效后，苹果在欧盟允许第三方浏览器使用自有引擎，但附加条件使 Mozilla 等厂商难以把现有用户迁出 WebKit；iPhone 上所有浏览器仍须运行苹果 WebKit 引擎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.mozilla.org/en/mozilla/internet-policy/apple-ios-browser-engine-rules/">Why there are still no non-WebKit browsers on iOS | The ...</a></li>
<li><a href="https://apple.gadgethacks.com/news/ios-browser-performance-webkit-rules-what-apples-engine-requirement-actually-means/">iOS Browser Performance WebKit Rules: What Apple&#x27;s Engine ...</a></li>

</ul>
</details>

**标签**: `#EU regulation`, `#Apple`, `#Digital Markets Act`, `#Tech policy`, `#App economy`

---

<a id="item-finance-news-6"></a>
### [新加坡总理：不允许成为规避美国芯片管制的通道](https://www.bloomberg.com/news/articles/2026-11-24/singapore-won-t-be-conduit-to-skirt-us-chip-curbs-wong-says) ⭐️ 7.0/10

新加坡总理黄循财表示，新加坡不会成为企业规避美国芯片出口管制的通道，并正在调查 Megaspeed 采购英伟达芯片的交易。此前美国商务部已将 Megaspeed 等 7 家东南亚企业列入贸易黑名单，其中包括阿里巴巴新加坡子公司 Apex Enterprise Solutions。

telegram · zaihuapd · 11月24日 05:03

**「背景」** 此前一天，美国商务部已将新加坡企业 Megaspeed 及另外六家东南亚公司列入贸易黑名单，其中包括阿里巴巴新加坡子公司 Apex Enterprise Solutions；美方称这些企业存在向未获授权用户转移先进计算产品的重大风险，且 Megaspeed 与英伟达芯片疑似流入中国的调查有关。

**「影响」** 在新加坡及东南亚运营的半导体企业和数据中心面临更严格的合规审查。美国商务部已将新加坡和马来西亚列入需向中国关联企业出租 GPU 算力时申领许可证的名单，叠加新加坡政府明确承诺配合执行出口管制，当地涉及先进计算芯片交易的企业将面临更高的合规成本和被列入黑名单的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/business/us-blacklist-megaspeed-chip-firm-linked-nvidia-scandal-source-says-2026-11-23/">US blacklists Alibaba subsidiary and Megaspeed linked to ...</a></li>
<li><a href="https://www.straitstimes.com/world/united-states/us-blacklists-megaspeed-chip-firm-linked-to-nvidia-scandal">US blacklists Megaspeed, Alibaba unit amid Nvidia scandal ...</a></li>
<li><a href="https://hwbusters.com/news/ai-chip-export-controls-now-reach-rented-gpus-and-malaysia-and-singapore-need-a-license/">AI Chip Export Controls Now Reach Rented GPUs, and Malaysia and...</a></li>

</ul>
</details>

**标签**: `#export controls`, `#semiconductors`, `#Singapore`, `#US-China tech`, `#trade policy`

---