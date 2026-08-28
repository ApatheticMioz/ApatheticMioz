<div align="center">

[![Profile Views](https://komarev.com/ghpvc/?username=ApatheticMioz&style=for-the-badge&color=bb9af7&label=Profile%20Views&cache=NONE)](https://github.com/ApatheticMioz)

</div>

<p align="center">
  <img src="assets/profile-header.svg" alt="Muhammad Abdullah Ali — AI/ML Systems Engineer" width="100%"/>
</p>

<div align="center">

[![Location](https://img.shields.io/badge/📍%20Islamabad%2C%20PK-0d1121?style=for-the-badge&labelColor=0d1121&color=7aa2f7)](#)
[![Education](https://img.shields.io/badge/🎓%20BS%20Data%20Science%20·%20FAST%20NUCES-0d1121?style=for-the-badge&labelColor=0d1121&color=bb9af7)](https://github.com/ApatheticMioz)
[![Role](https://img.shields.io/badge/💼%20Technical%20Lead%20·%20Data%20Precedes-0d1121?style=for-the-badge&labelColor=0d1121&color=f7768e)](#)
[![CGPA](https://img.shields.io/badge/🏅%20CGPA%203.73%2F4.00-0d1121?style=for-the-badge&labelColor=0d1121&color=e0af68)](#)
[![Status](https://img.shields.io/badge/🟢%20Open%20to%20Work%20·%20AI%2FEng%20Roles-0d1121?style=for-the-badge&labelColor=0d1121&color=9ece6a)](mailto:m.abdullah.ali.2523@gmail.com)

</div>

---

## 👋 Introduction

Hi — I'm **Muhammad Abdullah Ali**. I build the **infrastructure layer of applied AI**: quantized single-GPU LLM serving, geo-distributed retrieval pipelines over encrypted WAN meshes, and production multi-agent applications that ship to real users on real latency budgets.

Right now I'm a **Technical Lead on a 3-person AI team** at Data Precedes, where I architected a WhatsApp-first AI assistant (Next.js 16 · Mastra · Groq) with **sub-500ms webhook processing** and **620ms time-to-first-token**. I'm a BS Data Science student at **FAST-NUCES** (CGPA **3.73/4.00**, 6× Dean's List) who spends his nights pushing **245K-token context through a single RTX 3090** and auditing the literature for metric artifacts.

> **The one-line version:** I make expensive models cheap, distributed systems fast, and pipelines measurable — with numbers to prove it.

---

## 📈 Live Signals

| :---: | :---: |
| --- | --- |
| <a href="https://github.com/ApatheticMioz"><img src="https://github-readme-streak-stats.herokuapp.com/?user=ApatheticMioz&theme=tokyonight&background=0d1121&border=1a1b41&hide_border=false" alt="GitHub streak"/></a> | <a href="https://github.com/ApatheticMioz?tab=repositories"><img src="assets/language-chart.svg" alt="Language distribution across 30 public repositories"/></a> |

---

## 🎯 By The Numbers

<div align="left">

[![245K-token context](https://img.shields.io/badge/245K-token%20context%20on%201×%20RTX%203090-7aa2f7?style=flat-square&labelColor=0d1121)](#)
[![130 tok/s decode](https://img.shields.io/badge/130%20tok%2Fs%20decode%20·%20DFlash2-2ac3de?style=flat-square&labelColor=0d1121)](#)
[![36× TTFT speedup](https://img.shields.io/badge/36×%20TTFT%20speedup%20(4.7s%20vs%20169s)-bb9af7?style=flat-square&labelColor=0d1121)](#)
[![GSM8K 97.0%](https://img.shields.io/badge/GSM8K%2097.0%25%20at%20245K%20ctx-f7768e?style=flat-square&labelColor=0d1121)](#)

[![SWE-rebench 32.0%](https://img.shields.io/badge/SWE-rebench%2032.0%25%20best--of--1-9ece6a?style=flat-square&labelColor=0d1121)](#)
[![KVarN 4/2-bit KV](https://img.shields.io/badge/KVarN%204%2F2-bit%20KV%20cache%20·%205.26%20GiB-e0af68?style=flat-square&labelColor=0d1121)](#)
[![Sub-500ms webhook](https://img.shields.io/badge/Sub--500ms%20HMAC%20WhatsApp%20webhook-c678dd?style=flat-square&labelColor=0d1121)](#)
[![620ms TTFT](https://img.shields.io/badge/620ms%20TTFT%20·%20SSE%20streaming-ff9e64?style=flat-square&labelColor=0d1121)](#)

[![86.4% of 309 commits](https://img.shields.io/badge/86.4%25%20of%20309%20production%20commits-7aa2f7?style=flat-square&labelColor=0d1121)](#)
[![240× ETL speedup](https://img.shields.io/badge/240×%20ETL%20speedup%20·%2020min→5s-73daca?style=flat-square&labelColor=0d1121)](#)
[![15k records/s](https://img.shields.io/badge/15k%20records%2Fs%20HYBRIDJOIN%20DWH-9ece6a?style=flat-square&labelColor=0d1121)](#)
[![26-run ablation matrix](https://img.shields.io/badge/26-run%20paired%20ablation%20matrix-bb9af7?style=flat-square&labelColor=0d1121)](#)

</div>

---

## 🚀 Flagship Projects

### 🧠 Local LLM Serving & AVO Engine
<sub>vLLM · KVarN · DFlash2 · AutoRound · Node.js MCP · Goose · WSL2 — 🔒 code available on request</sub>

- **Single-GPU (RTX 3090 24 GB @ 250 W) serving recipe for Qwen3.8-27B** — W4A16 AutoRound weights, int8 heads/embeds, 2.7 GB vision tower stripped.
- **KVarN 4/2-bit KV cache → 245,760-token context in a 5.26 GiB pinned-memory budget**, verified byte-stable across `MAX_SEQS=2→8`.
- **DFlash2 speculative decoding: 130 tok/s decode** (up to 381 tok/s on structured reproduction, 32 tok/s at 112 k context) with **97.0% GSM8K** accuracy retained.
- **36× TTFT acceleration** (4.7 s vs. 169 s) on cached 100 k prefixes; production **Node.js MCP server suite** (`qwen_coworker`, `qwen_task`) bridging Claude Code / Antigravity orchestrators to local vLLM — long-poll wait server, disk-backed session resumption for KV reuse, 8-way concurrency semaphore.
- Validated end-to-end on **SWE-rebench** (50 post-cutoff issues): **32.0% resolved best-of-1**, 57.1% per-attempt within the 900 s budget — including patching 5 harness defects (one in upstream `eval.py`).

### 📱 Data Precedes AI Assistant — WhatsApp-First
<sub>Next.js 16 · React 19 · TypeScript · Mastra · Groq LLaMA 3.3 · Supabase · QStash · 🔒 code available on request</sub>

- **Led a 3-intern engineering team** as technical lead; **authored 86.4% of the repo's 309 commits**, architecting the core multi-agent service layer.
- **HMAC-verified WhatsApp Cloud API webhook with sub-500 ms processing**, queue-based deduplication, and parallel Groq Whisper STT — end-to-end voice turnaround under **4 s** with Opus synthesis and hallucination filtering.
- **3-agent Mastra orchestration with 429 auto-fallback hitting 620 ms TTFT over SSE**; 7-schedule QStash cron suite with per-user timezones.
- **768-dim embedding + centroid cosine-clustering memory engine** for recurring-task detection, universal dual-provider email ingestion (Gmail + Outlook Graph), and a **41-case evaluation harness** enforcing per-tier latency SLAs.

### 🌐 Geo-Distributed 3-Node Hybrid RAG Pipeline
<sub>Python · gRPC/Protobuf · FastAPI · AsyncIO · Tantivy BM25 · BGE-M3 (FP16) · Qdrant · WireGuard</sub> → [`ApatheticMioz/geo-distributed-hybrid-rag`](https://github.com/ApatheticMioz/geo-distributed-hybrid-rag)

- **Monolithic RAG decomposed into concurrent microservices over a WireGuard mesh**: Node C (async orchestrator with WAN-latency emulation) · Node A (dual HTTP/gRPC gateway) · Node B (dense retrieval worker).
- Node A fuses **Tantivy BM25 sparse + BGE-M3 dense retrieval** behind an `asyncio.Event` **160 ms barrier**, ranks via **Reciprocal Rank Fusion (k = 60)** with sparse-only fallback, and streams tokens over bidirectional gRPC.
- Node B runs **Qdrant gRPC ingestion with CUDA kernel warm-ups** to kill cold-start tail latency; automated TTFT profiling harness for the 2/3-node topology evolution.

### 🔬 Computational Pathology — Multi-Task U-Net & Metric Audit
<sub>PyTorch · Multi-Task U-Net · GradNorm · Macenko normalization · WandB · LaTeX</sub> → [`ApatheticMioz/cancer-pathology-dl`](https://github.com/ApatheticMioz/cancer-pathology-dl)

- **26-experiment reproducibility matrix** auditing joint **tumor classification (19 tissue types) + nuclear segmentation (5 categories)** against Rhanoui et al., *Onco* 2025, on H&E whole-slide imagery.
- **Shared-backbone multi-task U-Net with GradNorm dynamic loss balancing** that rescues collapsed baselines; paired ablations isolating gradient interference between macro-tumor and micro-glandular heads (<10 GB VRAM design target).
- **Original finding:** a literature-wide **metric-inflation artifact** in SIIM-ACR where **78% empty ground-truth masks** produce artificial **~99% Dice** via 0/0 edge cases — engineered isolated positive-mask evaluation protocols to expose true generalization.

---

## 🧩 Systems, Algorithms & Data (Public Labs)

| Repository | What's inside |
| :--- | :--- |
| [`hybridjoin-data-warehouse`](https://github.com/ApatheticMioz/hybridjoin-data-warehouse) | Near-real-time DWH: **HYBRIDJOIN stream-disk join, O(32 k) tuple memory, ~15 k records/s** on a 550 k-transaction dataset, 5-dimension star schema, producer→consumer→DB thread pipeline. |
| [`intelligent-cv-analyzer`](https://github.com/ApatheticMioz/intelligent-cv-analyzer) | FastAPI CV-screening engine implementing **Brute-Force / Rabin-Karp / KMP** string matching with live metric comparison; ranks candidates against 3 job profiles (KMP's O(n+m) wins for real-time screening). |
| [`shortest-path-algorithms-benchmark`](https://github.com/ApatheticMioz/shortest-path-algorithms-benchmark) | C++ benchmark suite: **Dijkstra vs A\* vs Bellman-Ford** with comparative profiling. |
| [`traffic-management-simulator-cpp`](https://github.com/ApatheticMioz/traffic-management-simulator-cpp) | Multi-threaded traffic-intersection simulator — **POSIX threads, mutexes, semaphores, IPC pipes**, deadlock-prevention analysis. |
| [`8086-pacman-adventure`](https://github.com/ApatheticMioz/8086-pacman-adventure) | Full **x86 MASM (Irvine32) game engine** — memory-mapped I/O, interrupt handlers, state machines at the register level. |
| [`cache-browser-sim-cpp`](https://github.com/ApatheticMioz/cache-browser-sim-cpp) | CPU cache simulator with **LRU/LFU replacement policies** and hit-ratio analytics. |
| [`disaster-resilience-analytics`](https://github.com/ApatheticMioz/disaster-resilience-analytics) | Fused **13 heterogeneous open-source datasets → 4,584 country-year records**; built DII / RRS / CRI composite resilience indices — and found the **Resilience Paradox**: governance quality (r = 0.78) out-predicts GDP per capita (r = 0.66). |
| [`pakistan-inflation-forecast`](https://github.com/ApatheticMioz/pakistan-inflation-forecast) | R time-series pipeline: **ARIMA / auto-ARIMA / regularized regression** (Elastic Net best) with full diagnostics. |

---

## 🛠️ Technical Arsenal

<div align="left">

**LLM Inference & Systems**
[![vLLM](https://img.shields.io/badge/vLLM-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![KVarN 4/2-bit](https://img.shields.io/badge/KVarN%204%2F2-bit-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![DFlash2](https://img.shields.io/badge/DFlash2%20Speculative%20Decoding-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![Quantization](https://img.shields.io/badge/AutoRound%2F%20GPTQ%20%2F%20AWQ-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![MCP](https://img.shields.io/badge/Model%20Context%20Protocol-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![Goose](https://img.shields.io/badge/Goose%20Agent%20Harness-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![gRPC](https://img.shields.io/badge/gRPC%20%2F%20Protobuf-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![AsyncIO](https://img.shields.io/badge/AsyncIO%20%2F%20FastAPI-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)
[![WireGuard](https://img.shields.io/badge/WireGuard-0d1121?style=flat-square&labelColor=1f2440&color=7aa2f7)](#)

**Machine Learning & Computer Vision**
[![PyTorch](https://img.shields.io/badge/PyTorch-0d1121?style=flat-square&labelColor=1f2440&color=9ece6a)](#)
[![Multi-Task U-Net](https://img.shields.io/badge/Multi--Task%20U--Net-0d1121?style=flat-square&labelColor=1f2440&color=9ece6a)](#)
[![GradNorm](https://img.shields.io/badge/GradNorm%20Loss%20Balancing-0d1121?style=flat-square&labelColor=1f2440&color=9ece6a)](#)
[![Hybrid RAG](https://img.shields.io/badge/BM25%2B%20Dense%20Hybrid%20RAG-0d1121?style=flat-square&labelColor=1f2440&color=9ece6a)](#)
[![BGE-M3](https://img.shields.io/badge/BGE--M3%20Embeddings-0d1121?style=flat-square&labelColor=1f2440&color=9ece6a)](#)
[![Qdrant](https://img.shields.io/badge/Qdrant%20gRPC-0d1121?style=flat-square&labelColor=1f2440&color=9ece6a)](#)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face%20%2F%20WandB-0d1121?style=flat-square&labelColor=1f2440&color=9ece6a)](#)

**Full-Stack & Orchestration**
[![TypeScript](https://img.shields.io/badge/TypeScript-0d1121?style=flat-square&labelColor=1f2440&color=ff9e64)](#)
[![Next.js 16](https://img.shields.io/badge/Next.js%2016%20%2F%20React%2019-0d1121?style=flat-square&labelColor=1f2440&color=ff9e64)](#)
[![Mastra](https://img.shields.io/badge/Mastra%20Multi--Agent-0d1121?style=flat-square&labelColor=1f2440&color=ff9e64)](#)
[![Drizzle](https://img.shields.io/badge/Drizzle%20ORM%20%2F%20Postgres-0d1121?style=flat-square&labelColor=1f2440&color=ff9e64)](#)
[![SSE](https://img.shields.io/badge/SSE%20Streaming-0d1121?style=flat-square&labelColor=1f2440&color=ff9e64)](#)
[![Java](https://img.shields.io/badge/Java%2023%20%2F%20Spring%20Boot-0d1121?style=flat-square&labelColor=1f2440&color=ff9e64)](#)

**Data Engineering & Analytics**
[![Python](https://img.shields.io/badge/Python%203-0d1121?style=flat-square&labelColor=1f2440&color=73daca)](#)
[![T-SQL](https://img.shields.io/badge/T--SQL%20%2F%20MySQL-0d1121?style=flat-square&labelColor=1f2440&color=73daca)](#)
[![Star Schema DWH](https://img.shields.io/badge/Star%20Schema%20DWH-0d1121?style=flat-square&labelColor=1f2440&color=73daca)](#)
[![ETL](https://img.shields.io/badge/ETL%20Optimization-0d1121?style=flat-square&labelColor=1f2440&color=73daca)](#)
[![Tableau](https://img.shields.io/badge/Tableau%20%2F%20D3.js-0d1121?style=flat-square&labelColor=1f2440&color=73daca)](#)

**Systems, Concurrency & Low-Level**
[![C++](https://img.shields.io/badge/C%2B%2B20%20%2F%2017-0d1121?style=flat-square&labelColor=1f2440&color=c678dd)](#)
[![POSIX](https://img.shields.io/badge/POSIX%20Threads%20%2F%20OpenMP%20%2F%20MPI-0d1121?style=flat-square&labelColor=1f2440&color=c678dd)](#)
[![x86 MASM](https://img.shields.io/badge/x86%20Assembly-0d1121?style=flat-square&labelColor=1f2440&color=c678dd)](#)
[![CUDA](https://img.shields.io/badge/CUDA-0d1121?style=flat-square&labelColor=1f2440&color=c678dd)](#)
[![Docker](https://img.shields.io/badge/Docker%20%2F%20WSL2-0d1121?style=flat-square&labelColor=1f2440&color=c678dd)](#)

</div>

---

## 🎓 Academic & Professional Leadership

- <b>Technical Lab Demonstrator — 5 consecutive semesters, FAST-NUCES</b> (Fall 2024 → present): Programming Fundamentals, OOP, COAL (8086), Database Systems, Data Analytics — **1,800+ curated teaching files** and automated evaluation pipelines for cohorts of 40–55 students per section.
- <b>Class Representative, BS Data Science</b> (Fall 2023 → present) — primary liaison between student body and administration.
- <b>FDSS — FAST Data Science Society</b>: built and maintained the society's web platform (Datathon registration, 31-member leadership grid, photo galleries).
- <b>Competition record:</b> NASCON 2025 (Speed Programming & Bug Catcher) · Devathon by Devsinc, Lahore · EDATHON EDA challenge — plus a maintained <b>C++ competitive programming suite</b> (DP, number theory, graph theory, two-pointers) and a **2100 peak Chess.com rapid rating** (A-Level Chess Club founder & president).
- <b>Honors:</b> Bronze Medalist (Fall 2025) · Medalist (Spring 2026, 3.94 SGPA) · **6× Dean's List** · CGPA 3.73/4.00, expected graduation Aug 2027.

---

## 💼 Experience Timeline

- <b>AI Intern — Technical Lead · Data Precedes Inc.</b> <i>(Jun 2026 – present, Remote/Toronto)</i> — lead of 3-intern team; 86.4% of 309 commits; sub-500 ms webhook, 620 ms TTFT, 41-case eval harness.
- <b>Data Engineering Intern · Octopus Digital (Avanceon), ML Solutions</b> <i>(Jun – Aug 2025, Lahore)</i> — re-engineered a core ETL flow from **~20 min → ~5 s (99.6% latency reduction, 240×)**; refactored 7+ production Python/T-SQL pipelines; negotiated data contracts between warehouse and ML feature pipelines.
- <b>Technical Lab Demonstrator · FAST-NUCES</b> <i>(Fall 2024 – present)</i> — paid teaching role across 5 courses, ~100+ contact hours.
- <b>Freelance 3D Artist</b> <i>(ongoing)</i> — Blender / Premiere / Photoshop; paid 3D modeling for game developers + independent animation work.

---

## 🔗 Connect

<div align="left">

[![GitHub](https://img.shields.io/badge/GitHub-@ApatheticMioz-565f89?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ApatheticMioz)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-M.%20Abdullah%20Ali-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/muhammad-abdullah-ali-71a528202/)
[![Email](https://img.shields.io/badge/m.abdullah.ali.2523@gmail.com-7aa2f7?style=for-the-badge&logo=gmail&logoColor=white)](mailto:m.abdullah.ali.2523@gmail.com)
[![Trello Portfolio](https://img.shields.io/badge/Trello-Portfolio%20Board-0052CC?style=for-the-badge&logo=trello&logoColor=white)](https://trello.com/b/vhoXbQvi/apatheticmioz-portfolio)
[![YouTube](https://img.shields.io/badge/YouTube-@apatheticmioz-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@apatheticmioz)

</div>

---

<div align="center">

<sub>Curious about the serving recipes, RAG architecture, or the pathology audit? <b><a href="mailto:m.abdullah.ali.2523@gmail.com?subject=Profile%20reach%20out">Reach out</a></b> — private codebases are shared with serious collaborators and recruiters.</sub>

<sub>🛠️ Hand-built with Markdown, shields.io, and home-rolled animated SVG — every number on this page is benchmarked, not estimated.</sub>

</div>
