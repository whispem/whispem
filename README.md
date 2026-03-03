# Hi there 👋🏼

**I'm Emilie — Rust developer, distributed systems enthusiast, and passionate about language design.**  
*From literature & languages to building storage systems in Rust: curiosity drives innovation.*

[![GitHub](https://img.shields.io/badge/GitHub-whispem-181717?logo=github)](https://github.com/whispem) [![LinkedIn](https://img.shields.io/badge/LinkedIn-emilie--peretti-0A66C2?logo=linkedin)](https://www.linkedin.com/in/emilie-peretti) [![Discord](https://img.shields.io/badge/Discord-RAM-5865F2?logo=discord&logoColor=white)](https://discord.gg/dZUtD9S2rT) [![Email](https://img.shields.io/badge/Email-contact.whispem-EA4335?logo=gmail&logoColor=white)](mailto:contact.whispem@gmail.com)

---

I build systems that are meant to be read, understood, and taken apart. I work primarily in Rust, across two domains: **distributed infrastructure** and **programming language design** — both driven by the same conviction: complexity should be earned, never hidden.

Everything I ship is open source, MIT-licensed, and built in public.

---

## whispem-lang

[![Version](https://img.shields.io/badge/version-3.0.0-cyan)](https://github.com/whispem/whispem-lang/releases) [![Tests](https://img.shields.io/badge/tests-125_passing-brightgreen)](https://github.com/whispem/whispem-lang/actions) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/whispem-lang)

**[whispem-lang](https://github.com/whispem/whispem-lang)** is a small, self-hosted programming language. The compiler is written in Whispem, compiles itself, and runs on a standalone C VM — no external dependencies beyond a C compiler. Rust serves as the reference implementation.

> *Whisper your intent. The machine listens.*

#### What makes v3.0.0 special

- **Self-hosted compiler** — `compiler/wsc.wsp`: 1 618 lines of Whispem implementing the full pipeline — lexer, recursive-descent parser, bytecode compiler, binary serialiser. Source goes in, `.whbc` bytecode comes out, byte-for-byte identical to the Rust compiler's output.

- **Verified bootstrap** — The compiler compiles itself. The result compiles itself again. Both outputs share the same SHA-1 — a stable fixed point. The same hash holds on both the C VM and the Rust VM.

- **Standalone C VM** — `vm/wvm.c`: a single-file runtime (~2 000 lines) with 34 opcodes, 20 builtins, refcounted copy-on-write arrays and dicts, an interactive REPL, and a `--dump` disassembler.

- **`.whbc` bytecode format** — Binary format with magic header, length-prefixed, line numbers preserved for error reporting. Compile once, run on either runtime.

- **125 tests, zero warnings** — 93 Rust tests (including 13 bytecode round-trip tests) + 32 autonomous C VM tests with bootstrap verification.

#### Architecture

```
source (.wsp)
    ↓  compiler/wsc.wsp (self-hosted)  or  src/compiler.rs (Rust)
bytecode (.whbc)
    ↓  vm/wvm.c (standalone)  or  src/vm.rs (Rust)
output
```

#### The language

```wsp
let name = "Emilie"
print "Hello, " + name

fn factorial(n) {
    if n <= 1 { return 1 }
    return n * factorial(n - 1)
}
print factorial(10)

let fruits = ["apple", "banana", "cherry"]
for fruit in fruits { print fruit }

let config = {"debug": true, "level": 3}
print has_key(config, "debug")
```

Variables, functions, recursion, forward calls, arrays, dicts, index assignment, `for`/`while`/`if`/`else`, short-circuit `and`/`or`, built-in I/O — all in a clean, line-oriented syntax with no semicolons.

#### Quick start

```bash
# Standalone — only needs a C compiler
make
./wvm compiler/wsc.whbc examples/hello.wsp   # compile + run
./wvm examples/hello.whbc                    # run precompiled bytecode
./wvm --dump examples/hello.whbc             # inspect bytecode
./wvm                                        # interactive REPL

# Rust reference implementation
cargo run -- examples/hello.wsp              # run source file
cargo run -- --compile examples/hello.wsp    # compile to .whbc
cargo test                                   # 93 tests
```

**Philosophy:** every feature must justify its existence. The entire language — and its implementation — fits in your head.

---

## minikv

[![Status](https://img.shields.io/badge/status-production_grade-success)](https://github.com/whispem/minikv) [![Rust](https://img.shields.io/badge/rust-1.81+-orange)](https://rustup.rs/) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/minikv)

**[minikv](https://github.com/whispem/minikv)** is a distributed, multi-tenant key-value & object store written in Rust — built as a reference implementation of production-grade distributed systems concepts.

#### Consensus & distribution

Raft consensus with leader election and log replication · two-phase commit (2PC) for multi-key transactions · 256 virtual shards with consistent hashing · automatic rebalancing and failover · cross-datacenter async replication · conflict resolution (LWW, vector clocks)

#### Storage & performance

Pluggable backends (RocksDB, Sled, in-memory) · write-ahead log (WAL) · Bloom filters · LZ4/Zstd compression · data tiering (hot/warm/cold/archive) · **50 000+ writes/sec** single node · **sub-millisecond reads** · tested on 3–5 node clusters

#### APIs

HTTP REST (CRUD, batch, range, prefix) · S3-compatible (buckets, objects, multipart) · gRPC (internal) · WebSocket/SSE (real-time watch/subscribe)

#### Security & multi-tenancy

RBAC · JWT + API key auth (Argon2) · AES-256-GCM encryption at rest · TLS everywhere · per-tenant isolation, quotas, rate limiting · audit logging

#### Observability & operations

Prometheus metrics · OpenTelemetry tracing · admin Web UI · health probes · backup/restore · CDC · plugin system

#### Cloud-native (v0.9.0)

Kubernetes Operator (CRD + autoscaling) · time-series engine (downsampling, aggregations) · geo-partitioning (GDPR compliance) · io_uring zero-copy I/O

#### Architecture

```
        REST · S3 · gRPC · WebSocket
                    │
        ┌───────────▼───────────┐
        │   Raft Coordinators   │  consensus + 2PC
        │     (3–5 nodes)       │
        └───────────┬───────────┘
                    │
        ┌───────────▼───────────┐
        │    Volume Servers     │  256 virtual shards
        │  RocksDB · Sled · Mem │
        └───────────────────────┘
```

**Status:** v0.9.0 — production-grade.

---

## Tech

```
Rust  ████████████████████████████████████████  primary
C     █████████████░░░░░░░░░░░░░░░░░░░░░░░░░░  whispem VM
```

**Core:** Rust · C · Tokio · Axum · Tonic (gRPC) · Protobuf  
**Storage:** RocksDB · Sled  
**Crypto:** AES-256-GCM · Argon2 · BLAKE3 · rustls  
**Ops:** Prometheus · OpenTelemetry · Docker · Kubernetes

---

*"The best way to learn is to build."*

**[GitHub](https://github.com/whispem)** · **[LinkedIn](https://www.linkedin.com/in/emilie-peretti)** · **[Discord](https://discord.gg/dZUtD9S2rT)** · **[contact.whispem@gmail.com](mailto:contact.whispem@gmail.com)**
