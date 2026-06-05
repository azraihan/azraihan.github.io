---
layout: page
title: Low-Resource ASR for Bangladeshi Dialects
# description: "1st Runner-Up · শব্দতরী Datathon · CUET ETE Televerse 1.0"
img: assets/img/asr1.jpg
importance: 3
category: research
related_publications: false
---

<div style="margin-bottom: 1.5rem;">
  <code><span style="color:#a0a0a0;">●</span> 1st Runner-Up</code>
  &nbsp;
  <code>CUET ETE · Televerse 1.0</code>
  &nbsp;
  <code>National</code>
  &nbsp;
  <code>ASR Datathon</code>
</div>

## Overview

Department of [Electronic and Telecommunication Engineering (ETE)](https://cuet.ac.bd/department/ETE) at the [Chittagong University of Engineering and Technology (CUET)](https://cuet.ac.bd/) organized **শব্দতরী — Where Dialects Flow into Bangla**, a low-resource automatic speech recognition (ASR) datathon, as part of [Televerse 1.0](https://www.eteteleverse.com/), the ETE department's flagship inter-university engineering event.

***The task:*** build an ASR system that transcribes speech from **20 regional Bangladeshi dialects** — Chittagong, Sylhet, Mymensingh, and others — into **standard Bangla**, with minimal labeled data. Bengali has over 160 million native speakers, yet regional dialect coverage in ASR remains largely unsolved.

---

## Technical Challenge

**`Low-resource ASR`** for South Asian languages sits at one of the harder corners of **`multilingual NLP`**. Three difficulties compounded each other:

- **High dialectal variation** — phonological, lexical, and prosodic differences across all 20 dialects
- **Limited labeled data** — too few examples per dialect for standard supervised training
- **Target normalization** — the output isn't just a transcription; it must conform to standardized Bangla orthography regardless of how the dialect sounds

Most multilingual NLP research implicitly assumes abundant data. Here, data scarcity was the central constraint — and it shaped every decision in the pipeline.

---

## Our Approach

We built a **`multilingual NLP pipeline`** around **Whisper Medium** — a **`multimodal audio-text sequence-to-sequence model`** — fine-tuned across four variants: encoder-only, full fine-tuning on standard Bangla, multi-task learning with a regional dialect classifier adapter, and full fine-tuning on regional speech. The four models were combined into a **`single inference system`** via **`ROVER ensemble voting`**.

Key decisions driven by the low-resource constraints:

- **Weighted random sampling** — rare dialects received up to 20× higher sampling weight per epoch, keeping the model from collapsing to dominant varieties
- **`LLM-in-the-loop data synthesis`** — used Gemini 2.5 Flash to generate ~290 additional training samples for the most data-scarce dialects via dialectal text → standard Bangla translation, an **`NLP-driven data augmentation`** strategy
- **Acoustic augmentation pipeline** — time stretching, pitch shifting, noise injection, and volume adjustment during training; spectral denoising and silence padding at inference

[Presentation](https://github.com/azraihan/Team-DejaView---CUET-ETE-Televerse-AIFication-2025-Datathon-Solution/blob/main/presentation/ai_fication_presentation.pdf) · [Code](https://github.com/azraihan/Team-DejaView---CUET-ETE-Televerse-AIFication-2025-Datathon-Solution)

---

<div class="row">
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/asr1.jpg" title="Team DejaView" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/asr2.jpg" title="Televerse 1.0 award" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">Team DejaView at শব্দতরী, CUET ETE Televerse 1.0.</div>

---

## Outcome

