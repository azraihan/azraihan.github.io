---
layout: page
title: Intent-Based Multilingual Search
# description: "Champions · AI Engineering Hackathon · Poridhi.io × Brain Station 23"
img: assets/img/poridhi1.jpg
importance: 2
category: research
related_publications: false
---

<div style="margin-bottom: 1.5rem;">
  <code><span style="color:#f59e0b;">●</span> Champions</code>
  &nbsp;
  <code>National · 86 Teams · 300+ Participants</code>
  &nbsp;
  <code>AI Hackathon</code>
</div>

## Overview

**[Poridhi.io](https://poridhi.io/)** × **[Brain Station 23](https://brainstation-23.com/)** organized one of Bangladesh's most competitive **AI Engineering Hackathons** — open to professionals and students alike — with 86 teams and 300+ participants nationwide.

***The challenge:*** push the boundaries of **`intent-based search`**, balancing precision, performance, and scalability with a robust, production-grade deployment pipeline. Each team was allocated 40 VMs with 80 GB VRAM on AWS. Judging covered the full AI engineering stack: embedding optimization, architectural decisions (RAG vs. agentic workflows), cost and latency reduction, monitoring and observability, and resilient deployment. Full problem statement [here]({{ '/assets/pdf/Rulebook-and-Problem-statement-for-hackathon-2025.pdf' | relative_url }}){:target="_blank"}.

---

## Technical Challenge

The problem demanded engineering across the full AI systems stack: from fine-tuning embedding models and architecting resilient search infrastructure, to choosing between **`retrieval-augmented generation`** and agentic workflows, pushing **`LLM efficiency`** to the limit on constrained hardware, and building real-time observability into the pipeline.

Every other team used the allocated GPU resources. We chose not to. We ran the entire system on 20 VMs (2 vCPU, 2 GB RAM each) — CPU only, no GPU anywhere in the pipeline — while still hitting sub-500ms average response latency with full multilingual support and high availability.

Every architectural choice — which retrieval paradigm to commit to, how aggressively to quantize, where to place the index — had a direct cost in latency or memory.

---

## Our Approach

- **In-memory LLM inference via llama's C++ runtime** — the core of the system. We ran quantized language models entirely in CPU memory, with custom modifications to the inference path to cut per-token latency. No GPU, yet the model retained the semantic quality needed for **`intent understanding`**.

- **4-bit quantization** — brought model sizes within the 2 GB RAM limit per VM. We didn't just apply off-the-shelf quantization: targeted modifications to the quantization scheme recovered accuracy losses specifically on **`multilingual intent classification`** and **`embedding generation`**.

- **Multilingual sentence encoder** — a multilingual **`dense retrieval`** encoder with fine-tuned query-document alignment. A single model handled product queries across languages, achieving strong **`cross-lingual semantic matching`** without any language-specific components.

- **In-memory LLM re-ranker** — after first-stage retrieval, a second-stage ranker (also running via llama's C++ runtime) re-scored candidates using deeper **`language understanding`**. This let us trade a small slice of compute budget for meaningful gains in **`ranking precision`**.

- **Hybrid retrieval with fallback and caching** — **`dense retrieval`** (embedding similarity) handled the majority of queries. **`BM25`** keyword search served as a fallback for out-of-distribution inputs. **`Query-result caching`** sat in front of both, cutting redundant encoder calls on repeated or near-duplicate queries.

- **Observability stack** — the full **`retrieval pipeline`** was instrumented with **Prometheus** metrics, **Grafana** dashboards, and **Jaeger** distributed tracing. **Apache Airflow** handled scheduled availability checks and automatic service recovery under load.

### Infrastructure
- **Allocated:** 40 VMs · 80 GB VRAM · AWS · GPU access permitted
- **Used:** 20 VMs · 2 vCPU · 2 GB RAM · **CPU only** — no GPU anywhere in the pipeline
- Average response latency: **~500ms**

Find code [here](https://github.com/azraihan/poridhi-2.0).

---

<div class="row">
  <div class="col-sm-4 mt-3">
    <img src="{{ '/assets/img/poridhi1.jpg' | relative_url }}" title="Team BUET XFACTOR" class="img-fluid rounded z-depth-1" style="width:100%; height:200px; object-fit:cover;">
  </div>
  <div class="col-sm-4 mt-3">
    <img src="{{ '/assets/img/poridhi2.jpg' | relative_url }}" title="Hackathon presentation" class="img-fluid rounded z-depth-1" style="width:100%; height:200px; object-fit:cover;">
  </div>
  <div class="col-sm-4 mt-3">
    <img src="{{ '/assets/img/poridhi3.jpg' | relative_url }}" title="Award ceremony" class="img-fluid rounded z-depth-1" style="width:100%; height:200px; object-fit:cover;">
  </div>
</div>
<div class="caption">Team BUET XFACTOR at the Poridhi.io × Brain Station 23 AI Engineering Hackathon.</div>

---

## Outcome

**1st place** among 86 teams and 300+ participants. The field included professional teams of industry software engineers, AI researchers, and ML practitioners. Our team was entirely undergraduates.