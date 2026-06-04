---
layout: page
title: Real-Time Ticketing System on Kubernetes
description: "2nd Runner-Up · BUET CSE Fest Hackathon 2024 · Microservices & DevOps"
img: assets/img/devops1.jpg
importance: 5
category: engineering
related_publications: false
---

<div style="margin-bottom: 1.5rem;">
  <span style="background:#8e44ad;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">🥉 2nd Runner-Up</span>
  &nbsp;
  <span style="background:#555;color:#fff;padding:3px 10px;border-radius:4px;font-size:0.82rem;font-weight:600;">BUET CSE Fest Hackathon 2024 · Microservices & DevOps</span>
</div>

## Overview

Built a production-grade, cloud-native real-time ticketing and booking system for the **BUET CSE Fest Hackathon 2024** Microservices and DevOps category, placing **2nd Runner-Up** — a strong result for a first-ever DevOps hackathon entry.

The system was designed to handle high concurrent load with zero-downtime deployments, automated scaling, and full observability.

---

## Architecture

**Microservices** — The system was decomposed into independent services for authentication and booking, each independently deployable and scalable.

**Azure Kubernetes Service (AKS)** — All services containerized with Docker and orchestrated via Kubernetes for automated horizontal scaling and load balancing.

**Redis caching** — Session and booking data cached to reduce database pressure under peak load.

**CI/CD with GitHub Actions** — Fully automated test, build, and deploy pipeline enabling zero-downtime rolling deployments.

**Observability stack** — Prometheus metrics collection, Grafana dashboards for real-time visibility, and k6 for systematic load testing.

**Rate limiting and OTP verification** — API security with rate limiting middleware and OTP-based booking confirmation.

---

<div class="row">
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/devops1.jpg" title="BUET CSE Fest Hackathon 2024" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3">
    {% include figure.liquid loading="eager" path="assets/img/devops2.jpg" title="Team at BUET CSE Fest" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">BUET CSE Fest Hackathon 2024 — Microservices & DevOps Category (October 2024).</div>

---

**Stack:** Node.js · Express.js · Redis · Docker · Kubernetes · Azure (AKS) · Terraform · GitHub Actions · Prometheus · Grafana · k6

**GitHub:** [github.com/azraihan/bcf2024-microservice-devops-team-95152-buet21](https://github.com/azraihan/bcf2024-microservice-devops-team-95152-buet21)
