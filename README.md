
# 🚀 Netpad: Time-Aware Collaboration & Sharing Platform

> **Your data. Your timeline. Your control.**

Netpad is a self-hosted, real-time collaboration platform that has grown beyond live sync. With built-in temporal navigation, Netpad now treats *time* as a first-class citizen, letting you rewind, replay, and reconstruct the entire arc of your work. It’s like version control for everything, code, notes, conversations, media, without the complexity or silos.

Whether you're a family sharing moments, a dev team iterating on ideas, or a research group preserving provenance, Netpad helps you stay in sync *and* in control, with full historical visibility.

---

## 🌟 What Sets Netpad Apart

Most collaboration tools treat history as a secondary feature. Netpad makes it core:

- **🗓️ GitHub-Style Activity Maps** – Visualize when and how work happens
- **🕹️ Timeline Scrubbing** – Glide through your project’s history like a video
- **🧭 Quantum Navigation** – Step through precise changes with full fidelity
- **♻️ State Reconstruction** – Instantly rebuild the state of any moment in time

All backed by a privacy-first, zero-cloud architecture that keeps your data where it belongs, on your machines, under your rules.

---

## 🛠️ Core Capabilities

### 🧠 Time-Aware Collaboration
- **Contribution Maps**: Visual heatmaps of activity across days and months
- **Day & Hour Navigation**: Explore work at any granularity
- **Event-Level Stepping**: Jump backward or forward through individual changes
- **Recover, Rewind, Relearn**: Perfect for debugging, retrospectives, or postmortems

### ⚡ Real-Time Sync
- **WebSocket Architecture**: Millisecond-latency updates with full-duplex channels
- **Register-Based Collaboration**: Avoid overwrites; work in parallel with clarity
- **Live vs Timeline Mode**: Move fluidly between active collaboration and historical review

### 🔐 Privacy by Design
- **Fully Self-Hosted**: No SaaS, no spying, no third-party lock-in
- **Immutable Event Store**: Append-only logs ensure auditability and integrity
- **REQ Header Pattern**: Secure, base64-encoded metadata in transport, no leaky URLs
- **No Telemetry**: Zero analytics, zero tracking, zero compromise

---

## UI Screenshot

<img width="800" height="627" alt="Stargate_basic_screenshot" src="https://github.com/user-attachments/assets/1e284796-fe6d-4716-bb14-a6c2e1d01058" />









## 🧱 Architecture Overview

### Backend (Bun + TypeScript)
```
EventStore (LibSQL) → TimeMapCalculator → StateReconstructor
     ↓                        ↓                    ↓
WebSocket Server → Message Broadcasting → Client Updates
```

### Frontend (DiamondJS 2.2.4)
```
TimeMap → DayScrubber → QuantumNavigator
   ↓           ↓              ↓
MessageBus → CollaborationService → UI Components
```

### Feature Stack
- **🔁 Event Sourcing** – Every change is an atomic event
- **⚡ Smart Caching** – Instant, in-memory navigation via LRU strategies
- **🔍 Integrated Search** – Powered by MiniSearch for blazing-fast lookup
- **🧩 Modular Components** – Clean service-oriented architecture

---

## 🎯 Use Cases

### 👨‍💻 Dev Teams
- **Time-Travel Debugging** – Trace how issues evolved across time
- **Context-Rich Code Reviews** – Understand the "why" behind the "what"
- **Infra Drift Tracking** – Monitor and reconstruct config changes

### 🔬 Researchers & Analysts
- **Reproducibility by Default** – Every step, timestamped and restorable
- **Parallel Inquiry** – Multiple researchers, no conflict
- **Compliance & Audit** – Full history of data access and modifications

### 🎨 Creative & Media Teams
- **Nonlinear Iteration** – Skip versions, branch ideas, preserve forks
- **Asset Commentary** – Annotate visuals, scripts, footage in real-time
- **Process Memory** – Review your creative journey from start to finish

---

## 🚀 Getting Started

```bash
# Prerequisites: Bun runtime (https://bun.sh)

# Clone and install
git clone <repository-url>
cd Netpad
bun install

# Development (hot reload)
bun run dev

# Production
bun run build && bun run server
```

Access Netpad at: `https://localhost:5900`

---

## 🤔 Why "Time-Aware"?

Most tools trap you in the present. Netpad unlocks the past.
Ideas evolve. Bugs emerge. Insights fade. With Netpad, you don’t just *collaborate in real time*, you can *retrace the path that got you there.*

This isn’t just about syncing faster. It’s about remembering better.

---

## 📄 License

Licensed under **AGPLv3** ,  Ensuring Netpad remains open, forkable, and community-driven.

**Ready to sync, rewind, and replay?** Netpad is your portal. 🚪✨
