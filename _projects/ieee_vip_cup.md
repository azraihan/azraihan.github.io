---
layout: page
title: IEEE VIP Cup 2025
# description: "Champions · Multimodal RGB-IR Fusion for Drone Surveillance · ICIP 2025"
img: assets/img/vip1.jpg
importance: 1
category: research
related_publications: false
---

<div style="margin-bottom: 1.5rem;">
  <code><span style="color:#f59e0b;">●</span> Champions</code>
  &nbsp;
  <code>IEEE · International · 40+ Teams</code>
  &nbsp;
  <code>Multimodal Systems</code>
  &nbsp;
  <code>ICIP 2025, Anchorage, AK</code>
</div>

## Overview

The competition theme of [IEEE SPS Video and Image Processing (VIP) Cup 2025](https://2025.ieeeicip.org/ieee-sps-video-and-image-processing-cup/) was [Infrared-Visual Fusion for Enhanced Drone Detection, Tracking, and Payload Identification in Surveillance Videos](https://2025.ieeeicip.org/wp-content/uploads/sites/679/2025-VIP-Cup-Competition-Official-Document_Version-1.2-with-extended-deadlines.pdf) — a challenging multimodal computer vision problem requiring robust performance under real-world degradations.

---

## Technical Problem

The task involved three simultaneous objectives on synchronized RGB and infrared video streams:

1. **Binary classification** — drone vs. bird with real-time confidence scoring
2. **Continuous trajectory tracking** — IoU-based accuracy with directional motion analysis
3. **Payload threat classification** — distinguishing harmful from benign cargo in drones

The challenge required systems to remain robust under severe environmental distortions: Gaussian blur, motion artifacts, camera instability, and additive white Gaussian noise (AWGN) — while maintaining real-time performance.

Find more [here](https://2025.ieeeicip.org/wp-content/uploads/sites/679/2025-VIP-Cup-Competition-Official-Document_Version-1.2-with-extended-deadlines.pdf).

---

## Our Approach

- Explored **`multimodal AI`** through a learned RGB-IR fusion architecture (DEYOLO) — using cross-modal attention (DECA + DEPA) to suppress inter-modal interference rather than naively concatenating modalities
- Applied **`computer vision`** at scale: ensembling YOLOv8, Co-DETR (transformer), and RF-DETR (DINOv2 ViT-L/14 backbone) via majority voting to exploit complementary error profiles across architectures
- Designed the full **`AI system`** end-to-end — from stratified data splitting and augmentation pipelines to ByteTrack integration and preprocessing — treating robustness as a systems problem, not just a training problem

***More details below.***

[Presentation]({{ '/assets/pdf/Team_NeuronX_VIP_Cup_2025.pdf' | relative_url }}){:target="_blank"} · [Paper]() · [Code]()


---

<div class="row" style="align-items: flex-start;">
  <div class="col-sm-6 mt-3">
    <img src="{{ '/assets/img/vip1.jpg' | relative_url }}" title="Team NeuronX at ICIP 2025" class="img-fluid rounded z-depth-1" style="width:100%; height:260px; object-fit:cover;">
    <div class="caption">Team NeuronX at ICIP 2025, Anchorage, Alaska.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <img src="{{ '/assets/img/vip2.jpg' | relative_url }}" title="VIP Cup award ceremony" class="img-fluid rounded z-depth-1" style="width:100%; height:260px; object-fit:cover;">
    <div class="caption">Championship award at the IEEE SPS VIP Cup 2025.</div>
  </div>
</div>

---

## Faculty supervisor
[Dr. Md. Shamsuzzöha Bayzid (BUET CSE)](https://cse.buet.ac.bd/faculty/faculty_detail/bayzid)

---

## Outcome

- Our solution earned us the **championship**, outperforming **40+ international teams**
- The final presentation took place at [ICIP 2025](https://2025.ieeeicip.org/) in Anchorage, AK


<!-- **Team:** Abrar Zahin Raihan · Ruwad Naswan · Sadik Mahamud Shakshor · Mehedi Khan · Sadman Sakib -->
