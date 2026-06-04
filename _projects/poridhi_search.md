---
layout: page
title: Intent-Based Multilingual Product Search
description: "Champions · AI Engineering Hackathon · Poridhi.io × Brain Station 23"
img: assets/img/poridhi1.jpg
importance: 2
category: research
related_publications: false
---

<div style="margin-bottom: 1.5rem;">
  <span style="background:#1a73e8;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">🏆 Champions</span>
  &nbsp;
  <span style="background:#2d9e2d;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">86 Teams · 300+ Participants</span>
  &nbsp;
  <span style="background:#555;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">April 2025</span>
</div>

## Overview

As **Team BUET XFACTOR**, we won 1st place at the **Poridhi.io × Brain Station 23 AI Engineering Hackathon** — one of Bangladesh's most competitive AI engineering competitions, with 86 teams and 300+ participants nationwide.

The challenge: build an **intent-based product search system** for multilingual product catalogs, deployable on severely constrained infrastructure (20 VMs, 2 vCPU, 2 GB RAM each — **no GPU access**).

---

## Technical Challenge

Standard LLM-based search systems assume GPU availability. Our constraint was extreme: we had to run sophisticated language models in-memory on CPU-only hardware while achieving sub-500ms average response latency, full multilingual support, and high availability.

This is precisely the kind of efficiency problem that motivates research into **retrieval-augmented generation** and **on-device LLM inference** — and it required us to make real systems-level decisions under pressure.

---

## Our Approach

**In-memory LLM inference via `llama.cpp`** — we ran quantized language models entirely in CPU memory, eliminating the GPU requirement while preserving the quality needed for intent understanding.

**4-bit quantization** — reduced memory footprint while maintaining acceptable accuracy for intent classification and embedding generation.

**Multilingual embedding models** — deployed multilingual sentence encoders to handle product queries across languages without language-specific fine-tuning.

**Hybrid retrieval** — combined dense semantic search (embedding similarity) with lightweight BM25 keyword matching for robustness on diverse query types.

**Automated monitoring and fallback** — built continuous availability checks with automatic recovery to ensure reliability under load.

### Infrastructure
- Used only **half** the allocated infrastructure (20 VMs, 2 vCPU, 2 GB RAM)
- Average response latency: **~500ms**
- No GPU resources anywhere in the pipeline

---

<div class="row">
  <div class="col-sm-4 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/poridhi1.jpg" title="Team BUET XFACTOR" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/poridhi2.jpg" title="Hackathon presentation" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/poridhi3.jpg" title="Award ceremony" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">Team BUET XFACTOR at the Poridhi.io × Brain Station 23 AI Engineering Hackathon (April 2025).</div>

---

## Connection to Research

This project sits at the intersection of **retrieval systems** and **LLM efficiency** — problems central to ongoing work in information retrieval and AI systems research. Deploying effective retrieval without specialized hardware forced us to think carefully about the tradeoffs between model expressiveness, quantization, and index design — questions closely related to work on late-interaction retrieval (ColBERT, WARP) and efficient LLM inference.

**Team:** Abrar Zahin Raihan · Ruwad Naswan · Mehedi Khan · Md. Mehedi Hasan · Dipit Saha

**Stack:** Python · llama.cpp · 4-bit quantization · multilingual embeddings · hybrid retrieval · FastAPI
