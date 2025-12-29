# Hi, I'm Emilie 👋🏼

**Rust Developer · Distributed Storage Systems · Community Builder**

From literature & languages (italian & english) to building distributed storage engines in Rust — my journey shows that curiosity and persistence matter more than background.


## 🦀 Current Focus

**Building distributed storage engines from first principles**  
Working on consensus (Raft), atomic writes (2PC), sharding, durability (WAL), and cluster maintenance.

**Latest project:** [minikv](https://github.com/whispem/minikv)  
Production-ready distributed key-value store with Raft, strong consistency, sharding, and durability.

- Raft-based cluster coordination & failover
- Two-phase commit for distributed writes
- Write-Ahead Logging & durability
- In-memory indexes, Bloom filters, segmented logs
- gRPC and HTTP REST APIs
- Docker Compose deployment

**Timeline:**  
Started Rust: October 27, 2025  
Shipped mini-kvstore-v2: November 21, 2025  
Released minikv (distributed): December 2025  
[Read the learning journey →](https://github.com/whispem/mini-kvstore-v2/blob/main/JOURNEY.md)


## 🌱 What I'm Learning

Currently exploring:
- Distributed systems: consensus protocols, replication, partitioning
- Storage engines: LSM trees, write-ahead logs, bloom filters
- Systems programming: async Rust, performance profiling, crash consistency
- Community building: Rust Aix-Marseille (RAM), local events & mentoring

**Resources:**
- [Database Internals](https://www.databass.dev/) by Alex Petrov
- [Designing Data-Intensive Applications](https://dataintensive.net/) by Martin Kleppmann
- [The Rust Book](https://doc.rust-lang.org/book/)


## 🛠️ Tech Stack

**Languages:**  
Rust · Swift · SwiftUI

**Distributed Systems:**  
Raft consensus · 2PC · Sharding · WAL · Append-only logs

**Async & APIs:**  
Tokio · Axum · Tonic (gRPC) · REST

**Tools:**  
Docker · k6 · Criterion · GitHub Actions


## 📂 Featured Projects

### [minikv](https://github.com/whispem/minikv) 🦀
Production-ready distributed KV store with Raft, strong consistency, and WAL.

- Raft consensus (multi-node, metadata replication)
- 2PC distributed writes
- Sharding & N-way replication
- Write-ahead logging, Bloom filters, cluster repair tools
- CLI, HTTP and gRPC APIs

**Tech:** Rust, Tonic, Axum, Docker  
**Benchmarks:** 80K writes/sec, 8M reads/sec (cluster, M4)

### [mini-kvstore-v2](https://github.com/whispem/mini-kvstore-v2)
Segmented, append-only key-value store (single node)

- In-memory HashMap index
- CRC32 checksums, compaction, async HTTP API
- 240K writes/sec, 11M reads/sec


## 🌍 Community

**Rust Aix-Marseille (RAM):**  
Co-organizing monthly meetups for Rust developers in Southern France.  
[Discord Server](https://discord.gg/sXr9ZqBJ) • [LinkedIn](https://www.linkedin.com/company/rust-aix-marseille-ram/)


## 💭 Philosophy

> "The best way to learn is to build."

- Learning in public: share the process, not just the polished result
- Systems from first principles: implement, then understand
- Community over competition: learning is collective
- Clarity over cleverness: well-documented, maintainable code


## 🎯 Goals for 2026

**Technical:**
- [ ] Distributed consensus in production (Raft)
- [ ] LSM-tree engine built in Rust
- [ ] Contribute to major open-source Rust projects
- [ ] Crash-consistent logging

**Community:**
- [ ] 12 Rust meetups (Aix-Marseille)
- [ ] Mentor new developers
- [ ] Write technical blog series
- [ ] Speak at a Rust event


## 📬 Connect

- GitHub: [whispem](https://github.com/whispem)
- LinkedIn: [Emilie Peretti](https://www.linkedin.com/in/emilie-peretti)
- Discord: [Rust Aix-Marseille](https://discord.gg/sXr9ZqBJ)
- Email: contact.whispem@gmail.com


## 🗺️ Background

**Education:**  
Italian Studies, Aix-Marseille University

**Transition:**  
Literature & linguistics → Programming (Swift) → Storage engines & distributed systems (Rust)


## ⭐ Support

If you find anything useful:
- ⭐ Star a repo
- 🐛 Open issues
- 🤝 Contribute (PRs welcome!)
- 📢 Share with Rust learners


*"Structure determines outcome. Precision isn't optional. You learn by building."*
