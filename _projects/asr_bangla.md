---
layout: page
title: Low-Resource ASR for Bangladeshi Dialects
description: "1st Runner-Up · শব্দতরী Datathon · CUET ETE Televerse 1.0"
img: assets/img/asr1.jpg
importance: 3
category: research
related_publications: false
---

<div style="margin-bottom: 1.5rem;">
  <span style="background:#c0392b;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">🥈 1st Runner-Up</span>
  &nbsp;
  <span style="background:#555;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">CUET ETE · Televerse 1.0 · November 2025</span>
</div>

## Overview

As **Team DejaView**, we placed 1st Runner-Up at **শব্দতরী — Where Dialects Flow into Bangla**, a low-resource automatic speech recognition (ASR) datathon organized by the Department of Electronic and Telecommunication Engineering (ETE), CUET, as part of Televerse 1.0.

The task: develop an ASR system capable of transcribing speech from **20 regional Bangladeshi dialects** — including Chittagong, Sylhet, Mymensingh, and others — into **standard Bangla**, using a severely limited training dataset.

---

## Technical Challenge

Low-resource ASR is one of the hardest problems in multilingual NLP. The challenge combined several compounding difficulties:

- **High dialectal variation** — phonological, lexical, and prosodic differences across 20 dialects
- **Limited labeled data** — insufficient examples per dialect for standard supervised training
- **Target normalization** — mapping dialectal speech to standardized Bangla orthography (not just transcription)

This is closely related to the broader problem of building NLP systems for under-resourced languages — a direction that motivates much of the recent work in multilingual AI.

---

## Our Approach

We built a pipeline centered on **transfer learning from large pre-trained speech models**, adapted to the Bangla multilingual setting:

- **Encoder adaptation** — fine-tuned a pre-trained multilingual speech encoder on available Bangla data before dialect-specific adaptation
- **Dialect-aware embeddings** — incorporated dialect identity signals to condition the decoder on expected phonological patterns
- **Data augmentation** — generated additional training signal through acoustic augmentation (speed perturbation, noise injection) to combat data scarcity
- **CTC + attention decoding** — combined connectionist temporal classification with attention mechanisms for robust sequence decoding

---

<div class="row">
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/asr1.jpg" title="Team DejaView" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/asr2.jpg" title="Televerse 1.0 award" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">Team DejaView at শব্দতরী, CUET ETE Televerse 1.0 (November 2025).</div>

---

## Why This Matters

Over 160 million people speak Bengali as a first language, yet the vast majority of ASR research focuses on standard dialects with abundant data. Building systems that work across regional varieties is a critical step toward equitable AI for South Asian languages — and a technically demanding multilingual NLP problem.

**Team:** Abrar Zahin Raihan · Ruwad Naswan · Shadab Tanjeed

**Stack:** Python · PyTorch · HuggingFace Transformers · Wav2Vec2 / Whisper · CTC decoding
