---
layout: default
title: Projects
permalink: /projects/
---

[← Back to About](/)

# Projects

A collection of professional and personal projects spanning distributed systems, AI, fintech, and mobile applications.

---

### 1. Screen Share Understanding for Teams Copilot
**Microsoft** · *AI/ML*

Added reasoning over Teams screen share capability to Teams Copilot — enabling Copilot to understand and reference shared screen content during live meetings.

**Engineering challenge: data volume:** A single meeting generates ~60 minutes of continuous video, far too much to ingest into an LLM. Built a **key frame detection** pipeline that filters out minor visual changes and extracts only significant moments from the screen share feed. These key frames serve as a knowledge base. Extracted visual information from each key frame and used it as an indexing mechanism to determine which images to pass into the LLM context window.

**Model/Agentic challenge: quality measurement:** Visual information extraction from key frames required rigorous quality benchmarking. Developed a **quantitative evaluation framework** with curated test inputs: frames containing just text, bullet points, tables, titles, and pictures with text, paired with expected extraction outputs. LLM outputs are compared against expected results via similarity scoring to ensure quality is preserved when switching models or prompts. Ran experiments across multiple LLM models (GPT-3.5 Turbo, GPT-4o, GPT-4o mini, and other vision models) and custom image processing built with OpenCV, combined with prompt variations to measure their impact on extraction quality.

> ⚡ 4× GPU optimization

🔗 [Microsoft 365 Copilot Blog](https://techcommunity.microsoft.com/blog/microsoft365copilotblog/what%E2%80%99s-new-in-microsoft-365-copilot--february-2026/4496489#community-4496489-communities)

---

### 2. Attendee chat in Microsoft Teams Townhalls
**Microsoft** · *Hyperscale*

Architected and scaled the Microsoft Teams Events chat platform, one of the fastest-growing features in Teams. Designed for massive concurrency supporting 100K event participants with real-time chat capabilities in single townhall.

**Problem:** In Microsoft Townhalls, organizer-to-attendee communication is one-way — attendees had no way to express reactions or participate via chat. The existing backend chat stack supported only 1,000 members on the roster and ~1 msg/sec throughput, designed for low-frequency, heavy payloads like cards and attachments. Townhall chat is the opposite: high-frequency, lightweight messages at massive scale.

**Scale targets:** 100K attendees on the roster, ~5 msg/sec ingestion, with delivery fanout to all attendees in under 5 seconds.

**Solution:** Identified bottlenecks across the pipeline and designed systems to address each. On the **frontend service**, redesigned the ingestion layer to accept messages at a higher rate into a queue; a periodic job batches queued messages and sends a single batch to the delivery engine. For **delivery fanout** to 100K endpoints, replaced sequential delivery with a **region-based fanout** routing delivery to edge endpoints closest to each client machine, enabling horizontal scale and reducing end-to-end latency.

> 💰 ~$100M business impact &nbsp;·&nbsp; 👥 Millions of users

🔗 [Microsoft Support: Chat in a Town Hall](https://support.microsoft.com/en-us/office/chat-in-a-town-hall-in-microsoft-teams-a4a0e102-ca45-4605-a0a8-83a884547338)

`Distributed Systems` `Azure` `Real-time Messaging` `Event-Driven Architecture` `Message Batching` `Regional Fanout`

---

### 3. CreativeCubs — India Daily Gold Silver Prices
*Founder · Startup*

Founded CreativeCubs to solve my own problem — finding the current gold price in India. Built an Android gold price tracking and forecasting application from scratch, now serving ~500K monthly active users.

Built the full backend system on **Google Cloud** with self-healing infrastructure and monitoring systems to ensure high availability. The app features ML-based price predictions, real-time alerts, historical analytics, and a strong user feedback system that drives continuous improvement. Conducted customer surveys to understand the market and shape product direction.

> 👥 ~500K MAU

🔗 [Play Store](https://play.google.com/store/apps/details?id=org.chittu.gold) &nbsp;·&nbsp; [Website](https://indiagoldpriceapp.com/)

`Android` `Google Cloud` `ML Forecasting` `Self-Healing Systems` `Monitoring` `Product Design`

---

<details markdown="1">
<summary><h2 style="display:inline">Other Projects</h2></summary>

### 4. Search Analytics / Insights
**Microsoft** · *AI/ML*

Built an extensible AI-driven Search Insights platform across the Microsoft Exchange ecosystem. Enabled intelligent search analytics with real-time data processing and ML-powered relevance ranking.

`Search Infrastructure` `AI/ML` `Exchange Ecosystem` `Analytics`

---

### 5. Exchange Admin REST API
**Microsoft** · *Hyperscale*

Architected Microsoft Exchange Admin management APIs handling ~2M requests per day. Scaled the system to handle ~500K objects per tenant (up from 100K), enabling enterprise-grade administration at scale.

> 🖥️ ~2M requests/day &nbsp;·&nbsp; 📈 5× object scale

`REST APIs` `Azure` `High Availability` `Enterprise Scale`

---

### 6. Amazon Invoice Scaling
**Amazon** · *Hyperscale*

Scaled Amazon's vendor payments invoice-matching platform to handle 5× load. Reduced processing time by 90% while increasing throughput from 100 req/sec to 800 req/sec and cutting tp99 latency from 500ms to 100ms.

> ⚡ 800 req/sec throughput &nbsp;·&nbsp; ⏱️ 100ms tp99 latency

`AWS` `Performance Engineering` `Anomaly Detection` `Self-Healing Systems`

---

### 7. D.E. Shaw Order Latency Optimization
**D.E. Shaw** · *Low-Latency*

Reduced trading order placement latency from 1800µs to 800µs in D.E. Shaw's high-frequency trading infrastructure. Built a transactional persistence framework handling 100K TPS and scaled the trading universe from 5K to 100K instruments.

> ⚡ 800µs order latency &nbsp;·&nbsp; 🗄️ 100K TPS persistence

`Low-Latency Systems` `HFT Infrastructure` `Memory Optimization` `Java/C++`

---

### 8. Clanaway
*Startup · AI*

A trip planning app for groups of friends to coordinate and plan trips together. Features an AI trip assistant powered by OpenAI APIs that helps plan trip itineraries, with tool integration for itinerary actions like scheduling, and recommendations.

🔗 [App Store](https://apps.apple.com/us/app/clan-away-group-trip-helper/id6738758284) &nbsp;·&nbsp; [Website](https://app.clanaway.com/)

`Mobile App` `OpenAI APIs` `AI Assistant` `Tool Integration` `Full Stack`

---

### 9. AI Dad Jokes
*AI · Fun*

A visual dad jokes app that takes existing funny jokes and generates visual representations of them using AI. Combines humor with AI-generated imagery to bring dad jokes to life in a fun, shareable format.

🔗 [App Store](https://apps.apple.com/us/app/joke-a-day/id6736678054)

`AI Image Generation` `Visual Content` `Python`

---

### 10. Zcash Open Source Contributions
*Open Source · Crypto*

Contributed to the Zcash cryptocurrency project — a privacy-focused digital currency using zero-knowledge proofs (zk-SNARKs). Contributed to the open-source codebase and privacy-preserving transaction infrastructure.

`Blockchain` `Cryptography` `C++` `Zero-Knowledge Proofs`

---

### 11. Crypto Arbitrage — India Exchanges
*Crypto · Low-Latency*

Built an automated arbitrage detection and execution system for cryptocurrency price discrepancies across Indian exchanges. Monitored real-time price feeds across multiple exchanges and executed cross-exchange trades to capture spreads.

`Trading Systems` `Real-time Data` `Python` `Exchange APIs`

---

### 12. On-Chain Coin Arbitrage — Solana
*Crypto · DeFi*

Built on-chain coin arbitrage system on the Solana network. Developed new smart contracts in Rust to detect and execute arbitrage opportunities across decentralized exchanges with minimal latency.

`Solana` `Rust` `Smart Contracts` `DeFi` `Arbitrage`

---

### 13. SPY LEAP Options Strategy
*Quantitative Finance*

Analyzed and built a long-term investment strategy using SPY LEAP options. Conducted deep analysis of options pricing, to construct optimized LEAP positions for sustained returns.

🔗 [Backtest Results](https://www.quantconnect.cloud/backtest/ee9a7aec98e04469dc7b328ae71003f1/?theme=darkly) &nbsp;·&nbsp; [Analysis Document](https://docs.google.com/document/d/19rYie1x8gU-CBWogfko_Oz9vKora1cldZzIxzZZ6dcQ/edit?usp=sharing)

`Options Trading` `LEAP Strategy` `Quantitative Analysis` `SPY`

</details>

---

<p align="center">
  <a href="/">⬅️ <strong>Back to About</strong></a>
</p>
