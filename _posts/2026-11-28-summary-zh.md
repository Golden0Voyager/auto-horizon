---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 31 条内容中筛选出 11 条重要资讯。

---

**科技新闻**
1. [Linux 内核 NFS 服务器曝 9.8 分预认证漏洞，无需登录可获 root](#item-tech-news-1) ⭐️ 8.0/10
2. [DeepCrossAttention：最高 3 倍加速，质量相当](#item-tech-news-2) ⭐️ 7.0/10
3. [Convex 技能未告知即上传用户应用想法至远程服务器](#item-tech-news-3) ⭐️ 7.0/10
4. [购物网站现 WebRTC 信用卡盗刷脚本](#item-tech-news-4) ⭐️ 7.0/10
5. [AI 工具 Artex 被用于攻击美国情报机构](#item-tech-news-5) ⭐️ 7.0/10
6. [《我的世界》基岩版资源包漏洞影响 26.52 至 26.63，26.65 已修复](#item-tech-news-6) ⭐️ 7.0/10
7. [微软推进以 Windows 内置驱动取代部分第三方驱动](#item-tech-news-7) ⭐️ 7.0/10

**财经新闻**
1. [国常会部署稳市：优化中央汇金类平准基金功能](#item-finance-news-1) ⭐️ 9.0/10
2. [英伟达行情波动考验沃什以市场信号指导政策的思路](#item-finance-news-2) ⭐️ 7.0/10
3. [央行下调大额存单认购门槛 个人起购降至 10 万元](#item-finance-news-3) ⭐️ 7.0/10
4. [市场监管总局约谈 15 家电动自行车企业](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Linux 内核 NFS 服务器曝 9.8 分预认证漏洞，无需登录可获 root](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

OpenSec 披露了 Linux 内核 NFS 服务器 nfsd 的预认证堆溢出漏洞 CVE-2026-99362，CVSS 评分为 9.8。攻击者无需任何登录凭据，仅需向 tcp/2049 端口发送一条连接即可越界写入内核堆，进而获取 root shell。该漏洞自 2014 年的 Linux 3.16 起存在，影响所有启用 NFSv4.1 或 4.2 的主机，波及文件服务器、NAS 和集群存储节点。修复版本已发布在 6.12.117、6.18.61、7.3.2 和 7.4-rc1 中，用户需升级内核并重启；无法立即升级的部署应通过防火墙限制 tcp/2049 访问。CVE 于 2026 年 11 月 20 日公开。

telegram · zaihuapd · 11月27日 12:57

**「背景信息」** NFS 服务器 nfsd 是 Linux 内核中处理 NFSv4.1/4.2 请求的组件，该漏洞位于其预认证处理路径，攻击者只需能访问 tcp/2049 即可触发。该缺陷自 Linux 3.16（2014 年）引入，至今已有 12 年。

**「影响与应对」** 对于启用 NFSv4.1 或 4.2 的主机（如文件服务器、NAS 和集群存储节点），攻击者无需任何凭据，仅向 tcp/2049 发送一条连接即可触发内核堆越界写入；Red Hat 的描述确认该漏洞可导致内存损坏、系统崩溃（拒绝服务）或执行任意代码，OpenSec 的披露进一步指出可借此获得 root shell。修复需升级内核至 6.12.117、6.18.61、7.3.2 或 7.4-rc1 并重启；无法立即升级的部署应通过防火墙限制 tcp/2049 的访问。该漏洞自 Linux 3.16（2014 年）起存在，且 NFSv4.1/4.2 是许多发行版的默认配置，受影响面较广。

<details><summary>参考链接</summary>
<ul>
<li>Critical Linux kernel vulnerability allows remote root access - SC Media</li>
<li>NFS2ROOT (CVE-2026-99362) on CentOS 7: Fixed Kernel</li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://feedly.com/cve/CVE-2026-99362">CVE-2026-99362 - Exploits &amp; Severity - Feedly</a></li>

</ul>
</details>

**标签**: `#Linux kernel`, `#NFS`, `#security vulnerability`, `#CVE`, `#remote code execution`

---

<a id="item-tech-news-2"></a>
### [DeepCrossAttention：最高 3 倍加速，质量相当](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

谷歌研究院推出 DeepCrossAttention，一种对 Transformer 残差连接的修改，声称在保持可比模型质量的同时实现最高 3 倍的速度提升。该技术来自研究博客，因此加速效果是研究报告的结果，而非独立测量的生产基准。“最高”这一限定词表明该增益并非在所有模型或任务上普遍适用。

hackernews · ComputedCamp995 · 11月27日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50672565)

**「背景」** Transformer 的残差连接传统上直接相加前几层的输出，可能稀释关键信息。DeepCrossAttention（DCA）通过可学习权重进行跨层路由，以增强残差学习；该工作此前已以论文形式在 arXiv 发布，并发表于 ICML 2025。

**「影响」** 对从业者而言，该结果暗示了在不损失质量的情况下加速 Transformer 训练的潜在路径，但该技术尚未作为现成库或框架功能发布，需要自行实现并在自身工作负载上验证。

**「社区讨论」** 评论者指出该方法在概念上与 DenseNet 相似（ipunchghosts），并询问它能否与 MTP 和 Dflash 等其他加速技术叠加以进一步获益（yieldcrv）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://arxiv.org/html/2502.06785">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>
<li><a href="https://scholar.google.com/citations?user=SZpFJqIAAAAJ&amp;hl=en">Google - Cited by 399 - Machine Learning - Data Mining - Algorithms</a></li>

</ul>
</details>

**标签**: `#transformer`, `#deep learning`, `#performance optimization`, `#Google Research`, `#residual connections`

---

<a id="item-tech-news-3"></a>
### [Convex 技能未告知即上传用户应用想法至远程服务器](https://github.com/convex/convex-backend-skill/issues/64) ⭐️ 7.0/10

GitHub 上的一个 issue 显示，Convex 的 AI 编码技能会在未明确告知用户的情况下，将用户的应用想法发送到远程服务器。Convex CEO Jamie 在评论中回应称，该提示词上传用于 Convex 的 quickstart 功能，是已关闭的 Convex Chef 项目的“精神继承者”，用于引导创建应用。该行为已随技能发布，但社区仍在讨论其透明度和信任问题。

hackernews · MickyTheMouse · 11月27日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50669765)

**「背景」** 该插件中的提示词上传功能驱动了 Convex 的“快速开始”功能，它是 Convex Chef 的精神继承者——Convex Chef 是一个端到端的 vibe-coding 产品，最近已被关闭。这解释了为什么该技能会将用户的应用想法发送到远程服务器：它从提示词引导出一个完整应用。

**「影响」** 使用该技能的开发者应意识到，其应用想法会被上传至 Convex 服务器，且该行为未在界面中明确披露。CEO 的回应将这一上传解释为 quickstart 功能的一部分，但并未消除社区对信任和提示注入的担忧；开发者可能需要自行审查数据流或选择替代方案。

**「社区讨论」** CEO Jamie 回应称该上传用于 Convex quickstart 功能，是已关闭的 Convex Chef 的精神继承者；评论者 jaynate 则指出提示注入比模型自行发起恶意工具调用更常见，社区因此围绕信任与透明披露展开争论。

<details><summary>参考链接</summary>
<ul>
<li>Convex skills send the user&#x27;s app idea to a remote server without telling ...</li>

</ul>
</details>

**标签**: `#security`, `#privacy`, `#AI tools`, `#prompt injection`, `#Convex`

---

<a id="item-tech-news-4"></a>
### [购物网站现 WebRTC 信用卡盗刷脚本](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

多个热门购物网站上发现了利用 WebRTC 的信用卡盗刷脚本，为 Magecart 式攻击开辟了一条新的数据窃取途径。与常见的 HTTP 请求方式不同，这些脚本借助 WebRTC 通道传输窃取的支付信息。该发现于 11 月 27 日由 hackernews 报道，社区讨论指出其核心风险并非 WebRTC 的技术能力，而是第三方脚本嵌入带来的信任缺口。

hackernews · scanr · 11月27日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50668145)

**「背景」** Magecart 是专门在在线结账页面植入恶意 JavaScript 窃取支付数据的犯罪集团统称。2026 年 1 月 14 日 Aviatrix 的研究报告曾披露一场持续数年的 Magecart 网络窃码活动，波及 American Express、Mastercard 等支付网络及众多电商网站；同年 8 月 Xictron 的防御指南也指出结账页仍是主要目标，建议用内容安全策略（CSP）和子资源完整性（SRI）加固。本次报道的 WebRTC 脚本延续了同一攻击家族的手法，但利用较少被监控的 WebRTC 通道作为新载体。

**「对站点运营者的影响」** 对运营电商站点的开发者而言，最直接的后果是必须重新审视第三方脚本的加载策略：将支付组件所需的第三方脚本锁定到明确的主机名并尽可能使用 SRI，同时采用 nonce 型 CSP 并开启 report-uri/report-to 以捕获异常脚本执行；此外，connect-src 规则可阻断 WebRTC 建立前的两个网络请求，从而在数据外传前拦截。受影响站点已于 11 月 24 日至 25 日移除该脚本，但任何嵌入第三方脚本的站点仍面临同类风险。

**「社区讨论」** 社区讨论中，用户 afavour 指出该攻击并非依赖 WebRTC 的技术能力，而是因为该协议较少被安全监控，且任何嵌入第三方脚本的站点都面临类似风险。用户 snickerer 进一步认为，根本问题在于网页允许第三方执行任意代码，浏览器应只接收数据并自行决定如何处理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aviatrix.ai/threat-research-center/web-skimming-campaign-magecart-2026/">2026 Magecart Web Skimming Campaign Compromises Payment Data</a></li>
<li><a href="https://www.xictron.com/en/blog/magecart-checkout-skimming-protection-2026/">Magecart 2026: Detect and Defend Checkout Skimming</a></li>
<li><a href="https://cyberreplay.com/blog/webrtc-skimmer-detection-detect-block-csp-bypassing-payment-skimmers/">WebRTC Skimmer Detection: How to Detect and Block CSP ...</a></li>
<li><a href="https://rfxn.com/research/webrtc-skimmer-csp-bypass">WebRTC Skimmers: How Payment Thieves Bypass Content Security ...</a></li>
<li><a href="https://daily.dev/posts/credit-card-skimming-scripts-using-webrtc-found-on-popular-shopping-sites-mr8zgdbaf">Credit card skimming scripts using WebRTC found on...</a></li>

</ul>
</details>

**标签**: `#web security`, `#credit card skimming`, `#WebRTC`, `#Magecart`, `#JavaScript`

---

<a id="item-tech-news-5"></a>
### [AI 工具 Artex 被用于攻击美国情报机构](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 7.0/10

《纽约时报》报道，黑客使用开源 AI 工具 Artex 攻击了美国中央情报局、国家地理空间情报局和国家情报总监办公室，影响限于非机密侦察数据。Artex 可整合多个开源 AI 模型来测试网络和计算机防御，今年早些时候由一名中国开发者发布，后被用于包括针对欧盟在内的多起攻击，该开发者已将其从 GitHub 删除。美国联邦调查局此前曾警告网络罪犯和间谍正广泛使用 Artex。

telegram · zaihuapd · 11月27日 10:42

**「背景」** Artex 是一个开源自主多智能体 AI 渗透测试框架，可整合多个开源 AI 模型来探测网络和计算机防御；它最初以开源项目形式发布，后因被滥用（包括针对韩国金融机构的攻击）而转为私有。

**「影响」** 由于 Artex 是开源工具，开发者删除 GitHub 仓库并不能阻止其继续传播；FBI 的警告及针对欧盟的攻击表明，AI 辅助的网络侦察已成为多起攻击的共同特征，防御方需将此类工具纳入威胁评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai-threat.watch/aof/artex/">ARTEX : agentic offensive framework | AI Threat Watch</a></li>
<li><a href="https://www.s-rminform.com/latest-thinking/artex-in-the-wild-lessons-from-responding-to-agentic-ai-attacks">Artex in the wild: Lessons from responding to agentic AI attacks</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#AI`, `#intelligence agencies`, `#Artex`, `#open-source`

---

<a id="item-tech-news-6"></a>
### [《我的世界》基岩版资源包漏洞影响 26.52 至 26.63，26.65 已修复](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

《我的世界》基岩版存在资源包安全漏洞：包含 content.zipe 文件的资源包可篡改游戏界面框架 Ore UI 并执行隐藏脚本，影响 26.52 至 26.63 版本（更早版本也可能受影响），覆盖 PC、手机和主机平台，Java 版不受影响。附加组件开发者 8Crafter 于 11 月 15 日在 Reddit 公开该问题，利用方式包括删除全部存档、获取玩家 IP，在 Windows 上特定条件下还能无提示打开任意 URI 并启动资源包内的批处理文件下载恶意软件。Mojang 已在 26.65 版修复该漏洞，AxmBro 发布了 Windows 只读检测工具用于查找 content.zipe 文件，但无法判定资源包是否恶意。

telegram · zaihuapd · 11月27日 18:04

**「背景」** 《我的世界》基岩版支持通过资源包自定义游戏界面，玩家加入服务器或 Realm 时若开启资源包自动下载，无需手动安装就可能收到问题文件。Ore UI 是基岩版的界面框架，本次漏洞正是通过篡改该框架的文件来运行隐藏脚本。

**「影响与应对」** Windows 玩家面临最高风险：特定条件下漏洞可无提示打开任意 URI 并启动资源包内的批处理文件下载恶意软件，可能导致系统感染。建议玩家立即更新至 26.65 或更高版本，并使用 AxmBro 发布的只读检测工具检查本地资源包中是否存在 content.zipe 文件。

**标签**: `#security`, `#vulnerability`, `#Minecraft`, `#malware`, `#resource pack`

---

<a id="item-tech-news-7"></a>
### [微软推进以 Windows 内置驱动取代部分第三方驱动](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

微软在 Ignite 2026 大会上确认，正为整类硬件开发全新驱动，计划以 Windows 内置驱动取代部分第三方驱动，以减少第三方代码进入系统内核。打印机是首批重点，近期推出的 Windows Ready Print 模式用于取代旧式第三方打印驱动；产品经理 Mehmet Kucukgoz 称，SoundWire、SDCA 等音频类驱动将很快成为 Windows 内置组件，I3C 总线、USB 以太网和 MIPI 摄像头类驱动也在开发中。微软还在 Windows 硬件工程大会上推出驱动质量倡议（DQI），提升驱动可靠性、质量和安全标准，并鼓励第三方开发者及 OEM 尽量使用内置驱动。

telegram · zaihuapd · 11月28日 02:09

**「背景」** Windows 传统上依赖第三方厂商提供的内核驱动来支持打印机、音频、总线等硬件，这些驱动运行在内核态，直接影响系统稳定性和安全性。Ready Print 是微软近期推出的内置打印驱动模式，用于取代旧式第三方打印驱动，是这一替代进程的首批成果。

**「对驱动开发者和 OEM 的影响」** 对驱动开发者和 OEM 而言，微软的驱动质量倡议（DQI）已实际改变其工作方式：驱动质量衡量标准从崩溃扩展到稳定性、功能、性能及功耗/热影响，并更新了相关要求、工具与质量信号。同时，随着打印机、音频、I3C、USB 以太网和 MIPI 摄像头等类别的内置驱动逐步落地，第三方驱动开发者需要评估其驱动是否会被 Windows 内置组件取代，并相应调整兼容性与测试策略。

<details><summary>参考链接</summary>
<ul>
<li>What is the Driver Quality Initiative (DQI)? - Windows - Microsoft Learn</li>
<li>Raising the bar together. Introducing the Driver Quality Initiative at ...</li>
<li>Welcome to WinHEC Online - Microsoft Community Hub</li>

</ul>
</details>

**标签**: `#Windows`, `#drivers`, `#Microsoft`, `#kernel security`, `#hardware`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [国常会部署稳市：优化中央汇金类平准基金功能](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 9.0/10

国务院常务会议 11 月 27 日部署资本市场稳市机制，提出优化中央汇金公司类“平准基金”功能、提供充足流动性保障，并推动上市公司加大分红回购、引导中长期资金入市。会议还要求依法强化全链条监管，坚决查处财务造假、违规减持等行为。

telegram · zaihuapd · 11月27日 05:35

**「背景」** 中央汇金是中国投资有限责任公司旗下的国有投资公司，市场俗称“国家队”，曾在 2015 年股市大跌时大举买入交易型开放式指数基金（ETF）和金融股；11 月 5 日国务院报告已提出支持其发挥类“平准基金”作用，即由政府资金在市场异常波动时买卖资产以稳定价格。

**「市场影响」** 受会议释放的稳市信号影响，11 月 27 日 A 股主要股指在消息公布后上涨，投资者信心得到提振。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.yahoo.com/economy/policy/articles/china-strengthen-defense-against-imported-063242849.html?fr=sycsrp_catchall">China cabinet calls for greater role by &#x27;national team ...</a></li>
<li><a href="https://www.globaltimes.cn/page/202611/1373716.shtml">China’s State Council report calls for supporting state-owned ...</a></li>
<li><a href="https://www.bnnbloomberg.ca/business/international/2026/11/27/what-is-chinas-national-team-and-can-it-stop-the-stock-market-slide/">What is China’s ‘national team’ of investors?</a></li>
<li><a href="http://en.people.cn/n3/2026/1128/c90000-20524130.html">China sends key signals to steady capital market - People&#x27;s ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-27/china-s-cabinet-stresses-market-support-in-midday-release">China Stocks Rally After Rare Midday Statement on Market ...</a></li>

</ul>
</details>

**标签**: `#China`, `#capital market`, `#policy`, `#Central Huijin`, `#stabilization fund`

---

<a id="item-finance-news-2"></a>
### [英伟达行情波动考验沃什以市场信号指导政策的思路](https://www.cnbc.com/2026/11/25/nvidia-kevin-warsh-fed-market-signals.html) ⭐️ 7.0/10

本周英伟达股价剧烈波动，令美联储主席沃什（Kevin Warsh）主张更多依赖市场信号而非经济预测来制定政策的思路面临考验。周一高盛金融状况指数实际回落 22 个基点，几乎逆转上周近一半的紧缩幅度，市场对 12 月和 1 月加息的预期随之回升。

rss · CNBC Finance · 11月27日 13:29

**「背景」** 沃什认为多数经济预测质量不佳，主张更多参考通胀补偿、信用利差、股指和国债利率等市场指标，并为此设立了包括人工智能在内的五个政策研究工作组，同时将议息会后新闻发布会缩短至半小时，避免提供前瞻指引。

**「影响」** 对依赖政策指引的投资者和企业而言，市场指标的高波动意味着美联储信号可能随每日行情反复摇摆；同一经济发展（如人工智能建设）可能同时发出通胀上行和就业冲击两种相反信号。

**标签**: `#Federal Reserve`, `#monetary policy`, `#Kevin Warsh`, `#market signals`, `#Nvidia`

---

<a id="item-finance-news-3"></a>
### [央行下调大额存单认购门槛 个人起购降至 10 万元](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 7.0/10

中国人民银行 11 月 27 日公布《大额存单管理办法》，将个人投资人认购起点从 20 万元下调至 10 万元、机构从 1000 万元下调至 500 万元，自 2027 年 3 月 21 日起施行；同日发布的《人民币存贷款利率管理规定》要求金融机构自主定价、不得高息揽储。

telegram · zaihuapd · 11月27日 11:36

**「背景」** 原 2015 年《大额存单管理暂行办法》规定个人、机构认购起点分别为 20 万元和 1000 万元，新办法将两个门槛均下调一半；同日发布的《人民币存贷款利率管理规定》要求金融机构自主确定存贷款利率，不得高息揽储。

**「影响」** 门槛降至 10 万元使更多普通储户可购买大额存单，而禁止高息揽储或限制中小银行以高利率吸储的空间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://post.smzdm.com/p/a26zmerq/">2026年20...</a></li>

</ul>
</details>

**标签**: `#央行政策`, `#大额存单`, `#存款利率`, `#银行业监管`, `#金融监管`

---

<a id="item-finance-news-4"></a>
### [市场监管总局约谈 15 家电动自行车企业](https://www.news.cn/20261127/0c8c665ce70c417b9263b39fa8a519f0/c.html?hl=zh-CN) ⭐️ 7.0/10

市场监管总局 11 月 27 日集中约谈雅迪、台铃、爱玛、九号、小牛等 15 家电动自行车企业，要求整改并严格执行“一车一池一充一码”（每辆车对应一块电池、一个充电器和一个编码）标准，对确认存在缺陷的产品立即召回。

telegram · zaihuapd · 11月27日 12:06

**「背景」** 此次约谈源于监管部门近期对电动自行车开展的 CCC 认证（强制性产品认证）全覆盖飞行检查，发现部分企业质量保证能力欠缺、产品一致性管控不严，并违反强制性国家标准出厂销售不合格产品。

**「影响」** 整改与召回要求将增加涉事企业的合规和售后成本；已购买相关车型的消费者若产品被确认存在缺陷，也可能获得召回处理。

**标签**: `#regulatory action`, `#electric bicycle industry`, `#product safety`, `#China regulation`, `#consumer goods`

---