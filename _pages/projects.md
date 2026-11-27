---
layout: page
title: Projects
permalink: /projects/
description: Competition projects in computer vision, multimodal learning, speech and language processing, and scalable systems.
nav: true
nav_order: 4
---

<style>
.az-proj-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  overflow: hidden;
}
[data-theme="dark"] .az-proj-card { border-color: #333; }

.az-proj-desc { color: #555; }
[data-theme="dark"] .az-proj-desc { color: #bbb; }
</style>

## Deep Learning Competitions and AI Engineering Hackathons

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 1.2rem; margin-bottom: 2.5rem;">

  <div class="az-proj-card">
    <img src="{{ '/assets/img/vip1.jpg' | relative_url }}" alt="IEEE VIP Cup 2025" style="width: 100%; height: 160px; object-fit: cover;">
    <div style="padding: 0.9rem 1rem 1rem;">
      <div style="margin-bottom: 0.4rem;">
        <code><span style="color:#f59e0b;">●</span> Champions</code><br><code>IEEE · International</code><br><code>Multimodal Systems</code>
      </div>
      <h4 style="margin: 0.5rem 0 0.3rem; font-size: 0.95rem; font-weight: 700;">IEEE VIP Cup 2025</h4>
      <p class="az-proj-desc" style="margin: 0 0 0.7rem; font-size: 0.85rem; line-height: 1.5;"><strong>Multimodal</strong> RGB-IR fusion for real-time <strong>UAV detection</strong>, <strong>tracking</strong>, and <strong>payload classification</strong>. 1st place among 40+ international teams. Presented at ICIP 2025, Anchorage, AK, USA.</p>
      <a href="{{ '/projects/ieee_vip_cup/' | relative_url }}" style="font-size: 0.85rem; font-weight: 600;">Read More →</a>
    </div>
  </div>

  <div class="az-proj-card">
    <img src="{{ '/assets/img/poridhi1.jpg' | relative_url }}" alt="Poridhi AI Hackathon" style="width: 100%; height: 160px; object-fit: cover;">
    <div style="padding: 0.9rem 1rem 1rem;">
      <div style="margin-bottom: 0.4rem;">
        <code><span style="color:#f59e0b;">●</span> Champions</code><br><code>National</code><br><code>AI Hackathon</code>
      </div>
      <h4 style="margin: 0.5rem 0 0.3rem; font-size: 0.95rem; font-weight: 700;">Poridhi.io × BrainStation23 AI Hackathon</h4>
      <p class="az-proj-desc" style="margin: 0 0 0.7rem; font-size: 0.85rem; line-height: 1.5;">Built a <strong>retrieval-augmented</strong>, intent-based <strong>multilingual search</strong> system — decomposing user queries into <strong>semantic intent</strong> before <strong>dense retrieval</strong> over a product corpus. Open to professionals; 1st place among 86 teams.</p>
      <a href="{{ '/projects/poridhi_search/' | relative_url }}" style="font-size: 0.85rem; font-weight: 600;">Read More →</a>
    </div>
  </div>

  <div class="az-proj-card">
    <img src="{{ '/assets/img/asr1.jpg' | relative_url }}" alt="ASR Bangla Dialects" style="width: 100%; height: 160px; object-fit: cover;">
    <div style="padding: 0.9rem 1rem 1rem;">
      <div style="margin-bottom: 0.4rem;">
        <code><span style="color:#94a3b8;">●</span> 1st Runner-Up</code><br><code>Multimodal NLP</code>
      </div>
      <h4 style="margin: 0.5rem 0 0.3rem; font-size: 0.95rem; font-weight: 700;">শব্দতরী — Bangla Dialect ASR</h4>
      <p class="az-proj-desc" style="margin: 0 0 0.7rem; font-size: 0.85rem; line-height: 1.5;">A <strong>multimodal NLP</strong> task — bridging the <strong>acoustic modality</strong> (dialectal speech) and the <strong>text modality</strong> (standard Bangla) across 20 <strong>low-resource</strong> regional varieties. Built on <strong>cross-lingual transfer</strong> and dialect-conditioned representations, highlighting the data-scarcity challenges central to <strong>multilingual NLP</strong>.</p>
      <a href="{{ '/projects/asr_bangla/' | relative_url }}" style="font-size: 0.85rem; font-weight: 600;">Read More →</a>
    </div>
  </div>

</div>

<details>
<summary style="cursor:pointer; font-size:1.5rem; font-weight:700; margin-bottom:1rem; list-style:none; display:flex; align-items:center; gap:0.5rem;">
  <span class="az-details-arrow" style="font-size:1rem; transition:transform 0.2s;">▶</span> Engineering Scalable Systems <span style="font-size:0.75rem; font-weight:400; opacity:0.5; margin-left:0.4rem;">click to expand</span>
</summary>

<script>
  document.currentScript.closest('details').addEventListener('toggle', function(e) {
    this.querySelector('.az-details-arrow').style.transform = this.open ? 'rotate(90deg)' : '';
  });
</script>

<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.2rem; margin-bottom: 2rem; margin-top: 1rem;">

  <div class="az-proj-card">
    <img src="{{ '/assets/img/codesprout1.jpg' | relative_url }}" alt="CodeSprout" style="width: 100%; height: 160px; object-fit: cover;">
    <div style="padding: 0.9rem 1rem 1rem;">
      <div style="margin-bottom: 0.4rem;">
        <code><span style="color:#22c55e;">●</span> Top 10 Finalist</code><br><code>AI Hackathon</code>
      </div>
      <h4 style="margin: 0.5rem 0 0.3rem; font-size: 0.95rem; font-weight: 700;">Therap JavaFest 2024</h4>
      <p class="az-proj-desc" style="margin: 0 0 0.7rem; font-size: 0.85rem; line-height: 1.5;"><strong>RAG</strong>-powered conversational assistant, <strong>semantic retrieval</strong>-based project recommender, and <strong>computer vision</strong> sketch-to-image pipeline — packaged as a gamified coding platform for children. Top 10 among <strong>1300+ participants</strong>.</p>
      <a href="{{ '/projects/codesprout/' | relative_url }}" style="font-size: 0.85rem; font-weight: 600;">Read More →</a>
    </div>
  </div>

  <div class="az-proj-card">
    <img src="{{ '/assets/img/devops1.jpg' | relative_url }}" alt="Real-Time Ticketing System" style="width: 100%; height: 160px; object-fit: cover;">
    <div style="padding: 0.9rem 1rem 1rem;">
      <div style="margin-bottom: 0.4rem;">
        <code><span style="color:#8B4513;">●</span> 2nd Runner-Up</code><br><code>BUET CSE Fest 2024</code><br><code>Microservices & DevOps</code>
      </div>
      <h4 style="margin: 0.5rem 0 0.3rem; font-size: 0.95rem; font-weight: 700;">Scalable Real-Time Ticketing System</h4>
      <p class="az-proj-desc" style="margin: 0 0 0.7rem; font-size: 0.85rem; line-height: 1.5;">Production-grade <strong>cloud-native</strong> ticketing system on <strong>Azure Kubernetes Service</strong>. Features zero-downtime rolling deployments, <strong>Redis</strong> caching, automated <strong>CI/CD</strong> via GitHub Actions, and full observability with <strong>Prometheus</strong> and Grafana.</p>
      <a href="{{ '/projects/devops_ticketing/' | relative_url }}" style="font-size: 0.85rem; font-weight: 600;">Read More →</a>
    </div>
  </div>

</div>

</details>
