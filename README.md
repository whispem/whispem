# Hi there 👋🏼

I'm Emilie — Rust developer, distributed systems enthusiast, and passionate about language design.  
From literature & languages to building storage systems in Rust: curiosity drives innovation.

---

## 👩🏻‍💻 Projects

### [whispem-lang](https://github.com/whispem/whispem-lang)

whispem-lang is a minimalist open-source programming language written in Rust — designed to be learnable in an afternoon and understandable in its entirety, including its own implementation.

**Core philosophy:**
- Simple to read, easy to reason about
- No hidden behavior; every feature must justify its existence
- The entire language — and its implementation — fits in your head

**Main features:**
- Clear, concise syntax (no semicolons, line-oriented)
- Explicit control flow, data types, arrays, dicts, strings
- Built-in I/O and file operations
- Helpful error messages and comprehensive documentation
- Bytecode VM with a `--dump` flag to inspect compiled bytecode

**Architecture:** whispem-lang v2.0.0 compiles to bytecode and runs on a stack-based VM (31 opcodes). The pipeline — Lexer → Parser → Compiler → VM — is readable in a single sitting.

whispem-lang is not meant to replace Python, JS, or Rust.  
Instead, it is:
- A teaching and exploration tool for language design
- Minimal, explicit, and fully bootstrappable
- Useful for scripting, education, and rapid prototyping

**Philosophy:** Whisper intent, don't shout complexity.  
**Status:** Feature-complete and stable (v2.0.0 — bytecode VM).  
**License:** MIT

> whispem-lang is for anyone who wants to fully understand their programming tools — down to the last opcode.

---

### [minikv](https://github.com/whispem/minikv)

minikv is a distributed, multi-tenant key-value & object store written in Rust — built as a reference implementation of production-grade distributed systems concepts.

**Core features:**
- Strong consistency via Raft consensus and two-phase commit (2PC)
- 256 virtual shards with consistent hashing, automatic rebalancing and failover
- Pluggable storage backends: RocksDB, Sled, in-memory
- Write-ahead log (WAL), LZ4/Zstd compression, Bloom filters
- S3-compatible API, HTTP REST, gRPC, WebSocket/SSE
- Multi-tenancy with RBAC, AES-256-GCM encryption, JWT and API key auth, audit logging
- Prometheus metrics, OpenTelemetry tracing, admin Web UI
- Time-series engine, geo-partitioning, data tiering, Kubernetes Operator (v0.9.0)

**Performance:** 50,000+ writes/sec on a single node (in-memory), sub-millisecond reads, tested on 3–5 node clusters.  
**Status:** v0.9.0 — production-grade.  
**License:** MIT

---

## 🌍 Community & Contact

- [GitHub](https://github.com/whispem)
- [LinkedIn](https://www.linkedin.com/in/emilie-peretti)
- [Discord RAM](https://discord.gg/dZUtD9S2rT)
- contact.whispem@gmail.com

---

*"The best way to learn is to build."*