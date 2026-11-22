---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 24 items, 9 important content pieces were selected

---

**Technology News**
1. [Lean verification of the Riemann Hypothesis with AI assistance](#item-tech-news-1) ⭐️ 10.0/10
2. [Zhejiang University reports first real-machine QRAM on superconducting chip](#item-tech-news-2) ⭐️ 9.0/10
3. [Monitor&\#x27;s USB Ethernet adapter silently cut download speed by 75%](#item-tech-news-3) ⭐️ 7.0/10
4. [Double-free vulnerability in GPGME before 2.3.0](#item-tech-news-4) ⭐️ 7.0/10
5. [Muru: Graham Dumpleton&\#x27;s AI-assisted Rust server for Python ASGI/WSGI](#item-tech-news-5) ⭐️ 7.0/10
6. [Microsoft&\#x27;s RDMA over USB4 preview lets multiple PCs share one local AI model](#item-tech-news-6) ⭐️ 7.0/10
7. [OpenRouter warns MiniMax prompts may have been read by third parties](#item-tech-news-7) ⭐️ 7.0/10

**Technology Blog**
1. [To Code Well, Avoid Blunders](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [Trump proposes tax on U.S. firms building AI data centers abroad](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Lean verification of the Riemann Hypothesis with AI assistance](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

A formal verification of the Riemann Hypothesis in Lean, assisted by AI, has been announced, marking a historic breakthrough in formal mathematics. The proof was developed in the Lean proof assistant with AI assistance, and the result is presented as a milestone for theorem proving and AI-assisted reasoning.

hackernews · g-b-r · Nov 21, 14:36 · [Discussion](https://news.ycombinator.com/item?id=50589618)

**「Background」** Lean is a proof assistant that mechanically checks mathematical arguments, and the Riemann Hypothesis is a 1859 conjecture about the zeros of the Riemann zeta function that has remained unproven for over a century. The Generalized Riemann Hypothesis extends this to Dirichlet L-functions. Anthropic researcher Levent Alpöge claimed in November 2026 that Claude assisted in proving the Generalized Riemann Hypothesis, with the proof written in Lean and now being verified by mathematicians.

**「Community Discussion」** Commenters debated the reliability of the verification: one argued that multiple independent checkers with consistency proofs make a bug-based refutation vanishingly unlikely, while another countered that a fake Collatz refutation previously passed an independent checker and that the checkers are not as independent as claimed, though a human expert in the loop reduces the risk.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/21/anthropic-riemann-hypothesis-solved-claude-ai">Anthropic mathematician claims he used Claude to... | The Guardian</a></li>
<li><a href="https://kingy.ai/blog/levent-alpoge-claude-riemann-hypothesis-proof/">Riemann hypothesis proof verified in Lean</a></li>
<li><a href="https://nypost.com/2026/11/20/business/anthropic-researcher-claims-claude-cracked-legendary-1m-math-problem-and-left-him-struggling-to-keep-up/">Anthropic researcher claims Claude cracked legendary $1M math...</a></li>

</ul>
</details>

**Tags**: `#formal verification`, `#Lean`, `#Riemann Hypothesis`, `#AI-assisted mathematics`, `#theorem proving`

---

<a id="item-tech-news-2"></a>
### [Zhejiang University reports first real-machine QRAM on superconducting chip](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 9.0/10

A Zhejiang University team has reported the first real-machine implementation of quantum random access memory \(QRAM\) on a self-fabricated superconducting quantum chip called Tianmu 2, with results published in Nature Physics. The chip ran prototypes that retrieved 4-bit and 8-bit data with accuracies of 80.9% and 60.4%, respectively, and the circuit depth was reduced by more than 30% compared with an unoptimized scheme. The team also verified for the first time that the architecture has local noise resistance. This is a research milestone on a prototype, not a commercial memory, and the team&\#x27;s next step is to pursue scale-up.

telegram · zaihuapd · Nov 21, 08:31

**「Background」** Quantum random-access memory \(QRAM\) is the quantum analogue of classical memory: it lets a quantum processor access stored data in superposition, rather than reading one address at a time. Earlier QRAM work had largely remained at the level of theoretical proposals or small-scale component demonstrations, so the reported implementation on Zhejiang University&\#x27;s superconducting chip &quot;Tianmu 2&quot; represents the first real-machine demonstration of the full QRAM architecture.

**「Impact」** For quantum computing researchers, this result provides the first real-hardware demonstration of QRAM on a superconducting chip, but the drop in accuracy from 80.9% at 4-bit retrieval to 60.4% at 8-bit retrieval, along with the team&\#x27;s stated need for scale-up, means practical use remains ahead.

**Tags**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#hardware`, `#research`

---

<a id="item-tech-news-3"></a>
### [Monitor&\#x27;s USB Ethernet adapter silently cut download speed by 75%](https://blog.tymscar.com/posts/studiodisplayethernet/) ⭐️ 7.0/10

A monitor&\#x27;s built-in USB Ethernet adapter was silently cutting download speeds by 75% because the extra latency it introduced prevented the laptop from acknowledging packets quickly enough, filling the adapter&\#x27;s buffer and forcing packet drops. The investigation traced the problem to the adapter&\#x27;s acknowledgement requirements and fixed it by switching to a different adapter that required less frequent acknowledgement. The case shows that USB hubs and docks can degrade networking in opaque ways that are easy to miss.

hackernews · soheilpro · Nov 21, 10:36 · [Discussion](https://news.ycombinator.com/item?id=50587875)

**「Background」** TCP throughput depends on the receiver acknowledging packets within the connection&\#x27;s window; if acknowledgements arrive too late, the sender&\#x27;s buffer fills and packets are dropped, triggering congestion control that cuts speed. USB Ethernet adapters add latency to this path, and a monitor&\#x27;s built-in hub can add enough to push the system past that threshold.

**「Impact」** Users who route Ethernet through a monitor or dock should check adapter flow-control and acknowledgement settings if they see unexplained throughput loss; one commenter reported that enabling flow control resolved a similar issue they had struggled with for over a year on a MacBook with a Thunderbolt dock.

**「Community Discussion」** Commenters clarified the mechanism—the monitor&\#x27;s extra latency delayed acknowledgements, filling the adapter&\#x27;s buffer and dropping packets—and noted the monitor itself is incidental; it is really a USB network switch. A parallel report described a similar opaque interaction where Ghostty&\#x27;s use of io\_uring registered as I/O pressure and throttled Baldur&\#x27;s Gate 3&\#x27;s shader compilation.

**Tags**: `#hardware`, `#networking`, `#debugging`, `#USB`, `#latency`

---

<a id="item-tech-news-4"></a>
### [Double-free vulnerability in GPGME before 2.3.0](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 7.0/10

A double-free vulnerability in GPGME versions before 2.3.0 affects applications that link the library, including mail clients, Samba, Flatpak, and GnuPG-based tools. The GnuPG project disclosed the bug on 2026-11-20 after GitLab informed it on 2026-11-12; a coordinated disclosure originally planned for 2026-11-25 was moved earlier because of the Ruby2Shell bug. The flaw is a double-free, not a remote code execution chain as the headline implies. The fix is available in GPGME 2.3.0.

hackernews · gdgghhhhh · Nov 21, 08:32 · [Discussion](https://news.ycombinator.com/item?id=50587208)

**「Background」** GPGME is a library that applications use to handle OpenPGP keys and signatures, and a double-free is a memory corruption bug where the same memory region is freed twice, which can be triggered by malicious OpenPGP keys.

**「Impact」** GitLab has published an Omnibus patch for the affected GPGME library; administrators should apply it or update to GPGME 2.3.0.

**「Community discussion」** Commenters noted that Red Hat had reportedly patched the same bug in CentOS Stream years earlier but the fix was not applied upstream, and one commenter questioned whether the headline&\#x27;s &\#x27;RCE chain&\#x27; characterization overstates the issue, since the bug is a double-free. Another commenter listed affected packages and asked whether apt is among them.

<details><summary>References</summary>
<ul>
<li>Critical GPGME Flaw CVE-2026-129975 - Aviatrix</li>
<li>GnuPG Warns Critical GPGME Flaw Could Expose App Data via ...</li>
<li>Fwd: GnuPG Security Advisory for GPGME (T8557,CVE-2026-129975)</li>

</ul>
</details>

**Tags**: `#security`, `#GPGME`, `#vulnerability`, `#double-free`, `#cryptography`

---

<a id="item-tech-news-5"></a>
### [Muru: Graham Dumpleton&\#x27;s AI-assisted Rust server for Python ASGI/WSGI](https://simonwillison.net/2026/Nov/21/muru/) ⭐️ 7.0/10

Graham Dumpleton, creator of mod\_wsgi, has started Muru, an AI-assisted Rust server for running Python ASGI and WSGI applications in development and production. The project is three weeks old and has been documented through 18 detailed public development posts since 2026-11-04, covering features such as HTTPS in development, combined WSGI/ASGI support, releases without restarts, canary deployments without a service mesh, Kubernetes integration, scaling to zero, and a per-page toolbar with tracing. Muru is still early-stage and not yet production-ready, but the public log provides unusually deep insight into its design and Dumpleton&\#x27;s 20 years of mod\_wsgi experience.

rss · Simon Willison · Nov 21, 23:56

**「Background」** Dumpleton created mod\_wsgi 20 years ago and has been thinking about the ideal way to serve Python web applications in production ever since. He previously published a similarly detailed development log for wrapture, another project. Muru builds on that experience, aiming to provide the best possible tools for running ASGI and WSGI apps.

**「Impact」** For Python web developers, Muru could eventually offer a Rust-based alternative to existing ASGI/WSGI servers, with built-in support for zero-downtime releases, canary deployments, and Kubernetes-native scaling. However, the project is only three weeks old and not yet mature, so developers should monitor the development log rather than adopt it for production.

**Tags**: `#Python`, `#Rust`, `#web servers`, `#ASGI`, `#developer tooling`

---

<a id="item-tech-news-6"></a>
### [Microsoft&\#x27;s RDMA over USB4 preview lets multiple PCs share one local AI model](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 7.0/10

Microsoft has released a developer preview of RDMA over USB4 for Windows, allowing multiple PCs to pool memory and GPU compute over standard USB4 connections to run a single local AI model without dedicated network cards or switches. In a demonstration, three AMD Ryzen AI Max+ 395 systems ran Qwen3-235B-A22B at 4-bit quantization at about 18.5 token/s. The feature will be distributed through Windows Insider, but it is a preview rather than a production-ready capability.

telegram · zaihuapd · Nov 21, 06:13

**「Background」** RDMA \(Remote Direct Memory Access\) is a networking technology that allows one computer to directly access another&\#x27;s memory without CPU involvement, and USB4 is a high-bandwidth connection standard; this developer preview applies RDMA over USB4 to Windows.

**「Impact」** For Windows users with USB4-capable PCs, this preview removes the need for specialized RDMA networking hardware to pool resources for local AI inference, but the demonstrated throughput \(~18.5 token/s\) and preview status mean it is not yet a production solution.

**Tags**: `#RDMA`, `#USB4`, `#distributed inference`, `#Windows`, `#local AI`

---

<a id="item-tech-news-7"></a>
### [OpenRouter warns MiniMax prompts may have been read by third parties](https://news.ycombinator.com/item?id=50585962) ⭐️ 7.0/10

OpenRouter warned users that prompts sent to MiniMax models may have been read by a third party. Security researchers sent prompts containing test URLs to MiniMax between July and October 2026, and those URLs were accessed by a third party 40 to 130 hours later. OpenRouter attributes the issue to MiniMax and its relays AtlasCloud, Novita, and StreamLake, and has removed the &quot;zero data retention&quot; labels from the affected endpoints. The warning was sent by email; OpenRouter has not published it on its website.

telegram · zaihuapd · Nov 21, 06:53

**「Background」** OpenRouter is an API gateway that routes developer prompts to AI models, including MiniMax, often through third-party forwarders such as AtlasCloud, Novita, and StreamLake. A common security-research technique is to embed unique test URLs in prompts and monitor whether those URLs are later fetched, which can reveal whether a provider or intermediary retains and accesses user data after processing.

**「Impact」** Developers who sent sensitive data to MiniMax through OpenRouter should rotate their API keys and passwords, since prompt contents may have been exposed. OpenRouter&\#x27;s removal of the zero-data-retention labels means those endpoints no longer carry the claim that data is not retained.

**Tags**: `#security`, `#AI privacy`, `#prompt injection`, `#OpenRouter`, `#MiniMax`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [To Code Well, Avoid Blunders](https://seangoedecke.com/to-code-well-avoid-blunders/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 22, 00:00

**「Background」** Sean Goedecke argues that many engineers treat programming as a hunt for brilliant insights, but the real skill is avoiding catastrophic mistakes. In large commercial codebases, one blunder can turn an elegant codebase into a janky one—unlike sports, where a mistake only costs a few points.

**「Solution」** The author identifies two cardinal sins: inconsistency and unnecessary requirements. Even a little inconsistency breaks trust, forcing engineers to hunt for surprises instead of assuming code works sensibly. Unnecessary requirements are sticky—they persist long after their context is gone—and interrelate in a combinatorial explosion that makes large codebases hard to work in. The remedy is to find where a task fits most normally into the existing codebase and trim it to the smallest set of requirements. Clever patterns are a warning sign of distraction from the main thing. The author notes that current coding agents are about as good as humans at consistency but far worse at avoiding unnecessary requirements.

**「Takeaway」** Good programming demands attention to detail and a laser focus on avoiding blunders, not cleverness—which can even be a disadvantage. The author limits this advice to large commercial codebases with big teams.

**Tags**: `#software engineering`, `#code quality`, `#technical debt`, `#consistency`, `#requirements management`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Trump proposes tax on U.S. firms building AI data centers abroad](https://apnews.com/article/trump-artificial-intelligence-data-centers-f1ac03b73d13445400eeed8631d9d879) ⭐️ 7.0/10

President Trump said on Nov. 20 he plans to impose a large tax on U.S. tech companies that build AI data centers overseas, aiming to keep the facilities in the U.S. and maintain an edge over China in AI.

telegram · zaihuapd · Nov 21, 03:26

**「Background」** The proposal follows local opposition to data centers over electricity use and noise, an issue that helped Republicans lose their House and Senate majorities in the November midterm elections.

**「Impact」** US technology companies that have built or plan to build AI data centers abroad would face a new tax burden if the proposal is enacted, potentially affecting their overseas expansion plans.

<details><summary>References</summary>
<ul>
<li><a href="https://www.abc.net.au/news/2026-11-21/trump-vows-tax-companies-building-data-centres-overseas/107412162">Donald Trump vows to tax US companies building data centres ...</a></li>
<li><a href="https://www.ibtimes.com/trump-tax-ai-data-centers-overseas-3810039">Trump Threatens &#x27;Tremendous Tax&#x27; On US Tech Firms Building AI ...</a></li>
<li><a href="https://www.politico.com/news/2026/11/20/trump-overseas-data-center-tax-01178999">Trump says he’ll tax companies building data centers outside ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#data centers`, `#tax policy`, `#Trump`, `#technology regulation`

---