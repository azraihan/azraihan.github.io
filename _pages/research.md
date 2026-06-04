---
layout: page
title: research
permalink: /research/
description: My research trajectory — how my work connects, where it leads.
nav: true
nav_order: 2
---

<style>
/* Timeline styles */
.rj-section-title {
  font-size: 1.1rem;
  font-weight: 700;
  letter-spacing: 0.07em;
  text-transform: uppercase;
  color: #888;
  margin: 2.5rem 0 1rem 0;
  padding-bottom: 0.4rem;
  border-bottom: 2px solid #e0e0e0;
}

.rj-vision {
  font-size: 1.05rem;
  line-height: 1.75;
  border-left: 4px solid #1a73e8;
  padding: 1rem 1.4rem;
  margin: 1.5rem 0 2rem 0;
  background: rgba(26,115,232,0.04);
  border-radius: 0 6px 6px 0;
}

/* Paper / output cards */
.rj-timeline {
  position: relative;
  padding-left: 0;
  list-style: none;
}

.rj-timeline::before {
  content: '';
  position: absolute;
  left: 10px;
  top: 6px;
  bottom: 6px;
  width: 2px;
  background: #ddd;
}

.rj-entry {
  display: flex;
  gap: 1.2rem;
  margin-bottom: 1.8rem;
  position: relative;
}

.rj-dot {
  flex-shrink: 0;
  width: 22px;
  height: 22px;
  border-radius: 50%;
  border: 3px solid #1a73e8;
  background: #fff;
  margin-top: 4px;
  z-index: 1;
}

.rj-dot.accepted { border-color: #1a73e8; background: #1a73e8; }
.rj-dot.review   { border-color: #e8871a; background: #fff; }
.rj-dot.comp     { border-color: #2d9e2d; background: #2d9e2d; }

.rj-card {
  flex: 1;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 1rem 1.2rem;
  background: #fafafa;
}

.dark .rj-card { background: #1e1e1e; border-color: #333; }
.dark .rj-vision { background: rgba(26,115,232,0.08); }

.rj-card-header {
  display: flex;
  align-items: flex-start;
  gap: 0.7rem;
  flex-wrap: wrap;
  margin-bottom: 0.5rem;
}

.rj-badge {
  font-size: 0.72rem;
  font-weight: 700;
  padding: 2px 8px;
  border-radius: 4px;
  white-space: nowrap;
  flex-shrink: 0;
  margin-top: 2px;
}

.badge-acl    { background: #1a73e8; color: #fff; }
.badge-cvpr   { background: #c0392b; color: #fff; }
.badge-icml   { background: #8e44ad; color: #fff; }
.badge-comp   { background: #2d9e2d; color: #fff; }
.badge-review { background: #e67e22; color: #fff; }

.rj-card h4 {
  margin: 0;
  font-size: 0.95rem;
  font-weight: 600;
  line-height: 1.45;
}

.rj-card p {
  margin: 0.4rem 0 0 0;
  font-size: 0.88rem;
  color: #555;
  line-height: 1.6;
}

.dark .rj-card p { color: #aaa; }

.rj-card .rj-connect {
  margin-top: 0.5rem;
  font-size: 0.82rem;
  color: #1a73e8;
  font-style: italic;
}

/* Theme threads */
.rj-themes {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
  gap: 1rem;
  margin: 1rem 0 2rem 0;
}

.rj-theme-card {
  border-radius: 8px;
  padding: 1rem 1.1rem;
  border: 1px solid #e0e0e0;
}

.dark .rj-theme-card { border-color: #333; }

.rj-theme-card h4 {
  margin: 0 0 0.4rem 0;
  font-size: 0.9rem;
  font-weight: 700;
}

.rj-theme-card p {
  margin: 0;
  font-size: 0.84rem;
  line-height: 1.55;
  color: #555;
}

.dark .rj-theme-card p { color: #aaa; }

.theme-nlp   { border-top: 4px solid #1a73e8; }
.theme-eff   { border-top: 4px solid #2d9e2d; }
.theme-mech  { border-top: 4px solid #8e44ad; }
.theme-sys   { border-top: 4px solid #e8871a; }

.rj-forward {
  border-radius: 8px;
  border: 1px solid #e0e0e0;
  padding: 1.2rem 1.5rem;
  margin-top: 1rem;
  background: #fafafa;
}

.dark .rj-forward { background: #1e1e1e; border-color: #333; }

.rj-forward p {
  margin: 0.3rem 0;
  font-size: 0.92rem;
  line-height: 1.7;
}
</style>

<div class="rj-vision">
I study how AI systems reason — across languages, modalities, and compositional tasks — and how to make them more robust, efficient, and principled. My work converges on a central question: <strong>can the design of AI pipelines be made systematic and optimizable, rather than a matter of prompt engineering?</strong>
</div>

<div class="rj-section-title">Research Timeline</div>

<ul class="rj-timeline">

  <li class="rj-entry">
    <div class="rj-dot accepted"></div>
    <div class="rj-card">
      <div class="rj-card-header">
        <span class="rj-badge badge-acl">ACL 2026 Workshop</span>
        <span class="rj-badge badge-acl">Accepted · Archival</span>
        <h4>Causal Localization of the English Pivot in LLaVA: Mechanistic VLM Analysis and Training-Free Multilingual Steering</h4>
      </div>
      <p>Applied logit-lens analysis and causal activation patching to locate the English-pivot bottleneck in LLaVA-1.5-7B at layers 5–17. Derived training-free steering vectors at those layers that improve Russian VQA by +6.5 pp and Portuguese by +4.0 pp — without any fine-tuning.</p>
      <p class="rj-connect">→ Multilingual AI · Mechanistic interpretability · Extending English-pivot analysis to multimodal models</p>
    </div>
  </li>

  <li class="rj-entry">
    <div class="rj-dot accepted"></div>
    <div class="rj-card">
      <div class="rj-card-header">
        <span class="rj-badge badge-cvpr">CVPR 2026 Workshop</span>
        <span class="rj-badge badge-acl">Accepted · Poster</span>
        <h4>Where Do Affordances Crystallize? Video vs. Image Self-Supervised Encoders for Embodied Perception</h4>
      </div>
      <p>Probed 25 layer positions of ViT-L encoders (V-JEPA 2, V-JEPA 2.1, DINOv2) on the UMD Part Affordance Dataset. Video SSL crystallizes affordance signal 4 layers earlier than image SSL; keeping the top-3 attention heads achieves 5.3× compute reduction with ≤0.1 mAP loss.</p>
      <p class="rj-connect">→ Representational analysis · Efficient inference · Embodied AI · Self-supervised learning</p>
    </div>
  </li>

  <li class="rj-entry">
    <div class="rj-dot review"></div>
    <div class="rj-card">
      <div class="rj-card-header">
        <span class="rj-badge badge-icml">ICML 2026 Workshop</span>
        <span class="rj-badge badge-review">Under Review</span>
        <h4>When Does Visual Context Help? Adaptive Modality Gating for Efficient Multimodal QA</h4>
      </div>
      <p>AdaGate is a lightweight MLP that, given only partial question text, predicts whether invoking the vision encoder will improve the answer. Trained on WebQA, it reduces vision encoder calls by ~53% with near-identical keyword F1. On text-only QANTA quizbowl questions the gate fires on fewer than 2.9% of inputs despite no explicit text-only supervision.</p>
      <p class="rj-connect">→ Selective retrieval · Efficient inference · Adaptive computation — structurally similar to RAG's "when to retrieve" decision</p>
    </div>
  </li>

  <li class="rj-entry">
    <div class="rj-dot review"></div>
    <div class="rj-card">
      <div class="rj-card-header">
        <span class="rj-badge badge-cvpr">CVPR 2026 Workshop</span>
        <span class="rj-badge badge-review">Under Review</span>
        <h4>SpatialCoT: Chain-of-Thought Spatial Grounding for Viewpoint-Robust 3D-LLMs</h4>
      </div>
      <p>Proposes a five-step geometry-grounded chain-of-thought (Localize → Orient → Enumerate → Compute → Answer) trained on ~8K auto-annotated ProcTHOR scenes. Reduces viewpoint-rotation accuracy degradation in Real-3DQA from 77% to 41%.</p>
      <p class="rj-connect">→ Structured reasoning · Spatial grounding · Addressing shortcut learning in 3D understanding</p>
    </div>
  </li>

  <li class="rj-entry">
    <div class="rj-dot comp"></div>
    <div class="rj-card">
      <div class="rj-card-header">
        <span class="rj-badge badge-comp">IEEE VIP Cup 2025 · Champions</span>
        <h4>Multimodal RGB-IR Fusion for Drone Surveillance</h4>
      </div>
      <p>1st place among 40+ international teams. Built a late-fusion multimodal system combining RGB and infrared streams for simultaneous drone/bird classification, trajectory tracking, and payload threat classification at 30 FPS under severe distortions (AWGN, motion blur, camera instability). Presented at ICIP 2025, Anchorage, AK.</p>
      <p class="rj-connect">→ Multimodal fusion · Robustness under distribution shift · Real-time inference</p>
    </div>
  </li>

  <li class="rj-entry">
    <div class="rj-dot comp"></div>
    <div class="rj-card">
      <div class="rj-card-header">
        <span class="rj-badge badge-comp">Poridhi × BS23 Hackathon · Champions</span>
        <h4>Intent-Based Multilingual Product Search (CPU-only, 86 teams)</h4>
      </div>
      <p>1st place. Built a multilingual semantic product search system with in-memory LLM inference via llama.cpp and 4-bit quantization — no GPU, using only half the allocated hardware. Sub-500ms latency, high availability, multilingual embedding retrieval.</p>
      <p class="rj-connect">→ Dense retrieval · LLM efficiency · Multilingual embeddings — directly in the territory of ColBERT, RAG, and efficient IR</p>
    </div>
  </li>

  <li class="rj-entry">
    <div class="rj-dot comp"></div>
    <div class="rj-card">
      <div class="rj-card-header">
        <span class="rj-badge badge-comp">শব্দতরী Datathon · 1st Runner-Up</span>
        <h4>Low-Resource ASR for 20 Bangladeshi Dialects</h4>
      </div>
      <p>Developed an ASR system transcribing speech from 20 regional Bangla dialects to standard Bangla using transfer learning, encoder adaptation, and dialect-aware embeddings — a low-resource multilingual NLP problem with real societal impact.</p>
      <p class="rj-connect">→ Low-resource NLP · Multilingual speech · Transfer learning under data scarcity</p>
    </div>
  </li>

</ul>

<div class="rj-section-title">Research Themes</div>

<div class="rj-themes">
  <div class="rj-theme-card theme-nlp">
    <h4>Multilingual &amp; Low-Resource AI</h4>
    <p>From dialect ASR for 20 Bangla varieties to causal analysis of multilingual VLMs — building AI that works equitably across languages.</p>
  </div>
  <div class="rj-theme-card theme-eff">
    <h4>Efficient &amp; Adaptive Inference</h4>
    <p>AdaGate's selective modality invocation, llama.cpp on constrained hardware, attention head pruning — the question of when and how to run expensive components.</p>
  </div>
  <div class="rj-theme-card theme-mech">
    <h4>Mechanistic Understanding</h4>
    <p>Using logit-lens and causal patching to locate where and why models succeed or fail — building principled interventions from structural insight.</p>
  </div>
  <div class="rj-theme-card theme-sys">
    <h4>AI Systems &amp; Programmability</h4>
    <p>The convergence point: how can complex AI pipelines — retrieval, reasoning, generation — be designed, composed, and optimized as systems rather than prompt assemblies?</p>
  </div>
</div>

<div class="rj-section-title">Where This Leads</div>

<div class="rj-forward">
  <p>The four threads above converge on a shared concern: AI systems that are <strong>reliable, composable, and improvable by design</strong>. Mechanistic interpretability reveals what existing pipelines are actually doing. Efficient inference asks how to reduce cost without sacrificing quality. Multilingual work surfaces where pipelines break for underserved users. And the systems thread asks how all of this can be expressed declaratively — so that optimization, not hand-tuning, drives quality.</p>
  <p>This is the direction I want to pursue at the PhD level: building the foundations for AI systems that reason systematically, retrieve selectively, and can be programmed and optimized like software — not assembled from heuristics. It is the question at the center of work on declarative AI programming, prompt optimization, and scalable retrieval-augmented systems.</p>
</div>
