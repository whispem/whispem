# Hi, I'm Emilie 👋🏼

**Rust Developer · Storage Systems · Community Builder**

[![Rust](https://img.shields.io/badge/Rust-1.75+-orange?logo=rust&logoColor=white)](https://www.rust-lang.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub followers](https://img.shields.io/github/followers/whispem?style=social)](https://github.com/whispem)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/company/rust-aix-marseille-ram/)
[![Discord](https://img.shields.io/badge/Discord-Join_RAM-5865F2?logo=discord&logoColor=white)](https://discord.gg/sXr9ZqBJ)

From literature & linguistics to building distributed storage engines in Rust — my journey proves that curiosity and persistence matter more than background.

---

## 🦀 Current Focus

**Building storage systems from first principles**  
I'm exploring how databases work under the hood by implementing core concepts: segmented logs, LSM trees, compaction strategies, and distributed architectures.

**Latest project:** [**mini-kvstore-v2**](https://github.com/whispem/mini-kvstore-v2)  
A production-ready key-value store with HTTP REST API, built in 3 weeks while learning Rust.

[![CI](https://img.shields.io/github/actions/workflow/status/whispem/mini-kvstore-v2/ci.yml?branch=main&label=CI&logo=github)](https://github.com/whispem/mini-kvstore-v2/actions)
[![Production Ready](https://img.shields.io/badge/status-production_ready-success)](https://github.com/whispem/mini-kvstore-v2)
[![Docker](https://img.shields.io/badge/docker-ready-2496ED?logo=docker&logoColor=white)](https://github.com/whispem/mini-kvstore-v2/blob/main/Dockerfile)
[![Performance](https://img.shields.io/badge/writes-240K_ops%2Fs-brightgreen)](https://github.com/whispem/mini-kvstore-v2#benchmarks)
[![Performance](https://img.shields.io/badge/reads-11M_ops%2Fs-brightgreen)](https://github.com/whispem/mini-kvstore-v2#benchmarks)

- 🔐 Append-only segmented logs with crash recovery
- ⚡ In-memory indexing for O(1) lookups  
- 🗜️ Manual compaction with space reclamation
- 🌐 Async HTTP API (Axum + Tokio)
- 🐳 Docker-ready with multi-node deployment
- 📊 ~240K writes/sec, ~11M reads/sec on M4

**Timeline:**  
📅 Started Rust: October 27, 2025  
🚀 Shipped mini-kvstore-v2: November 21, 2025  
📝 [Read the learning journey →](https://github.com/whispem/mini-kvstore-v2/blob/main/JOURNEY.md)

---

## 🌱 What I'm Learning

Currently exploring:
- **Distributed systems** — consensus protocols, replication, partitioning
- **Storage engines** — LSM trees, write-ahead logs, bloom filters
- **Systems programming** — async Rust, zero-copy I/O, performance profiling
- **Community building** — organizing [Rust Aix-Marseille (RAM)](https://www.linkedin.com/company/rust-aix-marseille-ram/)

**Resources I'm working through:**
- [Database Internals](https://www.databass.dev/) by Alex Petrov
- [Designing Data-Intensive Applications](https://dataintensive.net/) by Martin Kleppmann
- [The Rust Book](https://doc.rust-lang.org/book/) (repeatedly)

---

## 🛠️ Tech Stack

**Primary:**  
`Rust` · `Swift` · `SwiftUI`

**Storage & Systems:**  
Append-only logs · LSM trees · In-memory indexing · Segment compaction

**Async & APIs:**  
`Tokio` · `Axum` · REST · HTTP/2

**Tools:**  
`Docker` · `k6` · `Criterion` · `GitHub Actions`

**Learning:**  
Distributed consensus · gRPC · Prometheus metrics · Web Assembly

---

## 📂 Featured Projects

### [mini-kvstore-v2](https://github.com/whispem/mini-kvstore-v2) 🦀
**Production-ready segmented key-value store with HTTP API**

Built as a deep dive into storage engine fundamentals:
- Append-only logs with automatic rotation
- In-memory HashMap index for instant lookups
- CRC32 checksums for data integrity
- Background compaction (space reclamation)
- Async HTTP server with health checks & metrics
- Comprehensive test suite + benchmarks

**Tech:** Rust, Axum, Tokio, Docker  
**Highlights:** 364 commits in 3 weeks, 240K writes/sec, CI/CD pipeline

📖 [Read JOURNEY.md](https://github.com/whispem/mini-kvstore-v2/blob/main/JOURNEY.md) — 3 weeks from "what's a borrow checker?" to shipping a working storage engine

---

### Earlier Projects

#### [mini-kvstore (v1)](https://github.com/whispem/mini-kvstore)
First attempt at persistent storage — taught me where design choices break and how to redesign them.

#### [CSV-Key-Value-Store](https://github.com/whispem/CSV-Key-Value-Store)
Lightweight experiment using CSV as persistence — great for understanding abstraction boundaries.

#### [DNA Helix Visualization](https://github.com/whispem/DNA-Helix-3D-Visualization)
SwiftUI-based 3D DNA structure — crossover between science, art, and animation.

#### [LunarView](https://github.com/whispem/LunarView)
Exploration of lunar motion and lighting in SwiftUI.

---

## 🌍 Community & Writing

### Rust Aix-Marseille (RAM)
Co-organizing monthly meetups for Rust developers in southern France.

🔗 [LinkedIn Company Page](https://www.linkedin.com/company/rust-aix-marseille-ram/)  
💬 [Discord Server](https://discord.gg/sXr9ZqBJ)  
🎯 **Goal:** Build a welcoming local community for Rust learners and experts

### Recent Posts

**Reddit:**
- [3 weeks into Rust: Built a segmented log KV store](https://www.reddit.com/r/rust/comments/1p0foo8/3_weeks_into_rust_built_a_segmented_log_kv_store/) 
- [Follow-up: HTTP API + production features](https://www.reddit.com/r/rust/comments/1p2vmi6/followup_built_a_segmentedlog_storage_engine_3/)

**LinkedIn:**
- [Building storage systems from scratch](https://www.linkedin.com/feed/update/urn:li:activity:7396839801146085376/)
- [Learning journey reflections](https://www.linkedin.com/feed/update/urn:li:activity:7397583761036681219/)
- [RAM meetup launch announcement](https://www.linkedin.com/feed/update/urn:li:activity:7398990773125414912/)

---

## 💭 Philosophy

> *"The best way to learn is to build."*

I believe in:
- **Learning in public** — sharing the messy middle, not just polished results
- **Building from first principles** — understanding how things work by implementing them
- **Community over competition** — we learn faster together
- **Clarity over cleverness** — simple, well-documented systems that make sense

Coming from literature means I think about code as communication:  
Structure determines outcome. Precision isn't optional. Systems should tell their own story.

---

## 🎯 2026 Goals

**Technical:**
- [ ] Implement distributed consensus (Raft)
- [ ] Build a working LSM-tree storage engine
- [ ] Contribute to production Rust projects (Signal-iOS, sled, others)
- [ ] Write-ahead log implementation with crash guarantees

**Community:**
- [ ] Host 12 Rust meetups in Aix-Marseille
- [ ] Mentor 5+ developers new to Rust
- [ ] Write technical blog series on storage engines
- [ ] Speak at a Rust conference

**Learning:**
- [ ] Complete "Database Internals" with implementation examples
- [ ] Master async Rust patterns
- [ ] Understand distributed tracing & observability
- [ ] Explore WebAssembly compilation targets

---

## 📬 Connect

- **GitHub:** [github.com/whispem](https://github.com/whispem)
- **LinkedIn:** [linkedin.com/in/emilie-peretti](https://www.linkedin.com/in/your-profile)
- **X/Twitter:** [twitter.com/whisp_em](https://twitter.com/whisp_em)
- **HuggingFace:** [huggingface.co/whispem](https://huggingface.co/whispem)
- **Email:** `contact.whispem@gmail.com`

**Rust Aix-Marseille:**
- **Discord:** [discord.gg/sXr9ZqBJ](https://discord.gg/sXr9ZqBJ)
- **LinkedIn:** [Rust Aix-Marseille](https://www.linkedin.com/company/rust-aix-marseille-ram/)

---

## 🗺️ Background

**Education:**  
Italian Studies — Aix-Marseille University

**Journey:**  
Literature → Languages → Structure → Systems → Storage Engines

I came to programming through linguistics — the study of how meaning emerges from structure. 
Turns out, distributed systems and grammar have more in common than you'd think.

**What changed:**  
Realized that computer science is fundamentally about designing clear, predictable systems. 
My background in analyzing structure and meaning translates directly to writing good code.

**Timeline:**
- 🎓 Studied Italian literature & linguistics
- 🔄 Discovered programming through technical writing
- 📱 Built iOS apps with Swift/SwiftUI
- 🦀 Oct 2025: Started learning Rust
- 🚀 Nov 2025: Shipped first production Rust project
- 🤝 Nov 2025: Launched Rust Aix-Marseille community

---

## ⭐ Support My Work

If you find my projects helpful:
- ⭐ **Star the repositories** — helps others discover them
- 🐛 **Open issues** — feedback makes everything better
- 🤝 **Contribute** — PRs welcome on all projects
- 📢 **Share** — tell others about [Rust RAM](https://discord.gg/sXr9ZqBJ)

---

**"Structure determines outcome. Precision isn't optional. You learn by building."**

*Building in public, learning from first principles, sharing the journey.*
