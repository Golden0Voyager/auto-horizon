---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 35 条内容中筛选出 13 条重要资讯。

---

**科技新闻**
1. [矩阵乘法指数降至 9/4：算法理论重大突破](#item-tech-news-1) ⭐️ 8.0/10
2. [1Password 安全事件：员工 GitHub 账户被入侵](#item-tech-news-2) ⭐️ 8.0/10
3. [Anthropic 的 GRH Lean 证明压缩至约 7.6 万行](#item-tech-news-3) ⭐️ 8.0/10
4. [谷歌发布 Cogentic 论文，聚焦整数分解与离散对数](#item-tech-news-4) ⭐️ 8.0/10
5. [GDPx 基准：聚焦高经济影响领域的前沿模型评测](#item-tech-news-5) ⭐️ 8.0/10
6. [纽约时报警告摄影师勿更新 Photoshop 因 AI 功能](#item-tech-news-6) ⭐️ 7.0/10
7. [腾讯开源 Hy4 flash 量化权重，最小版可运行于 64GB Mac mini](#item-tech-news-7) ⭐️ 7.0/10
8. [Minecraft Java 版曝高危 RCE 漏洞，FreeType 字体越界写](#item-tech-news-8) ⭐️ 7.0/10
9. [三星与 SK 海力士将采用长江存储 Xtacking 堆叠技术](#item-tech-news-9) ⭐️ 7.0/10

**财经新闻**
1. [美商务部被曝施压英特尔交出 10%股权](#item-finance-news-1) ⭐️ 8.0/10
2. [美国拟对中国、欧盟等 14 个贸易伙伴加征新关税](#item-finance-news-2) ⭐️ 8.0/10
3. [英伟达行情波动考验美联储主席沃什的市场信号策略](#item-finance-news-3) ⭐️ 7.0/10
4. [黄仁勋重返英伟达，凸显美中 AI 人才竞争](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [矩阵乘法指数降至 9/4：算法理论重大突破](https://scottaaronson.blog/?p=10379) ⭐️ 8.0/10

斯科特·阿伦森（Scott Aaronson）的博客文章讨论了理论计算机科学的一项重大突破：矩阵乘法指数被证明为 9/4（即 2.25），这比此前已知的上界有显著改进。该结果意味着存在更快的矩阵乘法算法，对算法复杂度理论具有基础性意义。相关论文已在 Hacker News 上引发广泛讨论。

hackernews · Kotlopou · 11月25日 19:11 · [社区讨论](https://news.ycombinator.com/item?id=50646108)

**「背景」** 矩阵乘法指数 ω 是描述 n×n 矩阵乘法所需时间 O\(n^ω\) 的常数；该博客文章引用的论文标题宣称 ω ≤ 9/4（即 2.25）。若该上界成立，它将把矩阵乘法的渐近复杂度上界压低到 2.25，但源材料未提供证明细节。

**「影响」** 这一结果将矩阵乘法的理论复杂度上界降至 2.25，为算法复杂度理论提供了新的基础性结果。对于理论计算机科学研究者而言，这意味着矩阵乘法这一核心问题的复杂度有了新的上界，可直接用于后续算法分析和复杂度下界证明。

**「社区讨论」** 评论中，用户 utopiah 质疑这一突破是否真的归功于大语言模型，认为 Lean 和 MathLib 等形式化验证工具（分别始于 2013 年和 2017 年）早已为“数学大变革”奠定基础，大型企业只是恰好在此时补贴算力用于营销。这一观点与 jsLavaGoat 关于 AI 擅长公理化数学但未必能解决其他领域的看法形成对比，反映了社区对 AI 在数学发现中角色的分歧。

**标签**: `#matrix multiplication`, `#algorithms`, `#theoretical computer science`, `#AI`, `#mathematics`

---

<a id="item-tech-news-2"></a>
### [1Password 安全事件：员工 GitHub 账户被入侵](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password 于 11 月 19 日开始调查员工企业 GitHub 账户被入侵的迹象，攻击者借此访问源代码并向后台服务推送恶意代码，随后下载了部分客户账户信息，包括姓名、邮箱地址、账户标识及创建和最近登录时间。公司未披露受影响用户数量，但表示客户保险库及其内容未受影响。1Password 已停用涉事账户、轮换或撤销可能暴露的内部凭证，并加强邀请和恢复邮件验证码；用户无需更改账户，但应警惕钓鱼。

hackernews · lxhrstn · 11月25日 17:18 · [社区讨论](https://news.ycombinator.com/item?id=50644817)

**「背景」** 此次事件属于 SaaS 供应链攻击：攻击者先入侵员工企业 GitHub 账户，再借其访问源代码并向后台服务推送恶意代码。1Password 的客户保险库及内容未受影响，但攻击者仍获取了部分账户元数据。

**「影响」** 1Password 提醒用户无需更改账户，但应警惕钓鱼；社区用户已报告收到利用被窃邮箱地址制作的钓鱼邮件，伪装成保险库共享通知。

**「社区讨论」** 社区讨论聚焦于攻击路径：tptacek 认为员工笔记本被攻陷后向 GitHub 推送代码是 SaaS 公司最常见的攻击模式，但 1Password 的客户端加密缓解了最坏情况。ctidd 则质疑公告未说明是否缺少分支保护规则，认为“向后台服务推送恶意代码”是重大警示。

**标签**: `#security`, `#password-manager`, `#supply-chain`, `#SaaS`, `#incident`

---

<a id="item-tech-news-3"></a>
### [Anthropic 的 GRH Lean 证明压缩至约 7.6 万行](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

Anthropic 此前用 Lean 完成的广义黎曼假设（GRH）形式化证明，已被压缩至约 7.6 万行，较原 1700 万行减少 99.56%。新版本已发布在 GitHub 上，包含人类可读的文档，并明确区分已知数学与新增数学部分，便于数学家审阅。该压缩版可直接获取。

hackernews · nb-t · 11月25日 21:48 · [社区讨论](https://news.ycombinator.com/item?id=50648050)

**「背景」** 2026 年 11 月 20 日，Anthropic 数学家 Levent Alpöge 发布了黎曼猜想的 Lean 形式化证明，其原始归档包含约 175,187 个源文件和 239MB 数据，但该证明尚未得到专家确认（tool-2-1, tool-2-2, tool-2-3）。本次发布的版本将这一庞大形式化压缩至约 76k 行，并附有人类可读的文档，旨在解决 AI 生成证明难以理解的问题。

**「对数学界的影响」** 压缩后的证明将已知数学与新数学明确分开，并附有人类可读的文档，使数学家能够实际消化核心论证；这直接回应了陶哲轩关于 AI 生成证明难以阅读的担忧，但克莱奖的评审仍需数年时间。

**「社区讨论」** 评论者 gre 质疑这是否挑战了陶哲轩此前关于大型证明缺乏洞见的观点，并反问更聪明的语言模型是否已能压缩并解释证明；AIShill101 则希望数学家真正理解核心论证并写出正式论文、在会议上报告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Alp%C3%B6ge&#x27;s_proof_of_the_Riemann_hypothesis">Alpöge&#x27;s proof of the Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://interestingengineering.com/ai-robotics/anthropic-167-year-old-riemann-hypothesis-claude">Claude helped prove 167-year-old Riemann hypothesis , researcher...</a></li>
<li><a href="https://www.nacionale.com/en/articles/has-riemann-hypothesis-been-proved-levent-alpoge-claude-anthropic-claim-lean">Riemann hypothesis proof claimed with Claude, unverified</a></li>
<li><a href="https://www.newscientist.com/article/2583307-why-mathematician-terence-tao-thinks-ai-must-spark-a-rapid-revolution/">Why mathematician Terence Tao thinks AI must spark... | New Scientist</a></li>
<li><a href="https://www.nacionale.com/en/articles/when-will-we-know-riemann-hypothesis-proof-verified-alpoge-claude-lean-what-happens-next">Lean community certifies Riemann proof ; prize years off</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#Lean`, `#AI for mathematics`, `#proof compression`, `#Riemann hypothesis`

---

<a id="item-tech-news-4"></a>
### [谷歌发布 Cogentic 论文，聚焦整数分解与离散对数](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) ⭐️ 8.0/10

谷歌研究院发布了 Cogentic 系列论文，主题为整数分解和离散对数，这两类问题是密码学与算法数论的基础。目前公开信息有限，尚不能确认这些论文是否带来数学突破；社区讨论热烈，但结果仍需同行评审和独立验证。

hackernews · rgwohlbold · 11月25日 13:33 · [社区讨论](https://news.ycombinator.com/item?id=50642086)

**「背景」** 整数分解和离散对数是数论与密码学的基础难题，RSA 等公钥加密的安全性依赖于其计算难度。Google Research 发布的 Cogentic 论文声称在整数分解上取得了理论进展，但尚未经过外部数学家验证，也未表明能破解现代加密。

**「影响」** 对密码学领域而言，若这些论文中的算法确实有效，可能影响依赖整数分解和离散对数难解性的公钥密码方案；但当前仅为论文发布，尚无独立验证，具体影响尚不确定。

**「社区讨论」** Hacker News 评论中，有用户引用传闻称这可能只是更大进展的开端，但该说法未获证实；另有用户将近期数学进展类比 AlphaGo 对围棋搜索空间的探索，认为计算机科学正变得更有吸引力。这些是个人观点，不能作为事实依据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/google-research/google-research/tree/master/cogentic_research_papers">Google Releases Cogentic Papers on Integer Factorization ...</a></li>
<li><a href="https://www.rdworldonline.com/google-cogentic-ai-integer-factoring-bounds-lean-proofs/">Google’s Gemini 4 agent claims six math proofs in a day ...</a></li>

</ul>
</details>

**标签**: `#integer factorization`, `#discrete logarithms`, `#cryptography`, `#Google Research`, `#algorithmic number theory`

---

<a id="item-tech-news-5"></a>
### [GDPx 基准：聚焦高经济影响领域的前沿模型评测](https://newsletter.semianalysis.com/p/evaluating-recent-model-releases) ⭐️ 8.0/10

SemiAnalysis 于 11 月发布新基准 GDPx，聚焦芯片设计、网络安全、生物、金融、法律等 11 个高经济影响领域，与 14 家专业数据伙伴合作构建 206 项任务。与 GDPVal 和 Agent&\#x27;s Last Exam 按 GDP 占比或 O\*NET 分类选择领域不同，GDPx 刻意排除政府和房地产等行业，因为 AI 影响分布不均。发布日最高分模型 Opus 5.5 仅得 12%，远低于其他基准首日通常超 50%的得分，为未来模型区分留出巨大空间。自 11 月 1 日上线以来，Anthropic、OpenAI、Google（Gemini 4 系列）、阿里巴巴和月之暗面均发布新模型，GDPx 排行榜已更新。

rss · Semianalysis · 11月26日 00:05

**「背景」** 现有智能体基准多只测单一领域（如编程或法律），少数综合性基准如 GDPVal 和 Agent&\#x27;s Last Exam 按 GDP 占比或 O\*NET 职业分类选择领域，但 AI 影响并非均匀分布，导致领域选择失当。GDPx 因此转向高影响领域。

**「影响」** 对追踪前沿模型进展的开发者而言，GDPx 的低得分（Opus 5.5 仅 12%）意味着该基准能更好地区分未来模型发布，不像 Terminal Bench 4.0 等已饱和的基准。同时，Fable 5.2 和 GPT-6.2 Astra 因安全分类器在网络安全、生物和 alignment 领域触发而拉低总分，排除这些领域并改用部分评分后排行榜会变化，评估时需注意安全分类器的影响。

**标签**: `#AI benchmarking`, `#frontier models`, `#GDPx`, `#model evaluation`, `#agentic AI`

---

<a id="item-tech-news-6"></a>
### [纽约时报警告摄影师勿更新 Photoshop 因 AI 功能](https://www.theverge.com/ai-artificial-intelligence/1041227/the-new-york-times-warns-photographers-not-to-update-photoshop-over-ai-features) ⭐️ 7.0/10

《纽约时报》已告知其摄影师暂不要更新 Adobe Photoshop，理由是 Adobe 新增的 AI 功能可能危及新闻图片的真实性与可信度。这一内部指引属于媒体机构的政策决定，而非对某款已发布功能的独立测试结论；它反映出创意与媒体行业对 AI 编辑与 AI 生成难以区分的普遍担忧。目前尚不清楚该警告具体涉及哪些 Photoshop 版本或 AI 功能。

hackernews · rmason · 11月25日 21:18 · [社区讨论](https://news.ycombinator.com/item?id=50647673)

**「背景」** Adobe 近年来在 Photoshop 中持续集成生成式 AI 功能（如生成式填充、生成式扩展），这些功能通过“生成额度”计费使用。据俄罗斯媒体转述，纽约时报对摄影师的禁令从 Photoshop 2027 的 28.0.0 版本开始，并适用于该版本后续所有更新，反映出媒体机构对 AI 编辑痕迹难以与全 AI 生成内容区分的担忧。

**「对摄影师的影响」** 对为《纽约时报》供稿的自由摄影师而言，直接后果是必须继续使用旧版 Photoshop，不能升级到 2027 版（28.0.0），因为该版本新增的 AI 功能可能以用户不易察觉的方式使用 AI。政策中“目前”的措辞表明这一限制可能是暂时的，报社正在制定允许未来使用的指导方案。

**「社区讨论」** 一位自称在创意工具领域工作的人士指出，当最终产物是图像时，几乎无法区分“完全由 AI 生成”与“用 AI 做小幅调色、抠图或版式优化”，而社交平台上的“AI 生成内容”标签对权威品牌而言是公信力的致命打击。另有评论者提到，Tidal 上周也禁止了 AI 内容，显示这种污名化正在蔓延；这些是评论者的个人观察与职业经验，并非经核实的独立事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.adobe.com/products/photoshop.html">Official Adobe Photoshop | Free Trial and Online Photo &amp; Design App</a></li>
<li><a href="https://dzen.ru/a/aweGZ0k8xXcsyfG2">The New York Times потребовала обрабатывать... | Дзен</a></li>
<li><a href="https://www.dpreview.com/news/new-york-times-adobe-photoshop-2027-restriction-ai/">Photoshop’s latest AI features are generating some controversy</a></li>
<li><a href="https://petapixel.com/2026/11/24/new-york-times-prohibits-photographers-from-using-photoshop-2027/">New York Times Prohibits Photographers From Using Photoshop ...</a></li>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/1041227/the-new-york-times-warns-photographers-not-to-update-photoshop-over-ai-features">The New York Times warns photographers not to update ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#Photoshop`, `#Adobe`, `#New York Times`, `#creative tools`

---

<a id="item-tech-news-7"></a>
### [腾讯开源 Hy4 flash 量化权重，最小版可运行于 64GB Mac mini](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 7.0/10

腾讯混元通过大模型压缩加速工具箱 AngelSlim 开源了 224B 参数模型 Hy4 flash 的 GGUF 量化权重。原权重约 410.27 GiB，最小 IQ2-AH 版本降至 125.73 GiB（约为原版 30%），借助 Strata offload 框架可在 64 GB Mac mini 上运行。实测中，48 GB 显存设备在 10K 上下文下每秒生成 89 个 token，M5 Max 128 GB 上 Q3\_K 版本在 32K 上下文下每秒生成 47 个 token；在 DeepSWE v1.1 等评测中，Q3\_K 与原模型得分差距不超过 0.4 分。

telegram · zaihuapd · 11月25日 09:29

**「背景」** GGUF 量化通过降低权重精度来压缩模型体积，而 Strata offload 框架允许将部分层卸载到内存或存储，使大模型在有限内存设备上运行。AngelSlim 是腾讯用于模型压缩与加速的工具箱，此次开源即通过它生成 Hy4 flash 的量化权重。

**「影响」** 对于本地部署大模型的开发者，这一量化版本将 224B 级模型的硬件门槛降至 64 GB 内存的消费级设备，同时 Q3\_K 在 DeepSWE v1.1 等评测中与原模型差距不超过 0.4 分，表明量化对推理质量影响有限。用户可通过 AngelSlim 获取权重，并配合 Strata offload 框架在 Mac mini 等设备上运行。

**标签**: `#open-source`, `#quantization`, `#large language models`, `#inference`, `#Tencent`

---

<a id="item-tech-news-8"></a>
### [Minecraft Java 版曝高危 RCE 漏洞，FreeType 字体越界写](https://github.com/bikini/minecraft2shell) ⭐️ 7.0/10

11 月 22 日公开的 minecraft2shell 显示，服务器资源包中的特制 TrueType 字体可触发 FreeType 2.14.3 及更早版本的原生越界写，使 Java 版 26.3 Windows 客户端执行任意代码。1.20.5 至 1.21.10 及 26.1 至 26.4 快照受影响，1.20.4 及更早版本与基岩版不受影响。Mojang 仍使用 lwjgl-freetype 3.4.3 且暂无补丁，社区 11 月 24 日发布 m2sfix 1.0.0，以 Java agent 或 mod 关闭 hinting 作为临时修复。

telegram · zaihuapd · 11月25日 12:46

**「背景：FreeType 与资源包机制」** FreeType 是开源字体渲染库，Minecraft Java 版通过 LWJGL 的 lwjgl-freetype 绑定使用它来渲染 TrueType 字体；服务器资源包可携带字体文件，客户端接受后会自动下载并启用，因此恶意字体可进入渲染路径（tool-1-1, tool-1-2, tool-1-3）。此前资源包通常被视为可信内容，玩家手动安装并启用资源包同样可能触发该漏洞（tool-1-2）。

**「影响与应对」** 在官方补丁发布前，玩家应避免添加任何资源包，并将多人游戏服务器资源包权限设为“禁用”，或安装社区临时修复 mod，否则连接恶意服务器可能被远程执行代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://threatcluster.io/cluster/minecraft2shell-unpatched-freetype-rce-in-minecraft-java-via-7b380721">Minecraft2Shell: Unpatched FreeType RCE in Minecraft Java via ...</a></li>
<li><a href="https://wurst.wiki/minecraft2shell">Minecraft2Shell Vulnerability - wurst.wiki</a></li>
<li><a href="https://www.cubiclauncher.org/security/minecraft2shell">Minecraft2Shell: native code execution through resource packs</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#RCE`, `#Minecraft`, `#FreeType`

---

<a id="item-tech-news-9"></a>
### [三星与 SK 海力士将采用长江存储 Xtacking 堆叠技术](https://tech.ifeng.com/c/8yLRPKxQy4L) ⭐️ 7.0/10

三星电子和 SK 海力士已通过交叉许可协议，同意在 3D NAND 闪存生产中采用长江存储的 Xtacking 晶圆键合技术。该技术将存储单元阵列与 CMOS 控制电路分别制作在两片晶圆上，再通过键合工艺合二为一，使两部分可独立生产和优化。Omdia 高级分析师指出，这使厂商可自行生产存储阵列，而将逻辑电路交由晶圆代工厂，从而采用更先进的制程。三方均拒绝置评，该协议尚未得到官方确认。

telegram · zaihuapd · 11月25日 14:33

**「技术背景」** 3D NAND 闪存通过垂直堆叠存储单元来提高存储密度，传统工艺中存储阵列与外围 CMOS 逻辑电路通常在同一晶圆上制造，制程选择相互制约。长江存储的 Xtacking 技术将存储单元阵列和 CMOS 逻辑电路分别制作在两片晶圆上，再通过键合工艺合二为一，使两部分可以各自独立生产和优化。

**「影响」** 采用 Xtacking 技术后，三星和 SK 海力士可将 3D NAND 的逻辑电路部分外包给晶圆代工厂，以利用更先进的制程节点，而存储阵列仍由自身生产，这可能在性能或成本上带来优势。

**标签**: `#semiconductor`, `#3D NAND`, `#YMTC`, `#memory technology`, `#wafer bonding`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美商务部被曝施压英特尔交出 10%股权](https://www.wired.com/story/inside-trumps-demands-to-another-chips-ceo/) ⭐️ 8.0/10

据法庭文件，2025 年 8 月美国商务部律师在电话中警告英特尔首席财务官，不要“误以为这是一场谈判”，并称总统希望周五宣布协议，董事会可拒绝但会面临“无法预测的后果”。几天后英特尔董事会交出美方要求的股份，特朗普随后宣布美国政府“完全拥有并控制英特尔 10%的股份”，且未为此付款，这批股份现值约 110 亿美元。

telegram · zaihuapd · 11月25日 13:25

**「背景」** 此前，特朗普政府曾依据《芯片与科学法案》向英特尔提供拨款；2025 年 8 月，双方达成将剩余拨款转为股权的协议。

**「影响」** 据法庭文件，英特尔现有股东持股被稀释约 10%，相当于约 110 亿美元的公司价值被无偿划转给美国政府，股东权益受损。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.annacoulling.com/stock-trader-tips/intel-intc-from-chips-act-equity-stake-to-breakout-momentum/">Intel (INTC): From CHIPS Act Equity Stake to Breakout Momentum...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2025-08-22/trump-poised-to-unveil-intel-deal-for-equity-stake-on-friday">Trump Poised to Unveil Intel Deal For Equity Stake on... - Bloomberg</a></li>

</ul>
</details>

**标签**: `#Intel`, `#US Commerce Department`, `#government equity stake`, `#semiconductor industry`, `#industrial policy`

---

<a id="item-finance-news-2"></a>
### [美国拟对中国、欧盟等 14 个贸易伙伴加征新关税](https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html) ⭐️ 8.0/10

美国政府拟依据 1974 年《贸易法》第 301 条，对中国、欧盟、日本、印度等 14 个贸易伙伴加征新关税，以应对制造业产能过剩；其中中国将在 2018 年已加征的 25%基础上再加征 20%，若未遵守 2025 年 10 月釜山贸易休战协议，对华新关税可能升至 40%。

telegram · zaihuapd · 11月25日 13:59

**「背景」** 这是提案而非最终政策；新关税按国别设定，不实行统一税率，除中国外不与现有关税叠加，且不会超过双方在对等贸易框架协议中公布的税率。

**标签**: `#trade policy`, `#tariffs`, `#China`, `#European Union`, `#Section 301`

---

<a id="item-finance-news-3"></a>
### [英伟达行情波动考验美联储主席沃什的市场信号策略](https://www.cnbc.com/2026/11/25/nvidia-kevin-warsh-fed-market-signals.html) ⭐️ 7.0/10

上周英伟达引发的市场剧烈波动，使美联储主席凯文·沃什（Kevin Warsh）倡导的以市场信号而非传统预测指导政策的理念面临考验。高盛金融状况指数周一回落 22 个基点，逆转了上周近一半的紧缩幅度，市场对 12 月和 1 月加息的预期随之回升。

rss · CNBC Finance · 11月25日 12:26

**「背景」** 沃什认为市场预期比经济模型和华尔街经济学家的预测更准确，但市场指标本身可能极度波动。他正通过人工智能工作组等机制推动美联储减少前瞻指引、更多依赖市场信号，而英伟达行情恰恰显示了市场信号可能过于短期化。

**「影响」** 对美联储政策路径而言，这一波动凸显了依赖市场信号的挑战：人工智能建设对通胀和增长的影响尚不确定，若出现类似“中国冲击”的服务业失业，可能促使美联储降息，而当前 AI 投资热潮则推升通胀压力，使利率面临上行风险。

**标签**: `#Federal Reserve`, `#Monetary Policy`, `#Market Signals`, `#Nvidia`, `#Kevin Warsh`

---

<a id="item-finance-news-4"></a>
### [黄仁勋重返英伟达，凸显美中 AI 人才竞争](https://www.cnbc.com/2026/11/25/jensen-huang-nvidia-ai-talent-race.html) ⭐️ 7.0/10

黄仁勋于 11 月 23 日重返英伟达 CEO 职位，此前他于 11 月 12 日因婚外情报道辞职。卡内基国际和平基金会研究显示，中国在全球 AI 人才份额上已在三年内超过美国。

rss · CNBC Finance · 11月25日 14:29

**「背景」** 黄仁勋 11 月 12 日因被报道与一名美方情报机构认为与中国情报机构有关联的女性有婚外情而辞职，特朗普称其干预促成了他的回归；这一事件凸显美中 AI 竞争已从芯片延伸到人才争夺。

**标签**: `#Nvidia`, `#AI talent`, `#US-China tech race`, `#corporate governance`, `#semiconductors`

---