<div align="center">

# Dhanush C P

**AI Systems Engineer & Systems Builder** — Bengaluru, India  
*Designing low-latency agent architectures, high-throughput telemetry pipelines, and resilient production systems.*

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-chandes.in-10b981?style=for-the-badge&logo=googlechrome&logoColor=white)](https://chandes.in/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-dhanush--c--p-0284c7?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dhanush-c-p/)
[![Live Telemetry](https://img.shields.io/badge/Live_System-Track_Savvy-059669?style=for-the-badge&logo=speedtest&logoColor=white)](https://tracksavvy.in)
[![Email](https://img.shields.io/badge/Email-dhanushchande%40gmail.com-6366f1?style=for-the-badge&logo=gmail&logoColor=white)](mailto:dhanushchande@gmail.com)

</div>

---

## 📌 Executive Summary

I design and build complete software architectures operating under real-world physical and computational constraints. My core focus spans **low-latency autonomous agent runtimes** and **high-throughput industrial IoT telemetry platforms**.

Rather than treating AI as an isolated black box, I engineer systems around it—focusing on deterministic single-turn execution, semantic context pruning, spatial OS awareness, and fault-tolerant state synchronization over unstable networks. Currently a Software Engineer at **Tech Savvy** owning the Track Savvy telematics infrastructure, architect of **Sakura**, and published Generative AI researcher with **Springer Nature** from work at **Samsung Research Institute**.

---

### ⚡ Quick Benchmarks & Production Evidence

| Metric / Benchmark | System & Production Context | Engineering Implementation |
| :--- | :--- | :--- |
| **288k+ Daily Rows** | **Track Savvy** (Live 50-Bus Fleet) | Custom binary/ASCII TCP socket decoders, partitioned TimescaleDB hypertables |
| **< 150ms Latency** | **Sakura** (Desktop Agent Runtime) | Single-turn `OneShotRunner` parameter extraction with `<50ms` OS regex fast-lane |
| **80%+ Token Saved** | **Sakura** (Context Pruning Engine) | Dynamic semantic context pruning eliminating repetitive multi-turn loop costs |
| **Springer Nature** | **Samsung PRISM** Research Track | Published Generative AI book chapter on audio-visual multimodal summarization |

---

## 🛠️ Featured Engineering Systems

### 🔹 [Sakura](https://github.com/chande-dhanush/Sakura) — Desktop Agentic AI Operations Platform
> **Ultra low-latency desktop companion & deterministic execution pipeline**  
> `Python` `FastAPI` `Tauri` `Svelte` `SQLite WAL` `Groq (LLaMA 3, Whisper)` `Kokoro TTS`

- **The Problem**: Multi-turn cognitive loops and unbounded context windows create sluggish (>5s) and token-expensive agent interactions.
- **Architectural Solution**:
  - **Local Regex Fast Lane (<50ms)**: Bypasses LLM inference entirely for common OS queries & desktop actions.
  - **OneShotRunner (<150ms)**: Single-turn deterministic parameter extraction via Groq LLaMA models (with fallback to a bounded 4-turn ReAct planner only when required).
  - **80%+ Token Pruning**: Dynamic relevance scoring compresses working context prior to LLM calls.
  - **Thread-Safe Memory (`sakura.db`)**: Single SQLite WAL store with an exponential 48-hour half-life decay.
- **Link**: [📦 Explore GitHub Repository](https://github.com/chande-dhanush/Sakura)

---

### 🔹 Track Savvy — Production Fleet Telemetry Platform
> **High-frequency IoT telemetry & multi-protocol GPS ingestion engine**  
> `Node.js` `TypeScript` `TimescaleDB` `PostGIS` `TCP Sockets` `WebSockets` `Docker` `Cloudflare`

- **The Problem**: Managing vehicle tracking across spotty mobile networks requires zero-loss packet decoding and rapid state synchronization.
- **Architectural Solution**:
  - **Multi-Protocol TCP Sockets**: Custom low-level decoders for GT06, TK103, and JT808 trackers with monotonic validation.
  - **TimescaleDB + PostGIS**: Partitioned hypertables and spatial indexing handling **288k+ daily writes** with sub-5ms cache bounds.
  - **3-Tier State Sync**: Resilient topology combining WebSockets, in-memory caching, and fallback polling to survive mobile network drops.
  - **Sub-Meter Geofencing**: Real-time arrival ETA predictions and student QR boarding verification for a 50-bus fleet.
- **Links**: [🌐 Live Platform (tracksavvy.in)](https://tracksavvy.in) · [🔑 Management Portal](https://live.tracksavvy.in/login) *(Self-Hosted Production Platform)*

---

### 🔹 [Multimodal Video Summarization](https://github.com/chande-dhanush/Video-Summarization) — Dual-Stream Pipeline
> **Audio-visual frame & speech synthesis architecture**  
> `PyTorch` `Video LLaVA` `Whisper ASR` `Transformers` `Falcons AI` `React`

- **The Problem**: Summarizing dynamic video content requires simultaneously capturing fast visual changes and continuous audio speech without losing semantic coherence.
- **Architectural Solution**:
  - Decoupled multimodal ingestion separating visual frame extraction from audio speech transcripts before joint semantic synthesis.
  - Research conducted at **Samsung Research Institute (PRISM Track)**, resulting in a **Springer Nature book chapter publication** and **Samsung Certificate of Excellence**.
- **Link**: [📦 Explore GitHub Repository](https://github.com/chande-dhanush/Video-Summarization)

---

### 🔹 [Subject-Identity-Preservation](https://github.com/chande-dhanush/Subject-Identity-Preservation) — Diffusion Pipeline
> **Contextual variation engine with structural identity lock**  
> `PyTorch` `OmniGen` `LoRA` `Stable Diffusion` `Diffusers`

- **The Problem**: Generative image diffusion models distort subtle facial structures and identity when contextual backgrounds vary.
- **Architectural Solution**:
  - Built an identity-locking pipeline using OmniGen and LoRA fine-tuning paradigms to retain facial geometry across diverse poses and lighting.
- **Link**: [📦 Explore GitHub Repository](https://github.com/chande-dhanush/Subject-Identity-Preservation)

---

## 💻 Technical Arsenal

| Domain | Technologies & Implementations |
| :--- | :--- |
| **AI & Autonomous Agents** | Single-turn `OneShotRunner`, Bounded ReAct, Context Pruning, Memory Half-Life Decay, FAISS, Groq (LLaMA 3, Whisper), Gemini API |
| **Backend & Systems** | FastAPI (Async Python), Node.js, TypeScript, SQLite (WAL mode + RLock), TCP Sockets, WebSockets, Tauri IPC |
| **Data & Telemetry** | TimescaleDB (partitioned hypertables), PostGIS (spatial geometry), PostgreSQL, Industrial Protocol Decoders (GT06, JT808, TK103) |
| **DevOps & Infrastructure** | Docker, Self-Hosted Linux, Cloudflare Tunnels, Nginx, n8n Automation, AWS |
| **Frontend** | Svelte, React, Tailwind CSS |

---

## 🔬 Currently Exploring

- **Scaling Track Savvy Telemetry**: Expanding real-time fleet intelligence, automated arrival notification engines, and high-frequency route analytics in production.
- **Agentic IDEs & Developer Tooling**: Deep-diving into code-native AI developer environments — building custom autonomous skills, workspace rules, and Model Context Protocol (MCP) server integrations.
- **Deterministic Edge Runtimes**: Integrating compact distilled models with AST/regex fast-lanes for ultra-responsive local agent execution.

---

## 📬 Connect

- 🌐 **Portfolio**: [chandes.in](https://chandes.in/)
- 💼 **LinkedIn**: [linkedin.com/in/dhanush-c-p](https://www.linkedin.com/in/dhanush-c-p/)
- 📍 **Location**: Bengaluru, Karnataka, India
- ✉️ **Direct Email**: [dhanushchande@gmail.com](mailto:dhanushchande@gmail.com)
