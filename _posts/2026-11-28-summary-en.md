---
layout: default
title: "Horizon Summary: 2026-11-28 (EN)"
date: 2026-11-28
lang: en
---

> From 31 items, 11 important content pieces were selected

---

**Technology News**
1. [Critical pre-auth NFS server heap overflow \(CVE-2026-99362\) grants unauthenticated root](#item-tech-news-1) ⭐️ 8.0/10
2. [DeepCrossAttention: comparable quality, up to 3x faster](#item-tech-news-2) ⭐️ 7.0/10
3. [Convex skill uploads app ideas to remote server without telling users](#item-tech-news-3) ⭐️ 7.0/10
4. [WebRTC-based credit card skimmers found on shopping sites](#item-tech-news-4) ⭐️ 7.0/10
5. [AI tool Artex used in cyberattack on US intelligence agencies](#item-tech-news-5) ⭐️ 7.0/10
6. [Minecraft Bedrock resource pack vulnerability fixed in 26.65](#item-tech-news-6) ⭐️ 7.0/10
7. [Microsoft plans built-in Windows drivers to replace third-party drivers](#item-tech-news-7) ⭐️ 7.0/10

**Financial News**
1. [China&\#x27;s State Council moves to stabilize capital markets, optimize Central Huijin&\#x27;s quasi-stabilization fund role](#item-finance-news-1) ⭐️ 9.0/10
2. [Fed Chair Warsh&\#x27;s market-signal approach faces volatility test](#item-finance-news-2) ⭐️ 7.0/10
3. [China&\#x27;s central bank halves minimum purchase for large certificates of deposit](#item-finance-news-3) ⭐️ 7.0/10
4. [China&\#x27;s market regulator calls in 15 electric bicycle makers over quality issues](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Critical pre-auth NFS server heap overflow \(CVE-2026-99362\) grants unauthenticated root](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

OpenSec disclosed a critical pre-authentication heap overflow in the Linux kernel NFS server \(CVE-2026-99362, CVSS 9.8, public since Nov 20, 2026\). An unauthenticated attacker can send a single connection to tcp/2049 to write out of bounds into the kernel heap and obtain a root shell on hosts with NFSv4.1 or 4.2 enabled. The flaw has existed since Linux 3.16 \(2014\) and affects file servers, NAS, and cluster storage nodes. Fixes are available in kernels 6.12.117, 6.18.61, 7.3.2, and 7.4-rc1; until patched, restrict tcp/2049 access with a firewall.

telegram · zaihuapd · Nov 27, 12:57

**「Background」** NFS \(Network File System\) is a protocol that allows remote clients to access files over a network; in Linux, the kernel&\#x27;s nfsd server handles NFS requests. The vulnerability is a pre-authentication heap overflow in nfsd, which has been present since Linux 3.16 \(2014\). This long-standing flaw means many deployed file servers, NAS devices, and cluster storage nodes may be exposed.

**「Unauthenticated root access on NFSv4.1/4.2 hosts」** Administrators of Linux file servers, NAS appliances, and cluster storage nodes running NFSv4.1 or NFSv4.2 — the default in many distributions — face unauthenticated remote root access: a single connection to tcp/2049 can trigger a pre-authentication heap overflow \(CVE-2026-99362, CVSS 9.8\) and yield a root shell, with Red Hat confirming memory corruption and potential arbitrary code execution. The fix requires upgrading to kernel 6.12.117, 6.18.61, 7.3.2, or 7.4-rc1 and rebooting; where an immediate upgrade is not possible, restrict tcp/2049 access with a firewall.

<details><summary>References</summary>
<ul>
<li>NFS2ROOT (CVE-2026-99362) on CentOS 7: Fixed Kernel</li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://feedly.com/cve/CVE-2026-99362">CVE-2026-99362 - Exploits &amp; Severity - Feedly</a></li>

</ul>
</details>

**Tags**: `#Linux kernel`, `#NFS`, `#security vulnerability`, `#CVE`, `#remote code execution`

---

<a id="item-tech-news-2"></a>
### [DeepCrossAttention: comparable quality, up to 3x faster](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

Google Research introduced DeepCrossAttention, a modification to transformer residual connections that the team reports achieves model quality comparable to standard transformers while running up to 3x faster. The result is presented in a research blog post, so the speedup is a vendor claim rather than an independently measured production capability. Practitioners should treat the figure as a research finding to be validated on their own workloads.

hackernews · ComputedCamp995 · Nov 27, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50672565)

**「Background」** Standard transformer residual connections simply sum the outputs of previous layers, which can dilute crucial information as depth increases. DeepCrossAttention \(DCA\) was introduced in a paper presented at ICML 2025 to enhance residual learning in transformers, and the Google Research blog post describes the approach and its reported speedups.

**「Impact」** If the speedup holds on real workloads, transformer training and inference could become up to 3x faster, reducing compute costs for practitioners. Because the result is from a research blog post, teams should benchmark DeepCrossAttention against their own models before adopting it.

**「Community discussion」** ipunchghosts suggested the approach resembles DenseNet&\#x27;s dense connections, while yieldcrv asked whether it could stack with other token-generation speedups like MTP and Dflash to reach 30x tokens/sec. These are opinions from commenters, not established facts.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2502.06785">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>
<li><a href="https://scholar.google.com/citations?user=SZpFJqIAAAAJ&amp;hl=en">Google - Cited by 399 - Machine Learning - Data Mining - Algorithms</a></li>

</ul>
</details>

**Tags**: `#transformer`, `#deep learning`, `#performance optimization`, `#Google Research`, `#residual connections`

---

<a id="item-tech-news-3"></a>
### [Convex skill uploads app ideas to remote server without telling users](https://github.com/convex/convex-backend-skill/issues/64) ⭐️ 7.0/10

A GitHub issue reports that Convex&\#x27;s AI coding skill uploads a user&\#x27;s app idea to a remote server without telling them. Convex CEO Jamie responded that the prompt upload powers the Convex &quot;quickstart&quot; feature, the spiritual successor to the recently shut down Convex Chef. The response frames the upload as a product feature rather than disputing that the data is sent to Convex&\#x27;s servers.

hackernews · MickyTheMouse · Nov 27, 18:02 · [Discussion](https://news.ycombinator.com/item?id=50669765)

**「Background」** Convex previously ran Convex Chef, an end-to-end vibe-coding product that was shut down; the prompt upload in this skill powers the Convex &quot;quickstart&quot; feature, which CEO Jamie describes as the spiritual successor to Chef \(tool-2-1\). The skill is installed via \`npx convex ai-files\`, which now installs separate copies for each coding agent instead of symlinks \(tool-2-2\).

**「Impact」** Developers using the Convex quickstart feature should assume their app ideas are transmitted to Convex&\#x27;s servers, and those with privacy constraints may need to avoid the feature.

**「Community discussion」** Commenters disagreed about the upload&\#x27;s nature: one argued prompt injection is more common than models making malicious tool calls on their own, while another suggested self-hosted open-weight models as the long-term solution. Convex CEO Jamie&\#x27;s response frames the upload as powering the quickstart feature, but commenters still questioned whether the behavior was appropriate.

<details><summary>References</summary>
<ul>
<li>Convex skills send the user&#x27;s app idea to a remote server without telling ...</li>
<li>convex-js/CHANGELOG.md at main - GitHub</li>

</ul>
</details>

**Tags**: `#security`, `#privacy`, `#AI tools`, `#prompt injection`, `#Convex`

---

<a id="item-tech-news-4"></a>
### [WebRTC-based credit card skimmers found on shopping sites](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

Security researchers have identified credit card skimming scripts that abuse WebRTC on popular shopping sites, highlighting a new vector for Magecart-style attacks. The scripts were found in the wild, indicating an active attack rather than a theoretical risk. The finding warrants prompt attention from web security practitioners.

hackernews · scanr · Nov 27, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50668145)

**「Background」** Magecart groups have long used malicious JavaScript on checkout pages to steal payment data, a technique known as web skimming that has targeted e-commerce and payment websites since at least 2022. The new report describes a variant that uses WebRTC as a less-monitored channel for the same kind of credit card theft, extending the known attack surface rather than introducing a fundamentally new threat actor.

**「Impact on site operators and shoppers」** Site operators who embed third-party payment scripts face a CSP-bypassing exfiltration channel: the WebRTC skimmer can send stolen card data without being blocked by connect-src, and the five affected sites only removed the script on November 24–25 after detection. Mitigation requires locking third-party scripts to explicit hostnames with SRI, using nonce-based script policies, and enabling strict CSP reporting; a connect-src rule can also block the two web requests the script needs before WebRTC opens.

**「Community Discussion」** Commenters argued that the attack is not a WebRTC-specific vulnerability but rather a consequence of embedding third-party scripts, which are always a risk; one commenter noted the same approach could be done with simple HTTP requests. Another commenter questioned why ad providers do not sandbox ads to prevent JavaScript execution.

<details><summary>References</summary>
<ul>
<li><a href="https://aviatrix.ai/threat-research-center/web-skimming-campaign-magecart-2026/">2026 Magecart Web Skimming Campaign Compromises Payment Data</a></li>
<li><a href="https://www.xictron.com/en/blog/magecart-checkout-skimming-protection-2026/">Magecart 2026: Detect and Defend Checkout Skimming</a></li>
<li><a href="https://www.malwarebytes.com/blog/news/2026/01/online-shoppers-at-risk-as-magecart-skimming-hits-major-payment-networks">Online shoppers at risk as Magecart skimming hits major ...</a></li>
<li><a href="https://cyberreplay.com/blog/webrtc-skimmer-detection-detect-block-csp-bypassing-payment-skimmers/">WebRTC Skimmer Detection: How to Detect and Block CSP ...</a></li>
<li><a href="https://rfxn.com/research/webrtc-skimmer-csp-bypass">WebRTC Skimmers: How Payment Thieves Bypass Content Security ...</a></li>
<li><a href="https://daily.dev/posts/credit-card-skimming-scripts-using-webrtc-found-on-popular-shopping-sites-mr8zgdbaf">Credit card skimming scripts using WebRTC found on...</a></li>

</ul>
</details>

**Tags**: `#web security`, `#credit card skimming`, `#WebRTC`, `#Magecart`, `#JavaScript`

---

<a id="item-tech-news-5"></a>
### [AI tool Artex used in cyberattack on US intelligence agencies](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 7.0/10

A New York Times report cited by Forbes says hackers used the open-source AI tool Artex in an attack on US intelligence agencies, including the CIA, the National Geospatial-Intelligence Agency, and the Office of the Director of National Intelligence. The attack affected non-classified reconnaissance data, and Artex, which integrates multiple open-source AI models to probe network defenses, was released by a Chinese developer earlier this year and has been used in other attacks, including one against the EU. The developer has since removed Artex from GitHub, and the FBI had previously warned that criminals and spies were widely using the tool.

telegram · zaihuapd · Nov 27, 10:42

**「Background」** Artex is an open-source autonomous multi-agent AI penetration testing framework that integrates multiple AI models to probe network and computer defenses. It was originally released as an open-source project and later made private after reports of misuse, including attacks against South Korean financial institutions; the FBI had already warned that cybercriminals and spies were widely using Artex.

<details><summary>References</summary>
<ul>
<li><a href="https://ai-threat.watch/aof/artex/">ARTEX : agentic offensive framework | AI Threat Watch</a></li>
<li><a href="https://www.s-rminform.com/latest-thinking/artex-in-the-wild-lessons-from-responding-to-agentic-ai-attacks">Artex in the wild: Lessons from responding to agentic AI attacks</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#AI`, `#intelligence agencies`, `#Artex`, `#open-source`

---

<a id="item-tech-news-6"></a>
### [Minecraft Bedrock resource pack vulnerability fixed in 26.65](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

A resource pack vulnerability in Minecraft Bedrock allows packs containing a content.zipe file to modify Ore UI framework files and run hidden scripts, affecting versions 26.52 through 26.63 on PC, mobile, and console; Java Edition is unaffected. Add-on developer 8Crafter disclosed the issue on Reddit on November 15, reporting exploitation methods including deleting all saves, obtaining player IPs, and on Windows, silently opening arbitrary URIs to launch batch files that download malware. Mojang fixed the issue in version 26.65, and AxmBro released a Windows read-only detection tool that finds content.zipe files but cannot determine whether a pack is malicious.

telegram · zaihuapd · Nov 27, 18:04

**「Background」** Resource packs in Minecraft Bedrock are user-installable content bundles that customize the game&\#x27;s interface and assets, and the Ore UI framework is the game&\#x27;s interface layer that such packs can modify. The vulnerability arises because a content.zipe file inside a resource pack can alter Ore UI files to execute hidden scripts, and players who join a server or Realm with resource pack auto-download enabled may receive such files without manually installing them.

**「Impact」** Players who join a server or Realm with resource pack auto-download enabled can receive a malicious pack without manually installing it, and on Windows the exploit can silently open arbitrary URIs to launch batch files that download malware; updating to version 26.65 is the only confirmed remediation, while the AxmBro detection tool can locate content.zipe files but cannot judge whether a pack is malicious.

**Tags**: `#security`, `#vulnerability`, `#Minecraft`, `#malware`, `#resource pack`

---

<a id="item-tech-news-7"></a>
### [Microsoft plans built-in Windows drivers to replace third-party drivers](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

Microsoft confirmed at Ignite 2026 that it is developing new drivers for entire hardware classes and will rely more on built-in Windows drivers, with some third-party code potentially replaced by built-in functionality to minimize third-party code entering the Windows kernel. Printers are the first focus: the recently introduced Windows Ready Print mode is intended to replace legacy third-party print drivers, and Windows product manager Mehmet Kucukgoz said SoundWire and SDCA audio drivers will soon become built-in Windows components, while I3C bus, USB Ethernet, and MIPI camera drivers are in development. Microsoft also introduced the Driver Quality Initiative \(DQI\) at the Windows Hardware Engineering Conference to raise driver reliability, quality, and security standards, encouraging third-party developers to use built-in drivers where possible and asking OEMs to follow the same approach for custom drivers. The announcement describes planned and in-development drivers, not shipped capabilities.

telegram · zaihuapd · Nov 28, 02:09

**「Background」** Windows has historically relied on third-party drivers for many hardware classes, with vendor-supplied code running in the kernel alongside Microsoft&\#x27;s own in-box drivers. This arrangement has been a recurring source of kernel security concerns, as third-party code has direct access to privileged system memory. Microsoft&\#x27;s push to replace these drivers with built-in components represents a shift toward reducing the amount of external code that runs at the kernel level.

**「Impact on driver developers and OEMs」** Driver developers and OEMs will need to meet the Driver Quality Initiative&\#x27;s expanded requirements, which now measure stability, functionality, performance, and power and thermal impact in addition to crashes \(tool-2-1, tool-2-2\). As Microsoft moves printer, audio, bus, and camera classes toward built-in Windows drivers, third-party driver vendors should plan for migration to the new in-box components, since some third-party code may be replaced.

<details><summary>References</summary>
<ul>
<li>What is the Driver Quality Initiative (DQI)? - Windows - Microsoft Learn</li>
<li>Raising the bar together. Introducing the Driver Quality Initiative at ...</li>

</ul>
</details>

**Tags**: `#Windows`, `#drivers`, `#Microsoft`, `#kernel security`, `#hardware`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s State Council moves to stabilize capital markets, optimize Central Huijin&\#x27;s quasi-stabilization fund role](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 9.0/10

China&\#x27;s State Council said on Nov 27 it will optimize Central Huijin&\#x27;s quasi-stabilization fund function and provide ample liquidity to stabilize capital markets, while pushing listed companies to increase dividends and buybacks and guiding long-term funds into the market. The measures, announced at a meeting chaired by Premier Li Qiang, also include strengthening regulation against financial fraud and illegal share reductions.

telegram · zaihuapd · Nov 27, 05:35

**「Background」** The &quot;national team&quot; is the market nickname for China&\#x27;s state-backed investors, usually led by Central Huijin, the domestic unit of sovereign wealth fund China Investment Corp; a Nov 5 State Council report already called for supporting Central Huijin&\#x27;s quasi-stabilization fund role and improving related mechanisms.

**「Impact」** Chinese equity investors saw major stock indices surge after the meeting, as the pledge to optimize Central Huijin&\#x27;s quasi-stabilization fund function and provide ample liquidity signaled stronger state support for the market.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.yahoo.com/economy/policy/articles/china-strengthen-defense-against-imported-063242849.html?fr=sycsrp_catchall">China cabinet calls for greater role by &#x27;national team ...</a></li>
<li><a href="https://www.globaltimes.cn/page/202611/1373716.shtml">China’s State Council report calls for supporting state-owned ...</a></li>
<li><a href="http://en.people.cn/n3/2026/1128/c90000-20524130.html">China sends key signals to steady capital market - People&#x27;s ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-27/china-s-cabinet-stresses-market-support-in-midday-release">China Stocks Rally After Rare Midday Statement on Market ...</a></li>

</ul>
</details>

**Tags**: `#China`, `#capital market`, `#policy`, `#Central Huijin`, `#stabilization fund`

---

<a id="item-finance-news-2"></a>
### [Fed Chair Warsh&\#x27;s market-signal approach faces volatility test](https://www.cnbc.com/2026/11/25/nvidia-kevin-warsh-fed-market-signals.html) ⭐️ 7.0/10

Market-based odds of Fed rate hikes swung sharply this week as Nvidia-driven volatility hit the Goldman Sachs Financial Conditions Index, which eased 22 basis points on Monday after last week&\#x27;s tightening, according to CNBC. The swings highlight the tension in Fed Chair Kevin Warsh&\#x27;s push to rely on market indicators rather than traditional forecasts for policy guidance.

rss · CNBC Finance · Nov 27, 13:29

**「Background」** Warsh has argued that market expectations—derived from inflation compensation, credit spreads, stock indexes, and Treasury yields—forecast better than economic models, and he has cut press conferences to 30 minutes while avoiding forward guidance. He convened an AI task force, including a San Francisco meeting last week, to broaden Fed thinking beyond daily market moves.

**「Impact」** The episode shows how short-term market swings can send conflicting policy signals, complicating the Fed&\#x27;s ability to set rates for where the economy will be next year, given long and variable lags in monetary policy.

**Tags**: `#Federal Reserve`, `#monetary policy`, `#Kevin Warsh`, `#market signals`, `#Nvidia`

---

<a id="item-finance-news-3"></a>
### [China&\#x27;s central bank halves minimum purchase for large certificates of deposit](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 7.0/10

The People&\#x27;s Bank of China on Nov 27 issued new rules for large-denomination certificates of deposit, cutting the individual minimum purchase to 100,000 yuan from 200,000 yuan and the institutional minimum to 5 million yuan from 10 million yuan, effective March 21, 2027. The central bank also issued regulations on deposit and loan interest rates, requiring financial institutions to set rates independently and banning high-interest deposit solicitation.

telegram · zaihuapd · Nov 27, 11:36

**「Background」** The new rules replace the 2015 interim measures, which set the individual purchase threshold at 200,000 yuan and the institutional threshold at 10 million yuan, and the accompanying interest-rate regulation requires banks to set deposit and loan rates independently and bans high-rate deposit solicitation.

**「Impact」** Small and medium-sized banks that have relied on offering rates 0.5-0.6 percentage points above peers to attract deposits may need to adjust their pricing strategies under the new ban on high-interest deposit solicitation.

<details><summary>References</summary>
<ul>
<li><a href="https://news.cctv.com/2026/11/27/ARTIgKmrmpYUnQWWQn8hOoAG261127.shtml">中国人民银行有关部门负责人就 《大额存单管理办法》答记者问_新闻频...</a></li>
<li><a href="https://post.smzdm.com/p/a26zmerq/">2026年20...</a></li>

</ul>
</details>

**Tags**: `#央行政策`, `#大额存单`, `#存款利率`, `#银行业监管`, `#金融监管`

---

<a id="item-finance-news-4"></a>
### [China&\#x27;s market regulator calls in 15 electric bicycle makers over quality issues](https://www.news.cn/20261127/0c8c665ce70c417b9263b39fa8a519f0/c.html?hl=zh-CN) ⭐️ 7.0/10

China&\#x27;s market regulator on Nov 27 summoned 15 electric bicycle makers, including Yadea, Tailg, Aima, Ninebot and Niu, for talks after inspections found quality-control lapses and sales of products that violated mandatory national standards, and ordered them to rectify and recall any confirmed defective models.

telegram · zaihuapd · Nov 27, 12:06

**「Background」** The interviews followed unannounced inspections of CCC \(China Compulsory Certification\) coverage that found quality-assurance and product-consistency problems; the regulator also required compliance with the &\#x27;one vehicle, one battery, one charger, one code&\#x27; rule, which matches each e-bike to a coded battery and charger.

**「Impact」** The 15 companies, which include major e-bike brands, must now recall any confirmed defective models and tighten quality controls, adding compliance and recall costs.

**Tags**: `#regulatory action`, `#electric bicycle industry`, `#product safety`, `#China regulation`, `#consumer goods`

---