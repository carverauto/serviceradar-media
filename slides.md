---
# try also 'default' to start simple
theme: dracula
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://cover.sli.dev
favicon: https://staging.serviceradar.io/favicon.svg
# some information about your slides, markdown enabled
title: ServiceRadar Automation
info: |
  ## ServiceRadar Automation Pitch Book
  Distributed Network Monitoring for Infrastructure and Services

  Learn more at [serviceradar.io](https://staging.serviceradar.io)
# apply any unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
---

# ServiceRadar

### Monitor, Alert, Respond: Distributed Network Monitoring for Hard-to-Reach Environments


<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/carverauto/serviceradar" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<div class="justify-center items-center flex gap-4 mt-20">
    Press space for the next slide.
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

<div class="flex">

<div class="w-1/2">

# Agenda

1. **Introduction**
2. **Our Team**
3. **Business Overview**
4. **Market Opportunity**
5. **Value Proposition**
6. **Go-to-Market Strategy**
7. **Business Model**
8. **Financial Projections**

</div>

<div class="w-1/2 flex justify-center items-center">

<img src="/images/graph.svg" />

</div>

</div>

---
class: px-20
---

# Introduction

#### ***What is ServiceRadar***?

**Distributed Network Monitoring**: Open-source monitoring system designed for infrastructure and services in hard-to-reach places or constrained environments.

ServiceRadar enables organizations to monitor internal services with real-time insights and cloud-based alerting capabilities even during network outages, using its distributed agent-poller architecture.

**ServiceRadar Query Language (SRQL)**: Our custom query language allows powerful interrogation of network data with intuitive syntax, soon enhanced with LLM integration for natural language queries.

**Enhanced Visibility**: ServiceRadar provides comprehensive monitoring through:
- Timeplus Proton stream processing (90M EPS, 4ms latency)
- Network performance measurement with rperf
- SNMP integration for device monitoring
- Topology-aware monitoring for CLOS fabrics
- Secure communication with mTLS support

<!--

# Introduction

ServiceRadar: Transforming Monitoring in Constrained Environments

ServiceRadar is our platform built to monitor networks, services, and infrastructure in constrained
environments like edge networks, remote locations, and industrial settings. It provides real-time
monitoring through a distributed architecture of agents and pollers, with centralized analysis
and alerting.

What makes ServiceRadar unique is its ability to maintain monitoring capabilities during network
outages, thanks to its resilient architecture and store-and-forward model. It's designed to be
lightweight enough to run on minimal hardware while providing enterprise-grade monitoring features.

Our platform addresses critical monitoring challenges in industries ranging from telecommunications
to manufacturing, where traditional monitoring solutions often fail due to connectivity, resource,
or security constraints.

-->

---
class: px-20
transition: slide-down
---

<div class="flex">

<div class="w-1/2">

## Our Team

**Michael Freeman**  
*Co-Founder/CEO*

</div>

<div class="w-1/2 grid grid-cols-2 gap-4 items-start">

<img src="https://avatars.githubusercontent.com/u/1821930?v=4" class="w-full h-auto rounded shadow" alt="Michael Freeman"/>

</div>

</div>

---
class: px-20
---

# Business Overview

1. **ServiceRadar Core Platform**: A distributed, multi-layered architecture designed for flexibility, reliability, and security. It provides robust monitoring capabilities through lightweight agents, coordination pollers, and a centralized core service for data processing and alerts.

2. **Stream Processing Engine**: Powered by Timeplus Proton for high-performance data processing (90M EPS, 4ms latency, 1M unique key aggregation) on minimal hardware.

3. **SRQL Query Language**: Our custom ANTLR-based domain-specific language enables powerful data interrogation with upcoming LLM integration for natural language capabilities.

4. **Key Components**:
   - **Agent**: Runs on each monitored host, collects service status using minimal resources
   - **Poller**: Coordinates monitoring across agents, aggregates data
   - **Core Service**: Processes reports, triggers alerts, provides API
   - **Web UI**: Modern dashboard with visualization capabilities
   - **KV Store**: Dynamic configuration with NATS JetStream integration
   - **Specialized Checkers**: For SNMP, rperf network testing, topology monitoring

5. **Security-First Design**: All communications secured with mTLS, local API keys, and optional JWT authentication for multiple user tiers.

<!--

Why?

I first came up with the idea for ServiceRadar while working as a network engineer at a large telecommunications 
company. We constantly struggled with monitoring remote network equipment in areas with unreliable connectivity. 
Traditional monitoring solutions would either fail entirely or generate false alarms during brief network outages.

I started developing ServiceRadar as a solution to this problem, focusing on creating a lightweight, distributed
system that could maintain monitoring capabilities even in challenged network environments. After testing early
versions in several difficult monitoring scenarios, I realized we had built something unique - a robust monitoring
platform capable of operating where other solutions fail.

For our MVP, we've created a system that can monitor services across distributed locations with minimal resource
requirements while maintaining a centralized view. We expect to leverage this platform to provide monitoring
services across various constrained environments, from telecommunications to industrial IoT.

-->

---
class: px-20
---

# SRQL: ServiceRadar Query Language

**Natural language:** Which network links experienced packet loss in the last 24 hours?

**SRQL:** `FIND links WHERE packet_loss > 0 AND timestamp > now() - interval '24 hours'`

**Result:** Three backbone links reported packet loss exceeding threshold:
1. Core1-Edge3: 2.3% loss at 15:30
2. Core2-Transit1: 1.8% loss between 02:00-03:15
3. Edge1-Datacenter2: 3.1% loss at 21:45, correlated with maintenance window

**LLM Enhancement:** Our upcoming LLM integration will automatically translate natural language to SRQL, making complex queries accessible to all users, regardless of query language expertise.

**SRQL + Timeplus Proton:** Powered by Proton's high-performance stream processing (90M EPS, 4ms latency, 1M unique keys), SRQL can analyze massive datasets in near real-time, enabling instant insights into your infrastructure.

<!--
These are a few example queries that ServiceRadar can answer. The system is designed to understand natural language
queries and provide actionable insights based on the data it has ingested. The first example demonstrates how
ServiceRadar correlates packet loss events with topology and other events like maintenance windows. 

The second example shows topology-aware monitoring with ECMP balancing detection, which helps network engineers
quickly identify and resolve routing issues in data center fabrics. 

The third example illustrates ServiceRadar's comprehensive service monitoring capabilities with context awareness,
showing not just what services are down but providing additional context around the issues.
-->

---
class: px-20
---

# Market Opportunity

- 73% of network outages go undetected by traditional monitoring tools due to blind spots in remote locations and edge environments
- Global IT monitoring market expected to reach $62.7B by 2026, with industrial and edge monitoring growing at 19.3% CAGR
- Remote and edge network monitoring segment remains underserved with existing solutions being too resource-intensive, unreliable, or expensive
- Cost of network downtime averages $5,600 per minute, with 25% of outages occurring in hard-to-monitor environments
- ServiceRadar addresses the critical market gap for resilient monitoring in constrained environments, where traditional tools fail

<!--
After talking with potential customers, we discovered the biggest problem they face is maintaining visibility
into their networks and services in challenging environments. Traditional monitoring tools fail in these scenarios
because they're either too resource-intensive for edge deployment, too unreliable in unstable networks, or
too expensive to deploy comprehensively.

This creates a significant monitoring gap that leads to extended outages, missed SLAs, and wasted troubleshooting
time. ServiceRadar's distributed architecture specifically addresses these pain points, creating an immediate
opportunity to serve this underserved segment of the monitoring market.
-->

---
class: px-20
---

# Value Proposition

ServiceRadar sets itself apart through:

- **Powerful Query Engine**: SRQL enables precise, powerful data interrogation with upcoming LLM integration for natural language capabilities
- **High-Performance Stream Processing**: Built on Timeplus Proton, delivering 90M events per second with just 4ms latency
- **Distributed Resilience**: Agent-poller architecture allows local monitoring to continue during network outages with store-and-forward reporting once connectivity is restored
- **Resource Efficiency**: Lightweight agent runs on minimal hardware (even IoT/edge devices), using just 50MB RAM while providing enterprise-grade monitoring
- **Topology Awareness**: Unique CLOS fabric monitoring with ECMP path analysis and network flow visualization that traditional tools lack
- **Seamless Integration**: gRPC-based checkers enable easy extension for custom protocols and metrics without code changes
- **Zero-Trust Security**: mTLS encryption for all communications with SPIFFE/SPIRE integration for certificate management

<!--
Before ServiceRadar, organizations with distributed or constrained environments struggled with monitoring blind spots,
leading to costly outages and inefficient troubleshooting. Now, businesses can maintain visibility even in the most
challenging network conditions, dramatically reducing mean time to detection and resolution.

ServiceRadar's value proposition differs significantly from traditional monitoring tools that assume stable,
high-bandwidth connections and ample computing resources. Our technology specifically addresses monitoring challenges
in environments where these assumptions don't hold, providing reliable monitoring where other solutions fail.
-->

---
class: px-20
---

# Go-to-Market Strategy

**Target markets**: Telecommunications, Industrial IoT, Distributed Retail, Edge Computing, Remote Infrastructure

**Positioning**: The essential monitoring solution for environments where traditional tools fail

**Pricing**: Tiered open-source model with enterprise features and support
- Community Edition: Free, unlimited nodes, basic monitoring
- Professional: $89/month, enhanced features, email support
- Enterprise: $899/month, unlimited features, advanced security, priority support

**Marketing and Sales**: Open-source community building, targeted outreach to industries with distributed infrastructure challenges

**Partnerships**: Technology integration with edge hardware providers, telecommunications equipment providers

<!--
Our go-to-market strategy targets organizations struggling with monitoring distributed infrastructure in
challenging environments. We're focused on building an open-source community first, demonstrating value, and
then converting users to paid tiers based on feature needs and support requirements.

Our pricing model acknowledges that organizations may have hundreds or thousands of monitoring points, so we've
created a model that scales with feature usage rather than node count, making comprehensive monitoring economically
viable even for large distributed networks.

By partnering with edge hardware providers and telecommunications equipment manufacturers, we'll ensure ServiceRadar
is available as a pre-integrated solution in the environments where it delivers the most value.
-->

---
class: px-20
transition: fade
---

# Business Model

- Open-source core with tiered commercial offerings (Community, Professional, Enterprise)
- Subscription revenue from professional support and enterprise features
- Value-based pricing with no per-node fees, encouraging comprehensive deployment
- Enterprise deployments with custom SLAs and dedicated support
- Cloud-hosted option (SaaS) for organizations preferring managed solutions
- Training and integration services revenue stream

<!--

Open-Source Core with Commercial Offerings:

At the foundation of our business model is an open-source core that provides essential monitoring functionality. This
creates community engagement, accelerates adoption, and builds trust in our solution's capabilities. Our tiered
commercial offerings (Professional and Enterprise) enhance this core with additional features, support, and services.

Value-Based Pricing Strategy:

We've deliberately avoided the industry-standard per-node pricing model that punishes comprehensive monitoring. Instead,
our pricing is based on feature tiers and support levels, allowing organizations to monitor their entire infrastructure
without budget constraints forcing monitoring gaps.

Enterprise Deployments and SaaS Options:

For larger organizations, we offer enterprise deployments with custom SLAs, dedicated support channels, and integration
assistance. Additionally, our cloud-hosted SaaS option provides a turn-key solution for organizations that prefer
managed services over self-hosting.

Training and Services:

As monitoring in constrained environments often requires specialized knowledge, we provide training and integration
services to help customers maximize the value they receive from ServiceRadar. This creates an additional revenue
stream while ensuring customer success.

Our business model is designed for sustainable growth while maintaining the open-source ethos that makes ServiceRadar
accessible to organizations of all sizes. By focusing on value-based pricing and multiple revenue streams, we've
positioned ServiceRadar for long-term financial success.

-->

---
class: px-20
transition: fade-out
---

# Financial Projections

**Revenue Streams**: Multiple paths to monetization based on value delivery
- Community Edition: Building user base and community contributions
- Professional: Primary revenue source for small/medium deployments ($89/month)
- Enterprise: High-value customized deployments ($899-$1299/month)
- Services: Implementation, training, custom development

**Market Capture Strategy**: Target 10% of the underserved distributed monitoring segment within 3 years
- Year 1: 100 paying customers, $230K ARR
- Year 2: 500 paying customers, $1.2M ARR
- Year 3: 1,500 paying customers, $3.8M ARR

**Growth Drivers**: Industry partnerships, geographical expansion, feature enhancement for specialized vertical markets

<!--
Revenue Streams and Market Potential:

With the global IT monitoring market exceeding $30 billion and growing rapidly, ServiceRadar is positioned to capture
a meaningful share of the underserved distributed monitoring segment. Our multi-tier revenue model allows us to
monetize different customer segments while continuing to grow our open-source community.

Financial Trajectory:

Our projections show a clear path to $3.8M ARR by year three, based on conservative adoption rates within our target
verticals. The Professional tier will drive initial revenue growth, while Enterprise deployments will increase
average contract value in years 2-3 as we demonstrate success in complex monitoring environments.

Cost Structure and Profitability:

As an open-source solution with a relatively light infrastructure footprint, our margin structure is favorable compared
to traditional SaaS businesses. We anticipate reaching profitability in month 20, with customer acquisition costs
offset by our community-driven adoption model and industry partnerships.

Our financial strategy emphasizes sustainable growth over rapid expansion, ensuring we can maintain product quality
and support excellence while scaling the business. This approach aligns with our long-term vision of becoming the
standard for monitoring in constrained environments.

-->

---
class: px-20
---

# Thank You!

<!-- 
Thank you for taking the time to learn more about ServiceRadar. We're excited about the
opportunity to transform how organizations monitor their distributed networks and services
in challenging environments.
-->