---
layout: page
title: IEEE VIP Cup 2025
description: "Champions · Multimodal RGB-IR Fusion for Drone Surveillance · ICIP 2025"
img: assets/img/vip1.jpg
importance: 1
category: research
related_publications: false
---

<div style="margin-bottom: 1.5rem;">
  <span style="background:#1a73e8;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">🏆 Champions</span>
  &nbsp;
  <span style="background:#2d9e2d;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">International · 40+ Teams</span>
  &nbsp;
  <span style="background:#555;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">ICIP 2025, Anchorage, AK</span>
</div>

## Overview

As **Team NeuronX**, we won 1st place at the **IEEE Signal Processing Society Video and Image Processing (VIP) Cup 2025**, held at the International Conference on Image Processing (ICIP 2025) in Anchorage, Alaska. Our solution outperformed 40+ international teams.

The competition theme was **Infrared-Visual Fusion for Enhanced Drone Detection, Tracking, and Payload Identification in Surveillance Videos** — a challenging multimodal computer vision problem requiring robust performance under real-world degradations.

---

## Technical Problem

The task involved three simultaneous objectives on synchronized RGB and infrared video streams (320×256, 30 FPS):

1. **Binary classification** — drone vs. bird with real-time confidence scoring
2. **Continuous trajectory tracking** — IoU-based accuracy with directional motion analysis
3. **Payload threat classification** — distinguishing harmful from benign cargo

The challenge required systems to remain robust under severe environmental distortions: Gaussian blur, motion artifacts, camera instability, and additive white Gaussian noise (AWGN) — while maintaining real-time performance.

---

## Our Approach

We trained three distinct model families and developed a late-fusion architecture:

- **RGB-only model** — fine-tuned for color/texture features in visible spectrum
- **IR-only model** — adapted for thermal signatures and heat emission patterns
- **Fused RGB-IR model** — learned cross-modal complementarity for improved robustness

Key design decisions:
- Separate feature extraction branches preserved modality-specific inductive biases before fusion
- Hard negative mining from distortion-augmented samples improved noise robustness
- IoU-anchored temporal smoothing reduced trajectory jitter at 30 FPS

---

<div class="row">
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/vip1.jpg" title="Team NeuronX at ICIP 2025" class="img-fluid rounded z-depth-1" %}
    <div class="caption">Team NeuronX at ICIP 2025, Anchorage, Alaska.</div>
  </div>
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/vip2.jpg" title="VIP Cup award ceremony" class="img-fluid rounded z-depth-1" %}
    <div class="caption">Receiving the championship award at the IEEE SPS VIP Cup 2025.</div>
  </div>
</div>

---

## Outcome

- **1st place** among 40+ international university teams
- Presented the solution at ICIP 2025 in Anchorage, AK
- Faculty supervisor: Dr. Md. Shamsuzzöha Bayzid (BUET CSE)

**Team:** Abrar Zahin Raihan · Ruwad Naswan · Sadik Mahamud Shakshor · Mehedi Khan · Sadman Sakib

**Stack:** Python · PyTorch · RGB-IR fusion · real-time inference · multi-task learning
