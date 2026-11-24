---
layout: default
title: "Horizon Summary: 2026-11-24 (EN)"
date: 2026-11-24
lang: en
---

> From 38 items, 15 important content pieces were selected

---

**Technology News**
1. [Nvidia Reinstates Jensen Huang as CEO After Brief Removal](#item-tech-news-1) ⭐️ 8.0/10
2. [Ladybird browser reaches alpha with installable builds](#item-tech-news-2) ⭐️ 8.0/10
3. [GLM-5.4 debuts loop transformer architecture with coding plan access](#item-tech-news-3) ⭐️ 8.0/10
4. [ARM documentation site to shut down after Arm&\#x27;s trademark request](#item-tech-news-4) ⭐️ 7.0/10
5. [NariQ quantizes Qwen3.8-27B to 3-bit with near-BF16 agentic scores](#item-tech-news-5) ⭐️ 7.0/10
6. [Codex2api supply chain attack: backdoored releases v3.1.10–3.1.12](#item-tech-news-6) ⭐️ 7.0/10
7. [AI Lean proof of Riemann Hypothesis exposed as vacuous](#item-tech-news-7) ⭐️ 7.0/10
8. [Shenzhou-24 set for Nov 25 launch with first international crew member](#item-tech-news-8) ⭐️ 7.0/10

**Technology Blog**
1. [ERNIE 5.5 Flash Preview: Day-0 vLLM Plugin and Inference Acceleration](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [Fed&\#x27;s Williams signals more rate hikes ahead to tame inflation](#item-finance-news-1) ⭐️ 7.0/10
2. [Anthropic IPO Triggers AI Selloff, Clouding Chinese Tech Listings](#item-finance-news-2) ⭐️ 7.0/10
3. [Shanghai subway fares rise for first time in 21 years](#item-finance-news-3) ⭐️ 7.0/10
4. [SpaceX rents AI compute to Anthropic, Google for billions monthly](#item-finance-news-4) ⭐️ 7.0/10
5. [Tens of thousands of EU firms petition EU to investigate Apple&\#x27;s iPhone browser limits](#item-finance-news-5) ⭐️ 7.0/10
6. [Singapore Won&\#x27;t Be a Conduit for Chip Export Evasion, PM Says](#item-finance-news-6) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Nvidia Reinstates Jensen Huang as CEO After Brief Removal](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 8.0/10

Nvidia&\#x27;s board has reinstated Jensen Huang as CEO after a brief removal, following input from senior U.S. government officials who concluded his reinstatement poses no national security risk. The board&\#x27;s statement said it received input from senior levels of the U.S. government and is confident that Mr. Huang&\#x27;s reinstatement poses no national security risk. The decision restores Huang to leadership of the AI chip maker after an unusual corporate governance episode that drew government involvement.

hackernews · jaz · Nov 23, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50611576)

**「Prior board action」** Less than two weeks before this announcement, Nvidia&\#x27;s board had removed Jensen Huang as CEO; the board then reversed course after receiving input from senior U.S. government officials, saying it was confident the reinstatement poses no national security risk.

**「Impact on enterprise AI strategy」** The reinstatement may calm immediate concerns about Nvidia&\#x27;s leadership, but it does not reverse enterprise efforts to build alternatives into their AI infrastructure strategy, according to commentary cited by Yahoo Finance. Nvidia employees gave Huang a hero&\#x27;s reception at the company&\#x27;s Santa Clara headquarters as he returned.

**「Community Discussion」** Commenters debated whether the reinstatement reflects government pressure or a lack of evidence, with one noting the board&\#x27;s unanimous reversal in under two weeks and another arguing that the Delaware Caremark standard plus a DoJ decision not to prosecute would shield board members from individual liability. One commenter compared the episode to the 2023 OpenAI saga, arguing that a firm&\#x27;s nominal governance structure isn&\#x27;t necessarily its real governance structure.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.yahoo.com/markets/stocks/live/nvidia-live-updates-jensen-huang-reinstated-as-ceo-trump-says-no-reason-to-believe-huang-a-national-security-risk-152429808.html">Nvidia live updates: Jensen Huang reinstated as CEO; Trump says...</a></li>
<li><a href="https://wccftech.com/nvidia-employees-give-reinstated-ceo-jensen-a-heros-reception-at-endeavor-hq/">NVIDIA Employees Give Reinstated CEO, Jensen ...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#AI chips`, `#semiconductors`

---

<a id="item-tech-news-2"></a>
### [Ladybird browser reaches alpha with installable builds](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird released its first alpha on November 23, 2026, making the from-scratch browser installable on macOS and Linux without compiling. The engine implements its own HTML parsing, CSS engine, layout, JavaScript, and WebAssembly, while relying on external components such as HarfBuzz, Skia, ffmpeg, and SQLite. In October, the project gained 75,650 new web-platform-tests passes, overtaking Safari, and a new Cranelift WebAssembly engine delivered a 7x boost on the JetStream 3 WASM benchmark. The alpha is not yet a daily driver: some sites fail and crashes are expected, as with the reported Datasette Lite error caused by a missing \`navigator.serviceWorker.startMessages\` implementation.

hackernews · janvdberg · Nov 23, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50614249)

**「Background」** Ladybird began as the browser of SerenityOS, an ambitious from-scratch operating system project, and split into its own project to build a browser independent of any OS. In February 2026, the project adopted Rust with AI assistance, porting 25,000 lines of its LibJS JavaScript engine from C++ to Rust in two weeks using Claude Code and Codex. The October 2026 newsletter documented the WPT gains and the new JavaScript JIT that preceded this alpha.

**「Impact」** Users can now install Ladybird on macOS or Linux without building it from source, but should expect crashes and broken sites; the project asks users to report broken sites from inside the browser and to review crash reports before sending them. Developers testing complex service-worker-based apps may hit missing APIs, as with Datasette Lite&\#x27;s \`navigator.serviceWorker.startMessages\` error.

**「Community Discussion」** Testers reported that most sites rendered correctly, with one noting &quot;every single one of them rendered correctly&quot; and another finding NoVNC snappier than in Firefox, though jerky scrolling was a minor complaint. Commenters also raised forward-looking concerns: one hoped Ladybird would address fingerprinting with a non-compliant JS mode, another asked what precautions users should take during alpha, and one expressed nostalgia for the original SerenityOS hacker spirit while acknowledging that adopting production-grade libraries like Skia and SQLite helped.

**Tags**: `#browser`, `#open source`, `#software engineering`, `#alpha release`, `#web standards`

---

<a id="item-tech-news-3"></a>
### [GLM-5.4 debuts loop transformer architecture with coding plan access](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

Z.ai has released GLM-5.4, its first model using a looped transformer architecture that runs weight-shared layers multiple times per forward pass, enabling deeper computation without increasing parameter count. The model is available only through the Coding Plan subscription, not the regular API or OpenRouter, and is not open weights. Simon Willison&\#x27;s pelican tests show GLM-5.4 output is similar to GLM-5.3 but notably different from the distinctive styles of GLM-5.1 and 5.2.

hackernews · foohis · Nov 23, 10:06 · [Discussion](https://news.ycombinator.com/item?id=50609685)

**「Background」** A loop transformer reuses a weight-shared group of layers for multiple iterations per token, refining hidden states from the previous pass to deepen the network without adding parameters. Thinking Machines Lab&\#x27;s Inkling 2 Mini, released on November 20, 2026, already used this design, running its middle layers three times per token for agentic coding. GLM-5.4 is Zhipu AI&\#x27;s first model to adopt the looped architecture, following the GLM-5.1, 5.2, and 5.3 generations.

**「Impact」** Developers cannot access GLM-5.4 through the standard Z.ai API or OpenRouter; access requires a Z.ai Coding Plan subscription, which provides API keys that work with the same OpenAI-compatible Responses API endpoint. The model runs a shared 28-layer block twice, which Z.ai claims delivers reasoning depth comparable to 2T–3T parameter models, but the author&\#x27;s pelican tests show output quality similar to GLM-5.3.

**「Community Discussion」** Commenters noted that GLM-5.4 requires a Coding Plan subscription for API access, and one user reported that the model&\#x27;s &\#x27;marathon thinking&\#x27; sessions make it slow on simple tasks despite strong benchmark performance. Another commenter praised Zhipu&\#x27;s technical transparency, while one explained that loop transformers address memory bandwidth bottlenecks by reusing weights across iterations.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.z.ai/guides/llm/glm-5.4">GLM - 5 . 4 - Overview - Z. AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://anyrouter.dev/model/z-ai/glm-5.4">GLM - 5 . 4 · Zhipu AI · pricing &amp; API · AnyRouter</a></li>
<li><a href="https://www.youtube.com/watch?v=G6-3js4jjTo">GLM - 5 . 4 Beat Opus 5.5? - YouTube</a></li>

</ul>
</details>

**Tags**: `#GLM-5.4`, `#loop transformer`, `#Zhipu AI`, `#LLM architecture`, `#coding`

---

<a id="item-tech-news-4"></a>
### [ARM documentation site to shut down after Arm&\#x27;s trademark request](https://arm.jonpalmisc.com/) ⭐️ 7.0/10

The ARM architecture documentation site arm.jonpalmisc.com is scheduled to be discontinued on 4 December 2026 after Arm requested removal, citing trademark and IP concerns. Site owner jonpalmisc said Arm claims hosting their documentation constitutes use of their trademarks and IP, and he is considering mirrors, legal advice, or releasing source code without Arm IP. The site will remain available until the shutdown date.

hackernews · tech234a · Nov 23, 19:17 · [Discussion](https://news.ycombinator.com/item?id=50617499)

**「Background」** Jon&\#x27;s Arm Reference is a community-maintained site that documents AArch64 instructions and system registers, built from Arm&\#x27;s publicly available documentation. Arm&\#x27;s lawyers have notified the site&\#x27;s creator, Jon, to remove the content or face legal action, citing trademark and IP concerns, leading to the announced shutdown on December 4, 2026.

**「Impact」** Developers who used arm.jonpalmisc.com as a reference for ARM architecture documentation will lose access to the site on 4 December 2026. The site owner said he is exploring mirror hosting and other options, but no replacement has been announced.

**「Community discussion」** Commenters questioned the legal basis, with ethin noting that Arm&\#x27;s machine-readable specification \(MRAS\) appears to be BSD-licensed, and fweimer observing that the site&\#x27;s content resembles a Stanford-hosted page possibly generated by the same conversion tool. Site owner jonpalmisc said he is considering mirrors, legal advice, or releasing source code without Arm IP.

<details><summary>References</summary>
<ul>
<li><a href="https://arm.jonpalmisc.com/">Jon&#x27;s Arm Reference</a></li>
<li><a href="https://news.lavx.hu/article/jon-s-arm-reference-to-shut-down-dec-4-after-arm-legal-request">Jon&#x27;s Arm Reference to Shut Down Dec. 4 After Arm Legal ...</a></li>

</ul>
</details>

**Tags**: `#ARM`, `#documentation`, `#trademark`, `#legal`, `#developer resources`

---

<a id="item-tech-news-5"></a>
### [NariQ quantizes Qwen3.8-27B to 3-bit with near-BF16 agentic scores](https://huggingface.co/nari-labs/Qwen3.8-27B-NariQ-GGUF) ⭐️ 7.0/10

NariQ introduces 3-bit-or-lower quantizations of Qwen3.8-27B that reportedly retain near-BF16 quality on long-horizon agentic tasks, math, multilingual reasoning, and image understanding, with a ~10 GB file. The reported benchmarks \(BF16 / 3-bit / 2.5-bit / 2-bit\) include DeepSWE 39.8/41.0/41.9/28.6, Terminal-Bench 2.1 62.6/63.8/60.2/52.4, AIME 25+26 97.7/98.3/96.5/86.0, MSGM 94.0/93.1/91.8/90.6, and RealWorldQA 82.4/82.4/81.3/80.9. The authors claim this is the first 3-bit-or-lower quantization to retain BF16-level performance on long-horizon agentic tasks, but running these quants currently requires their custom llama.cpp fork \(nari-labs/nari-llama.cpp\), and the results are not independently verified.

hackernews · toebee · Nov 23, 13:42 · [Discussion](https://news.ycombinator.com/item?id=50611402)

**「Background」** Quantization compresses model weights from their original BF16 \(16-bit floating-point\) representation to fewer bits, reducing memory footprint at the cost of some precision. Qwen3.8-27B is a 27B-parameter model; NariQ applies 3-bit-or-lower quantization to it and reports near-BF16 performance across agentic, math, multilingual, and vision benchmarks.

**「Impact」** For self-hosted users, the concrete consequence is a 27B-class model in a ~10 GB file, but the benefit is conditional: the quants require the nari-llama.cpp fork, and on an Apple M3 Pro \(18 GB\) Metal decode is reported at about 3.8 tok/s with the 3.0bpw file \(4.9 tok/s with 2.0bpw\), far slower than CUDA. Benchmark gains may also partly reflect harness differences rather than the model, so users should verify on their own workloads.

**「Community Discussion」** Commenters were cautiously positive but divided: rao-v appreciated the multiple long-horizon task types and &\#x27;held out&\#x27; mentions but remained skeptical of benchmark overfitting, while WithinReason argued most gains come from a different harness, not the model. jedbrooke asked about 16GB Macs and Bonsai 2 27B comparisons after noting the M3 Pro Metal decode speed, and Retro\_Dev asked what information is actually lost as file size shrinks.

**Tags**: `#quantization`, `#LLM`, `#Qwen`, `#agentic AI`, `#model compression`

---

<a id="item-tech-news-6"></a>
### [Codex2api supply chain attack: backdoored releases v3.1.10–3.1.12](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 7.0/10

Codex2api&\#x27;s author account was compromised, and the attacker pushed tags that bypassed the main branch to build backdoored releases v3.1.10–3.1.12. Version 3.1.11 removed authentication, enabling passwordless remote code execution, and a workflow exfiltrated 16 GitHub Actions secrets affecting at least 21 repositories. Users who installed or updated to these versions should immediately disable the service, roll back to 3.1.9, and rotate all related keys \(GitHub tokens, SSH keys, database and DeepSeek credentials\). The advisory comes from a Telegram community post referencing an original incident report, so the details are not independently confirmed.

telegram · zaihuapd · Nov 23, 11:21

**「How the attack worked」** Codex2api is distributed through GitHub Releases built by a GitHub Actions workflow. The attacker compromised the author&\#x27;s account and pushed tags directly, bypassing the main branch, which triggered the release pipeline to build and publish the backdoored versions 3.1.10–3.1.12.

**「Impact」** Affected users must treat any deployment of v3.1.10–3.1.12 as compromised: stop the service, roll back to 3.1.9, and rotate GitHub tokens, SSH keys, database credentials, and DeepSeek keys, because the exfiltrated Actions secrets may allow continued access to the 21 affected repositories.

**Tags**: `#supply-chain-attack`, `#security`, `#codex2api`, `#github-actions`, `#incident-response`

---

<a id="item-tech-news-7"></a>
### [AI Lean proof of Riemann Hypothesis exposed as vacuous](https://x.com/i/web/status/2124987173439209561) ⭐️ 7.0/10

A claimed AI-generated Lean proof of the Riemann Hypothesis by Alpöge and the AI model Claude has been exposed as vacuous. The authors published 17 million lines of Lean code across 175,000 files with no human-readable proof, and the Lean/Mathlib community initially said it had &quot;full confidence&quot; the code proved the claim. Researchers then found key definitions written as tautologies and geometric conditions meaningless, and on November 23 Alpöge admitted the 250,000-page claim was &quot;a joke&quot; and the code is &quot;full of garbage but compiles,&quot; calling the criticism completely reasonable.

telegram · zaihuapd · Nov 24, 01:29

**「Background」** Levent Alpöge&\#x27;s November 2026 announcement claimed a proof of the Riemann hypothesis found with the AI system Claude, but the argument exists only as a formal proof in the Lean proof assistant, about 17 million lines long, with no human-readable paper \(tool-1-2, tool-1-3\). Lean is a proof assistant that checks each step of a proof, so the claim&\#x27;s validity depends on the definitions and statements encoded in those lines \(tool-1-3\).

**「AI-generated Lean proofs still require human review」** For mathematicians and formal-verification practitioners, the episode shows that a Lean proof passing the kernel does not guarantee a meaningful theorem: the vacuous definitions compiled, so type-checking alone failed to catch the flaw. This shifts the verification burden back to human reviewers, who must inspect statements and definitions for hidden gaps—a risk already documented for AI-generated Lean proofs \(tool-3-1, tool-3-3\). Institutions relying on AI-generated formal proofs as a substitute for human peer review remain exposed to undetected logical errors \(tool-3-3\).

<details><summary>References</summary>
<ul>
<li><a href="https://math.uwaterloo.ca/~mrubinst/alpoge_claude_grh/zeta-paper.pdf">The Alpoge - Claude proof of the Riemann hypothesis explained for...</a></li>
<li><a href="https://www.cryptopolitan.com/alpoge-claude-riemann-hypothesis-proof/">Anthropic&#x27;s Alpöge says Claude helped him prove the Riemann ...</a></li>
<li><a href="https://mathoverflow.net/questions/513540/should-we-trust-ai-generated-formal-proofs-in-lean-4">Should we trust AI-generated formal proofs in Lean 4?</a></li>
<li><a href="https://gridthegrey.com/posts/openai-lean-proof-mistranslation-exposes-ai-verification-risk/">OpenAI Lean Proof Mistranslation Exposes AI Verification Risk</a></li>

</ul>
</details>

**Tags**: `#AI proof`, `#Lean`, `#formal verification`, `#Riemann Hypothesis`, `#mathematics`

---

<a id="item-tech-news-8"></a>
### [Shenzhou-24 set for Nov 25 launch with first international crew member](https://www.news.cn/20261124/3b116eb35c404cd7b897b23a50099b5b/c.html) ⭐️ 7.0/10

China&\#x27;s Shenzhou-24 mission is scheduled to launch on November 25 at 8:18 AM Beijing time from Jiuquan, carrying the first international crew member to visit the Tiangong space station. The crew consists of commander Tang Hongbo, Wu Yi, and Pakistani astronaut Muhammad Zeeshan Ali, who will become the first foreign astronaut aboard Tiangong. The spacecraft will use a 3.5-hour autonomous fast rendezvous and docking profile to the forward port of the Tianhe core module.

telegram · zaihuapd · Nov 24, 04:08

**「Background」** China&\#x27;s Tiangong space station has been crewed by rotating Shenzhou missions, with the Tianhe core module serving as the primary habitat. Shenzhou-24 continues this rotation, but with a crew that for the first time includes a non-Chinese astronaut.

**「Impact」** The mission establishes a precedent for international crew participation on Tiangong, and the Pakistani astronaut&\#x27;s flight is a concrete step in China&\#x27;s bilateral space cooperation with Pakistan.

**Tags**: `#spaceflight`, `#aerospace`, `#China space program`, `#international cooperation`, `#Tiangong`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [ERNIE 5.5 Flash Preview: Day-0 vLLM Plugin and Inference Acceleration](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 7.0/10

rss · vLLM Blog · Nov 24, 00:00

**「Background」** ERNIE 5.5 Flash Preview is a 280B-parameter sparse MoE model with only 14B active per token and a 1M-token context, designed from the start around inference cost. Its new attention, MoE, and output-head structures, however, would pay heavily in memory traffic and kernel launches if implemented op by op, and the team wanted day-0 support in vLLM without maintaining a fork.

**「Solution」** The authors redesigned each new structure around a dedicated fused kernel. VHA cross-head mixing is pre-folded into a single matrix at load time with FP8 quantization fused in registers; all router weights are concatenated so one GEMM produces every router&\#x27;s logits, followed by a fused routing chain; the MultiMax output head merges its four pieces into a single pass that is bitwise identical to the term-by-term version; and gated attention fuses the gate projection and sigmoid gating. These fusions run 1.55× to 6.53× faster than naive implementations. FlashIndexer adds a small head router that selects sparse indexer heads per token, plus threshold pre-filtering, yielding a 1.4× speedup at 1M context. W4A8 quantization-aware training matches inference numerics exactly, and a multi-stage DSpark training pipeline produces a draft model with mean acceptance length above 4.0 on coding and agent workloads. The vLLM-ERNIE plugin registers architectures through the vllm.general\_plugins entrypoint, so the official vllm==0.32.0 wheel works unchanged, with prefix caching, chunked prefill, CUDA graphs, and PD disaggregation all functioning out of the box.

**「Takeaway」** The article&\#x27;s core point is that inference-oriented architecture design, combined with a plugin-based integration path, lets a new model ship on vLLM&\#x27;s release day without a fork while still achieving large speedups from kernel fusion, quantization, and speculative decoding. This makes plugin-based model support a practical template for future architectures.

**Tags**: `#vLLM plugin`, `#MoE inference`, `#kernel fusion`, `#quantization-aware training`, `#speculative decoding`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed&\#x27;s Williams signals more rate hikes ahead to tame inflation](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

New York Fed President John Williams said Monday the Federal Reserve must raise interest rates further over time to bring inflation back to its 2% target, which he expects to reach in 2028. Markets are fully pricing in a quarter-point increase at the Fed&\#x27;s Dec. 8-9 meeting, which would lift the target range from 3.75%-4% to 4%-4.25%.

rss · CNBC Finance · Nov 23, 21:02

**「Background」** Williams attributed current price pressures to the conflict in Iran, demand tied to the AI build-out, and tariffs, whose effects he said have largely abated, and said monetary policy cannot reopen pipelines or refineries but must ensure such shocks do not lead to persistent inflation.

**「Impact」** Markets expect the Fed to raise rates by a quarter point at its Dec. 8-9 meeting, which would raise borrowing costs for households and businesses with variable-rate loans as the target range moves to 4%-4.25%.

**Tags**: `#Federal Reserve`, `#Monetary Policy`, `#Inflation`, `#Interest Rates`, `#John Williams`

---

<a id="item-finance-news-2"></a>
### [Anthropic IPO Triggers AI Selloff, Clouding Chinese Tech Listings](https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo) ⭐️ 7.0/10

Anthropic&\#x27;s record $119.5 billion IPO triggered a global AI selloff that has erased $1.7 trillion from Chinese tech stocks since end-June, according to Bloomberg.

telegram · zaihuapd · Nov 23, 09:31

**「Background」** Anthropic rose 17% on debut to a $1.8 trillion market value, then fell 8.5% the next day; Zhipu is down over 85% from its June high after a 2,000% six-month gain, and MiniMax has slipped below its IPO price.

**「Impact」** The selloff has clouded IPO plans at DeepSeek, Moonshot, and StepFun, which are preparing or considering share offerings.

**Tags**: `#AI stocks`, `#IPO`, `#market selloff`, `#Chinese tech`, `#Anthropic`

---

<a id="item-finance-news-3"></a>
### [Shanghai subway fares rise for first time in 21 years](https://weibo.com/1699432410/5368461393397183) ⭐️ 7.0/10

Shanghai will raise subway fares for the first time in 21 years, with a starting fare of 3 yuan for rides up to 4 km, effective Dec 1, according to Xinhua.

telegram · zaihuapd · Nov 23, 10:45

**「Background」** The previous fare structure had been unchanged for 21 years; the new multi-ride tickets and monthly discount are aimed at reducing the impact on frequent riders.

**「Impact」** The fare increase affects Shanghai commuters, while multi-ride tickets and a 10% discount after 90 yuan of monthly spending are designed to ease the burden on frequent riders.

**Tags**: `#Shanghai`, `#subway fare`, `#public transport`, `#cost of living`, `#policy`

---

<a id="item-finance-news-4"></a>
### [SpaceX rents AI compute to Anthropic, Google for billions monthly](https://www.nytimes.com/2026/11/23/business/elon-musk-ai-anthropic-google.html) ⭐️ 7.0/10

SpaceX has been renting out compute capacity from its data centers to Anthropic and Google since May, earning billions of dollars per month, according to a New York Times report citing three unnamed sources. Musk reportedly told employees the company&\#x27;s AI efforts lag and that renting compute is more profitable than using it.

telegram · zaihuapd · Nov 24, 02:06

**「Background」** SpaceX has rented out data-center compute—processing power for AI training—to Anthropic and Google since May, after Musk said its own AI effort lagged, and has signed binding deals worth $81.3B \(per the AI Compute Deal Ledger\).

**「Impact」** Google has agreed to pay about $920 million a month for roughly 110,000 NVIDIA GPUs at SpaceX data centers under a 33-month deal, which Google described as bridge capacity to meet unexpectedly high demand for Gemini Enterprise, its agentic AI platform.

<details><summary>References</summary>
<ul>
<li><a href="https://www.regardsofwallstreet.com/data/ai-deals/entity/spacex">SpaceX AI Compute Deals: $81.3B in Binding... | Regards of Wallstreet</a></li>
<li><a href="https://www.linkedin.com/posts/abhinav-pabba-b383312a0_ai-genai-agenticai-activity-7469101321921634305-Arq6">Google pays SpaceX $920M/month for GPU access | LinkedIn</a></li>
<li><a href="https://theagenttimes.com/articles/google-commits-920-million-monthly-to-rent-spacex-gpu-capaci-0e9b00b9">Google Commits $920 Million Monthly to Rent SpaceX GPU Capacity...</a></li>
<li><a href="https://getaibook.com/news/gemini-enterprise-demand-drives-30b-spacex-gpu-contract/">Gemini Enterprise Demand Drives $30B SpaceX GPU Contract | News</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#AI compute`, `#Elon Musk`, `#Anthropic`, `#Google`

---

<a id="item-finance-news-5"></a>
### [Tens of thousands of EU firms petition EU to investigate Apple&\#x27;s iPhone browser limits](https://appleinsider.com/articles/26/11/23/eu-urges-to-challenge-apples-grip-on-iphone-browsers?utm_source=rss) ⭐️ 7.0/10

A coalition of about 45,000 to 55,000 EU companies and organizations, including Mozilla and Shopify, has petitioned the European Commission to investigate Apple&\#x27;s iPhone browser restrictions under the Digital Markets Act. The coalition estimates that if half of native iOS apps moved to the web, EU businesses could save €11 billion a year in development costs.

telegram · zaihuapd · Nov 24, 03:02

**「Background」** Under the EU Digital Markets Act, Apple began allowing alternative browser engines on iOS in the EU, but its published conditions still make it impractical for companies like Mozilla to bring their own engine, and every iPhone browser is still required to run Apple&\#x27;s WebKit rendering engine.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.mozilla.org/en/mozilla/internet-policy/apple-ios-browser-engine-rules/">Why there are still no non-WebKit browsers on iOS | The ...</a></li>
<li><a href="https://apple.gadgethacks.com/news/ios-browser-performance-webkit-rules-what-apples-engine-requirement-actually-means/">iOS Browser Performance WebKit Rules: What Apple&#x27;s Engine ...</a></li>

</ul>
</details>

**Tags**: `#EU regulation`, `#Apple`, `#Digital Markets Act`, `#Tech policy`, `#App economy`

---

<a id="item-finance-news-6"></a>
### [Singapore Won&\#x27;t Be a Conduit for Chip Export Evasion, PM Says](https://www.bloomberg.com/news/articles/2026-11-24/singapore-won-t-be-conduit-to-skirt-us-chip-curbs-wong-says) ⭐️ 7.0/10

Singapore&\#x27;s Prime Minister Lawrence Wong said the city-state will not be used as a conduit to evade U.S. chip export controls. The U.S. Commerce Department blacklisted Megaspeed and six other Southeast Asian firms, including Alibaba&\#x27;s Singapore subsidiary Apex Enterprise Solutions, for a &\#x27;significant risk&\#x27; of transferring advanced computing products to unauthorized users.

telegram · zaihuapd · Nov 24, 05:03

**「Background」** On Nov. 23, the U.S. Commerce Department added Singapore-based Megaspeed and six other Southeast Asian firms, including Alibaba&\#x27;s Singapore subsidiary Apex Enterprise Solutions, to its trade blacklist over the risk of diverting advanced computing products to unauthorized users, according to Reuters and The Straits Times. The action came amid a probe into suspected Nvidia AI chip diversions to China.

**「Impact」** The blacklisting and Singapore&\#x27;s pledge raise compliance and licensing risks for Singapore-based chip distributors, data centers, and logistics firms handling advanced AI chips, as US rules now cover rented GPUs and transshipment hubs like Singapore and Malaysia.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/business/us-blacklist-megaspeed-chip-firm-linked-nvidia-scandal-source-says-2026-11-23/">US blacklists Alibaba subsidiary and Megaspeed linked to ...</a></li>
<li><a href="https://www.straitstimes.com/world/united-states/us-blacklists-megaspeed-chip-firm-linked-to-nvidia-scandal">US blacklists Megaspeed, Alibaba unit amid Nvidia scandal ...</a></li>
<li><a href="https://hwbusters.com/news/ai-chip-export-controls-now-reach-rented-gpus-and-malaysia-and-singapore-need-a-license/">AI Chip Export Controls Now Reach Rented GPUs, and Malaysia and...</a></li>

</ul>
</details>

**Tags**: `#export controls`, `#semiconductors`, `#Singapore`, `#US-China tech`, `#trade policy`

---