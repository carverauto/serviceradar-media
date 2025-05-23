---
theme: dracula
favicon: https://staging.serviceradar.io/favicon.svg
title: ServiceRadar - Zero-Trust Network Monitoring
info: |
  ## ServiceRadar - Zero-Trust Network Monitoring
  The first network monitoring platform built with security-first design
  for today's distributed infrastructure challenges.

  Learn more at [serviceradar.io](https://staging.serviceradar.io)
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: slide-left
mdc: true
lineNumbers: false
download: true
exportFilename: serviceradar-overview
css: unocss
---

# ServiceRadar

<div class="text-xl mt-2 mb-6">Zero-Trust Network Monitoring for Hard-to-Reach Environments</div>

<div class="mb-4">
  <span class="px-2 py-1 rounded bg-red-500 text-white mx-1">Secure by Design</span>
  <span class="px-2 py-1 rounded bg-blue-500 text-white mx-1">Edge to Cloud</span>
  <span class="px-2 py-1 rounded bg-green-500 text-white mx-1">No Blind Spots</span>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/carverauto/serviceradar" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>


---
layout: default
class: px-4
---

# The Invisible Problem

## Monitoring Blind Spots Are Costing You

- **73% of network outages** in remote locations go undetected for 4+ hours
- Intermittent connections create **false alarms** and **missed incidents**
- Security vulnerabilities from **monitoring backdoors**
- Per-node licensing makes comprehensive monitoring **prohibitively expensive**
- Traditional tools are **too resource-intensive** for edge devices

<div class="mt-8 text-amber-400 font-bold">
You can't manage what you can't see. And you can't secure what you can't properly monitor.
</div>

---
layout: two-cols
class: px-4
---

# Why ServiceRadar Is Different

## Built for Zero-Trust From Day One

- **No monitoring back doors** - one-way data flow from edge to cloud
- **Zero-trust architecture** with mTLS encryption everywhere
- **Rust/Go core** eliminates entire classes of security vulnerabilities
- **Lightweight agents** (50MB) optimized for constrained environments
- Monitoring designed for the **modern distributed era**

::right::

<div class="pl-4 mt-12">

## Traditional Monitoring Platforms

- Built before modern security threats emerged
- Two-way communication creates attack vectors
- Heavyweight agents (500MB+) drain resources
- Per-node licensing creates financial blind spots
- Inconsistent security model

<div class="border-l-4 border-red-500 pl-4 mt-4 italic">
"Legacy monitoring tools force you to choose between security and visibility."
</div>

</div>

---
layout: statement
class: text-center
---

# Security Shouldn't Be Optional in Monitoring

<div class="text-xl mt-4 text-amber-400">
ServiceRadar is the first monitoring platform designed with security-first architecture
</div>

---
layout: default
class: px-4
---

# Complete Visibility with Zero-Trust

- **🔒 Secure by Design:** Zero-trust, one-way data flow, mTLS encryption.
- **⚙️ Distributed Fleet Control:** NATS JetStream for KV and message broker.
- **🚀 Lightweight & Modern:** 50MB agent, built with Rust/Go for performance.
- **📊 Advanced Analytics:** SRQL, LLM integration, NetFlow analysis (coming soon).
- **🔍 Complete Visibility:** Topology-aware, ECMP analysis, 90M EPS processing.

---
layout: default
class: px-4
---

# ServiceRadar Architecture Overview

```mermaid
graph LR
    subgraph "Edge"
        Agent[ServiceRadar Agent<br>at Edge (50051)]
    end

    subgraph "Monitoring & Aggregation"
        Poller[ServiceRadar Poller<br>(50053)]
    end

    subgraph "Core Layer"
        CoreService[Core Service<br>API (8090) & gRPC (50052)]
        WebUI[Web UI (80/nginx)]
        ProtonDB[Proton DB<br>(Data Storage)]

        CoreService -- uses --> ProtonDB
        WebUI -- interacts with --> CoreService
    end

    Agent -->|Service Status| Poller
    Poller -->|Aggregated Data| CoreService

    style Agent fill:#fd9,stroke:#333,stroke-width:1px
    style Poller fill:#adb,stroke:#333,stroke-width:1px
    style CoreService fill:#9bc,stroke:#333,stroke-width:2px
    style WebUI fill:#b9c,stroke:#333,stroke-width:1px
    style ProtonDB fill:#e1f5fe,stroke:#01579b,stroke-width:1px
```

---
layout: default
class: px-4
---

# Real-World Applications

<div class="grid grid-cols-3 gap-4">
<div class="p-4 border rounded shadow-md">
  <div class="text-xl mb-2 font-bold text-green-400">Telecommunications</div>
  <p>Monitor thousands of remote cell sites with minimal footprint and no security vulnerabilities.</p>
</div>

<div class="p-4 border rounded shadow-md">
  <div class="text-xl mb-2 font-bold text-blue-400">Retail</div>
  <p>Secure monitoring for distributed POS and store networks with minimal IT support.</p>
</div>

<div class="p-4 border rounded shadow-md">
  <div class="text-xl mb-2 font-bold text-purple-400">Data Centers</div>
  <p>Topology-aware CLOS fabric monitoring with ECMP analysis and flow optimization.</p>
</div>

<div class="p-4 border rounded shadow-md">
  <div class="text-xl mb-2 font-bold text-amber-400">Industrial IoT</div>
  <p>Lightweight monitoring for resource-constrained edge environments with secure data flow.</p>
</div>

<div class="p-4 border rounded shadow-md">
  <div class="text-xl mb-2 font-bold text-red-400">Hybrid Cloud</div>
  <p>Unified view across on-prem and cloud with security-first architecture.</p>
</div>

<div class="p-4 border rounded shadow-md">
  <div class="text-xl mb-2 font-bold text-cyan-400">Critical Infrastructure</div>
  <p>Monitoring for sensitive networks without introducing new attack vectors.</p>
</div>
</div>

---
layout: default
class: px-4
---

# Architecture & Performance

<div class="grid grid-cols-2 gap-4 mt-4">
  <div class="p-3 border rounded">
    <div class="text-lg font-bold">Secure Edge Agents</div>
    <div>Rust/Go architecture</div>
    <div>50MB memory footprint</div>
    <div>mTLS everywhere</div>
  </div>

  <div class="p-3 border rounded">
    <div class="text-lg font-bold">Powerful Analytics</div>
    <div>90M events/second</div>
    <div>4ms end-to-end latency</div>
    <div>1M unique metrics</div>
  </div>

  <div class="p-3 border rounded">
    <div class="text-lg font-bold">One-Way Data Flow</div>
    <div>Edge to cloud only</div>
    <div>Zero monitoring backdoors</div>
    <div>No remote agent control</div>
  </div>

  <div class="p-3 border rounded">
    <div class="text-lg font-bold">Distributed KV Store</div>
    <div>Secure configuration</div>
    <div>NATS JetStream powered</div>
    <div>Real-time updates</div>
  </div>
</div>

---
layout: statement
class: text-center
---

# "ServiceRadar is the first monitoring solution that our security team actually approved without hesitation."
<div class="text-right mt-4 italic">— Network Director, Fortune 500 Retailer</div>

---
layout: default
class: text-center
---

# Get Started in Minutes

<div class="mb-4 flex justify-center">
  <div class="p-4 border rounded-md inline-block text-left bg-gray-800">
    <code>curl -sSL https://github.com/carverauto/serviceradar/releases/download/1.0.36/install-serviceradar.sh | bash</code>
  </div>
</div>

<div class="grid grid-cols-3 gap-6 mt-8">
  <div class="flex flex-col items-center">
    <div class="text-5xl mb-4">🔒</div>
    <div class="font-bold">Secure by Default</div>
    <div class="text-sm">mTLS preconfigured</div>
  </div>

  <div class="flex flex-col items-center">
    <div class="text-5xl mb-4">⚡</div>
    <div class="font-bold">Instant Visibility</div>
    <div class="text-sm">See results in seconds</div>
  </div>

  <div class="flex flex-col items-center">
    <div class="text-5xl mb-4">🌐</div>
    <div class="font-bold">Web Dashboard</div>
    <div class="text-sm">Modern UI included</div>
  </div>
</div>

<div class="mt-8">
  <a href="https://demo.serviceradar.cloud" class="px-4 py-2 rounded bg-green-600 text-white font-bold">
    Try Now →
  </a>
</div>

---
layout: end
---

# Start monitoring securely today

[demo.serviceradar.cloud](https://demo.serviceradar.cloud) | [@ServiceRadar](https://twitter.com/serviceradar)
