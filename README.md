# Dhanush C P

**AI Systems Engineer & Systems Builder** — Bengaluru, India  
Designing low-latency agent architectures, high-throughput telemetry pipelines, and resilient production systems.

I build software architectures that operate under real-world constraints — from sub-150ms deterministic agent runtimes with OS-level spatial awareness to high-frequency IoT telemetry platforms ingesting raw binary TCP packets. My engineering focus is on deterministic execution over cognitive overhead, strict state synchronization, and observable self-hosted infrastructure.

[Website](https://chandes.in/) · [LinkedIn](https://www.linkedin.com/in/dhanush-c-p/) · [Email](mailto:dhanushchande@gmail.com)

---

## What I Build

- **Low-Latency Agent Runtimes**: Single-turn deterministic execution pipelines, local OS fast-lanes (<50ms regex dispatch), semantic context pruning (>80% token reduction), and thread-safe WAL memory stores with exponential half-life decay.
- **Real-Time Telemetry & Systems**: High-frequency industrial GPS socket ingestion (GT06, TK103, JT808), sub-meter PostGIS geofencing, and multi-tier state synchronization surviving mobile network drops.
- **Multimodal & Generative Pipelines**: Dual audio-visual extraction systems (Video LLaVA + Whisper ASR) and subject-identity-preserving diffusion workflows (OmniGen + LoRA), validated by peer-reviewed research.

---

## Featured Systems & Projects

### 1. Sakura — Desktop Agentic AI Operations Platform
*Ultra low-latency desktop companion & deterministic execution pipeline*

- **The Problem**: Traditional autonomous agents rely on sluggish, non-deterministic multi-turn cognitive loops and unbounded context windows that bloat latency (>5–10s) and token costs.
- **What I Built**: A desktop AI assistant with spatial operating system awareness (active window focus, clipboard, screen context) engineered for sub-second execution and minimal memory footprint.
- **Engineering Highlights**:
  - **Local Regex Fast Lane (<50ms)**: Bypasses LLM inference entirely for common OS queries and commands.
  - **OneShotRunner (<150ms)**: Single-turn deterministic parameter extraction powered by Groq LLaMA models, with graceful fallback to a bounded 4-turn ReAct planner only when multi-step synthesis is required.
  - **Context Pruning Engine**: Dynamically scores and compresses working context, slashing token consumption by **80%+**.
  - **World-Graph Memory Architecture**: Consolidated thread-safe SQLite database in Write-Ahead Logging (WAL) mode (`sakura.db`) with an exponential 48-hour half-life recency decay and active-directory relevance boosting.
- **Stack**: Python, FastAPI, Tauri, Svelte, LangChain, SQLite (WAL), Groq (LLaMA 3, Whisper), Kokoro TTS, FAISS
- **Links**: [Repository](https://github.com/chande-dhanush/Sakura)

### 2. TrackSavvy — Production Fleet Telemetry Platform
*High-performance fleet intelligence & multi-protocol GPS ingestion engine*

- **The Problem**: Vehicle tracking across fragmented cellular connectivity requires fault-tolerant ingestion of diverse proprietary hardware protocols, real-time geofence alerting, and instant state recovery during network drops.
- **What I Built**: An end-to-end telemetry and logistics platform operating in self-hosted production for a 50-bus fleet across Bengaluru, covering the entire lifecycle from SIM/TCP configuration to transport manager portals and parent apps.
- **Engineering Highlights**:
  - **Multi-Protocol TCP Decoding**: Low-level socket decoders parsing raw binary and ASCII frames from GT06, TK103, and JT808 trackers with monotonic timestamp validation and replay protection.
  - **Geospatial Time-Series Database**: Optimized partitioned TimescaleDB hypertables and PostGIS geometry, sustaining **288,000+ daily writes** with sub-5ms cache read bounds.
  - **3-Tier Synchronization Topology**: Combines low-latency WebSockets, in-memory state caching, and database polling to ensure zero state loss across intermittent mobile connectivity.
  - **Sub-Meter Geofencing**: Polygon boundary triggers for arrival ETAs and student QR boarding rosters with holiday alert suppression.
- **Stack**: Node.js, TypeScript, TimescaleDB, PostGIS, TCP Sockets, WebSockets, Docker, Nginx, Cloudflare
- **Links**: [Live Platform](https://tracksavvy.in) · [Portal Login](https://live.tracksavvy.in/login) *(Proprietary Production Platform at Tech Savvy)*

### 3. Multimodal Video Summarization Pipeline
*Dual-stream audio-visual ingestion & synthesis architecture*

- **The Problem**: Summarizing dynamic video content accurately requires simultaneously capturing fast-moving visual frames and asynchronous audio speech without losing semantic coherence.
- **What I Built**: An end-to-end multimodal pipeline that decouples visual frame extraction from audio speech channels, synchronizes the modalities, and generates unified summaries. Developed through research at Samsung Research Institute (PRISM Track).
- **Engineering Highlights**:
  - Dual-modal architecture combining Video LLaVA visual streams with Whisper ASR speech transcripts.
  - Integration with Falcons AI text summarization and a reactive interface.
  - Research outcomes published as a formal **Springer Nature book chapter** on Generative AI; recipient of the **Samsung PRISM Certificate of Excellence**.
- **Stack**: Python, PyTorch, Video LLaVA, Whisper ASR, Transformers, Falcons AI, React
- **Links**: [Repository](https://github.com/chande-dhanush/Video-Summarization)

### 4. Subject-Identity-Preservation Pipeline
*Diffusion-based contextual variation with structural identity lock*

- **The Problem**: Standard diffusion models alter subtle facial features and structural geometry when generating contextual background variations.
- **What I Built**: A generative vision pipeline using OmniGen and LoRA fine-tuning paradigms to retain subject facial features, proportions, and style consistency across extreme lighting and pose variations.
- **Stack**: Python, PyTorch, OmniGen, LoRA, Stable Diffusion, Diffusers
- **Links**: [Repository](https://github.com/chande-dhanush/Subject-Identity-Preservation)

---

## Technical Focus

| Domain | Technologies & Implementations |
| :--- | :--- |
| **AI & Autonomous Agents** | Single-turn OneShotRunner, Bounded ReAct planning, Semantic context pruning, Memory decay scoring (48h half-life), FAISS vector search, Groq (LLaMA 3, Whisper STT), Gemini API, LangChain |
| **Backend & Systems** | FastAPI (Async), Node.js, TypeScript, Python, Rust (systems exploration), SQLite (WAL mode + RLock), TCP binary sockets, WebSockets, Tauri desktop IPC |
| **Data & Telemetry** | TimescaleDB (partitioned hypertables), PostGIS (spatial geometry & geofencing), PostgreSQL, Raw packet decoding (GT06, JT808, TK103) |
| **Infrastructure & DevOps** | Docker, Self-hosted Linux environments, Cloudflare Tunnels, Nginx, n8n workflow automation, AWS |
| **Frontend & Clients** | Svelte, React, Tailwind CSS |

---

## Currently Exploring

- **Low-level systems programming in Rust** (`evie` project) for deterministic, zero-overhead memory and concurrency management in streaming engines.
- **Deterministic local agent runtimes** — exploring smaller distilled local models (<3B parameters) paired with strict AST/regex routers to further decrease agent execution latency on consumer hardware.

---

## Verified Links & Contact

- **Website**: [chandes.in](https://chandes.in/)
- **LinkedIn**: [linkedin.com/in/dhanush-c-p](https://www.linkedin.com/in/dhanush-c-p/)
- **Live System**: [tracksavvy.in](https://tracksavvy.in)
- **Direct Email**: [dhanushchande@gmail.com](mailto:dhanushchande@gmail.com)
