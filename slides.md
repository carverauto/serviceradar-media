---
# try also 'default' to start simple
theme: dracula
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://cover.sli.dev
favicon: https://staging.threadr.ai/favicon.svg
# some information about your slides, markdown enabled
title: Carver Automation
info: |
  ## Carver Automation Pitch Book
  AI-Driven Analytics for Business Intelligence

  Learn more at [threadr.ai](https://staging.threadr.ai)
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

# ThreadR.ai

### Unlock Insights, Drive Decisions: The Future of Data Intelligence


<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/carverauto/threadr-pitch" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
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

#### ***What is ThreadR***?

**PaaS**: OpenSource AI-powered graph-based streaming ETL platform, hosted in the cloud or on-prem.

ThreadR enables businesses to analyze and derive insights from streaming data in real-time using
our ETL pipelines, knowledge graph, and Large Language Models (LLMs).

**ChatOps**: Real-time analytics for digital communication platforms built on top of our platform

ThreadR's ChatOps solution provides businesses with a powerful tool to analyze and manage digital
communications across platforms like Slack, Discord, Teams, and Telegram.

<!--

# Introduction

ThreadR: Transforming Data into Decisions

ThreadR is our platform we built to ingest streaming data and process it in real-time
using ETL pipelines, stored in a knowledge graph, and analyzed using Large Language Models.

We're able to enrich that data with expert systems of agents that can add insights and context to the data,
and we provide a natural language interface around that system.

This data can be anything from chat logs, emails, social media, rich media like audio, video, or images,
or any other large collections of data, like the Panama Papers. We're able to provide insights into the data
that would be impossible to get otherwise.

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

**Shruti Mantri**  
*Co-Founder/Platform*

**Kevin Olson**  
*Co-Founder/Front-End & API*

**Rutvik Tak**  
*Co-Founder/Mobile*

</div>

<div class="w-1/2 grid grid-cols-2 gap-4 items-start">

<img src="https://avatars.githubusercontent.com/u/1821930?v=4" class="w-full h-auto rounded shadow" alt="Michael Freeman"/>
<img src="https://avatars.githubusercontent.com/u/6594483?v=4" class="w-full h-auto rounded shadow" alt="Shruti Mantri"/>
<img src="https://avatars.githubusercontent.com/u/967369?v=4" class="w-full h-auto rounded shadow" alt="Kevin Olson"/>
<img src="https://avatars.githubusercontent.com/u/65209850?v=4" class="w-full h-auto rounded shadow" alt="Rutvik Tak"/>

</div>

</div>

<!-- 
What led us to this opportunity:

My journey into the tech world began in the early '90s, at the age of 13, diving headfirst into
the computer hacking and phreaking scene. I was one of the founders of the hacker collective known
as 'w00w00', where some of the members went on to create Napster, WhatsApp, CloudVolumes, and others. 
Kevin and I met through that group while in high school and have worked together on various projects
ever since.

Most recently, Kevin, Rutvik, and I worked together to build ChaseApp, an entertainment app that
released into both the Apple and Google app stores. I found Rutvik through social media and hired
him to help with the mobile development. Rutvik and I hit it off and have collaborated together 
over the past several years on various projects.

Kevin and I also most recently worked together at a threat intelligence company funded by In-Q-Tel. 
Kevin also created and developed Fume.App, a platform for serverless deployment of web applications and 
cloud functions.

Shruti is the newest member to our team and has been a great addition. Shruti and I worked together on
the Mage.AI opensource ETL orchestration tool, contributing several new features. 
Prior to that, she was an SRE at Amazon worked on the platform engineering team at Twitter.

-->

---
class: px-20
---

# Business Overview

ThreadR revolutionizes business analytics by employing streaming ETL pipelines to integrate data from
digital platforms into a dynamic knowledge graph. 

Enhanced with fine-tuned Large Language Models, our 
platform excels in deciphering complex communication patterns and offers users a powerful exploration 
and investigation tool. 

With ThreadR, querying your data becomes a natural process, enabling the discovery 
of actionable insights and facilitating strategic decisions with unprecedented ease and efficiency.

<!--

Why?

I first came up with the idea for ThreadR while I was working at VulnCheck on threat intelligence, 
specifically attribution around threat actors, their infrastructure, and also tracking exploit developers. 

The idea came back to me while working at my next job after my boss complained that he had no
idea what I was working on because he didn't have time to sit around and read Slack all day. 

I started to develop ThreadR as more than a side project and after running a few different prototype versions 
of it on various chat platforms, I realized that we had a very sophisticated chat bot and
analytics platform that combined the power of knowledge graphs, with natural language search 
in a way I hadn't seen before.

For our MVP we've set out to build a system that can analyze the relationships between users on a chat
platform and extract insights from the data. We expect that we can leverage this platform to provide
the same analytics services across other domains, such as social media, email, and collections from
law enforcement and defense.

-->

---
class: px-20
---

# Example Queries

**User:** What were the top 3 conversations of utmost importance over the last week?

**ThreadR:** 1. Search system was down for an hour in production impacting all the customers. The revenue impact is still uncertain.
2. We signed up with 3 new customers: ABC, DEF, and XYZ.

**User:** Does Jason from the Sales team know our Platform Engineer Mike?

**ThreadR:** There has been no direct communication between them, neither have they been part of the same thread. Hence, it is unlikely they know each other.

**User:** How many PagerDuty alerts fired over the last month along with their teamwise split?

**ThreadR:** There were 106 PagerDuty alerts in total that were fired. Here is the split:
- Platform team: 67
- DevOps team: 29
- Customer Support team: 10

<!--
These are a few example questions that ThreadR can answer. The system is designed to understand natural language
queries and provide actionable insights based on the data it has ingested. The first example is a query that
is in the form of a question and the system responds, an easy problem for the LLM to solve. This is a
summarization, classification, and ranking problem. The second example is a question about relationships
between users and the system responds with a summary of the data it has ingested. The third example is a
question about a specific event and the system responds with a summary of the data it has ingested.
-->

---
class: px-20
---

# Market Opportunity

- Gartner reports 47% of digital workers struggle to find information, and 32% make wrong decisions due to lack of awareness
- Rapid expansion of remote work and digital collaboration drives urgent need for advanced communication analysis solutions
- Slack AI customers save an average of 97 minutes per user each week, highlighting strong demand for AI-powered tools
- ThreadR addresses these critical needs with an AI-driven solution that simplifies management and analysis of complex digital communications

<!--
After talking with our potential customers, we found that the biggest problem they face is that they are
are either unable to keep up with the volume of messages or they are unable to find the information they
need when they need it. This leads to poor decisions and missed opportunities.
-->

---
class: px-20
---

# Value Proposition

ThreadR elevates data utility and insight discovery by:

- **Real-Time Insight**: Harness the power of real-time stream processing to capture and analyze data as events unfold, ensuring immediate access to insights that drive critical business decisions.
- **Sophisticated Data Transformation**: Utilize advanced ETL pipelines for seamless data integration and transformation, aligning diverse data sources with a dynamic knowledge graph schema for enriched analysis.
- **Deep Intelligence Enhancement**: Go beyond surface-level data interpretation to uncover profound relationships and insights, empowering organizations to leverage their data for strategic advantage and innovation.

<!--
Before ThreadR, organizations struggled with information silos, leading to costly oversights and missed 
opportunities. Businesses can now harness the power of AI-driven insights to enhance productivity, 
foster innovation, and stay ahead in today's rapidly evolving digital landscape
-->

---
class: px-20
---

# Go-to-Market Strategy

**Target market**: Businesses and organizations relying heavily on digital communication platforms

**Positioning**: The essential tool for managing and analyzing digital interactions across all platforms

**Pricing**: SaaS subscription model with tiered pricing based on data volume and feature set

**Marketing and Sales**: Inbound marketing, content marketing, targeted outreach to key decision-makers

**Partnerships**: Integrate with popular communication platforms and complementary tools

<!--
Our go-to-market strategy targets businesses drowning in digital communications, offering them a 
straightforward SaaS solution with flexible pricing. We're focused on cutting through the noise with 
direct marketing and sales efforts, targeting decision-makers who need our tool the most. By partnering 
with leading communication platforms, we ensure ThreadR integrates seamlessly into our clients' 
workflows, making it the essential tool for managing and analyzing digital interactions. 
-->

---
class: px-20
transition: fade
---

# Business Model

- SaaS subscription revenue
- Tiered pricing based on data volume and feature set
- Upsell opportunities for advanced features and customization
- Potential for enterprise-level contracts and custom solutions

<!--

SaaS Subscription Revenue:

At the core of our business model is a SaaS subscription structure. This ensures a steady, predictable 
revenue stream while providing our customers with continuous access to the latest in AI-driven communication
analysis.

Tiered Pricing Strategy:

We've designed our pricing with scalability in mind. Our tiered model is based on data volume and feature set, 
allowing businesses of all sizes to find a plan that suits their needs today, with the flexibility to grow tomorrow.

Upsell Opportunities:

Beyond the base subscription, we offer upsell opportunities for advanced features and customization. 
This not only caters to the specific needs of our customers but also opens additional revenue streams 
for our business.

Enterprise-Level Contracts:

There's a significant opportunity for enterprise-level contracts and custom solutions. These not only bring 
in higher revenue but also deepen our relationships with key customers, turning them into long-term partners.

Closing:

Our business model is built for growth, scalability, and customer satisfaction. By combining a flexible SaaS 
subscription model with tiered pricing and upsell opportunities, we're positioned to meet the market's needs 
today and adapt to its demands tomorrow. With the potential for enterprise contracts, we're ready to scale and 
innovate, ensuring ThreadR remains at the forefront of AI-driven communication analysis.

-->

---
class: px-20
transition: fade-out
---

# Financial Projections

**Competitive Pricing**: Entry at $89/month, scaling to $899-$1000 for enterprise solutions.

**Massive Market**: Targeting the 50M+ servers across Slack, Discord, Teams, Telegram for our ChatOps solution.

**Modest Goal**: Capturing a fraction (e.g., 0.0001%) translates to significant revenue.

**Growth Strategy**: Tiered pricing for scalability, upsell for advanced features, and custom enterprise solutions.

**Long-Term Vision**: Beyond initial capture, focusing on retention and expanding market share.

<!--
Market Size & Opportunity: 

With over 50 million servers across platforms like Slack, Discord, Teams, and Telegram, 
even a conservative market penetration of 0.0001% positions us for substantial revenue growth. 
This isn't just about numbers; it's about the untapped potential waiting for the right solution.

Pricing Strategy for Scalability: 
Our competitive pricing for our ChatOps service starts at $89/month, scaling up to $899-$1000 for 
enterprise solutions. This tiered approach not only makes our product accessible to a wide range 
of businesses but also aligns with our strategy to grow with our customers, maximizing lifetime value.

Growth and Scalability:

By focusing on a scalable SaaS model, we're not just aiming for initial sign-ups. Our strategy includes 
upselling advanced features and custom solutions, ensuring long-term growth and a steady increase in average 
revenue per user (ARPU).

-->

---
class: px-20
---

# Thank You!

<!-- 
Thank you for taking the time to learn more about Carver Automation and ThreadR. We're excited about the
opportunity to make strides in communication analysis.
-->
