<div align="center">

<img src="hi-emilie.svg" alt="Hi! I’m Emilie (Em’) 👋🏼" />

<strong>Founder of <a href="https://whisphub.dev">WhispHub</a>.<br/>
I build programming languages and distributed systems in Rust — mostly to understand how they work.</strong>

<em>A DESU in Data Science freshly in hand (Aix-Marseille School of Economics) — because curiosity refuses to sit still.</em>

</div>

---

> *Around here, everything begins with a whisper.*

I came to code from the other side of language — literature and grammar, the human kind.
Somewhere between conjugation tables and my first compiler error, something clicked: a programming language is just another grammar, one where intent becomes action.
So instead of only learning languages, I started building them.

That curiosity became **whispem-lang**, a small compiler that now compiles itself.
Rust taught me how machines like to be spoken to; distributed systems, what happens when thousands of them talk at once; a data-science degree, how to listen when the data answers back.

The whisper follows me everywhere — **whispem**, **WhispHub**, ***sussurro*** — because it *is* the philosophy: good software doesn't shout.
It stays small, legible, and honest about what it does — complexity earned, never hidden — built to be read, understood, and taken apart.
And whispers carry further than you'd think: *small ideas, big echoes.*

Most of what I ship is open source.
WhispHub is a hosted product I keep private — but everything else lives on GitHub, MIT-licensed, built in public.

---

## Where the whisper began 🫧

### whispem-lang — a language that compiles itself

[![Version](https://img.shields.io/badge/version-6.0.0-cyan)](https://github.com/whispem/whispem-lang/releases) [![Tests](https://img.shields.io/badge/tests-204_passing-brightgreen)](https://github.com/whispem/whispem-lang) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/whispem-lang)

Everything I do carries the *whisper* — and this is where it began.
**[whispem-lang](https://github.com/whispem/whispem-lang)** is a small, self-hosted programming language: the compiler is written in Whispem itself, compiles itself, and produces byte-identical output with the reference Rust implementation. It runs on a standalone C VM with no dependencies beyond a C compiler.

> *Whisper your intent. The machine listens.*

- **Self-hosted compiler** — `compiler/wsc.wsp`: 1724 lines of Whispem for the full pipeline. Source in, `.whbc` bytecode out — identical to the Rust output.
- **Verified bootstrap** — the compiler compiles itself, and both outputs share the same SHA-1: a stable fixed point.
- **Standalone C VM** — `vm/wvm.c`: a single-file runtime (~2000 lines), 34 opcodes, interactive REPL, `--dump` disassembler.
- **204 tests, zero warnings** — 153 Rust tests + 51 autonomous C VM tests with bootstrap verification.

```wsp
fn factorial(n) {
    if n <= 1 { return 1 }
    return n * factorial(n - 1)
}

for n in range(1, 16) {
    if n % 15 == 0 { print "FizzBuzz" }
    else if n % 3 == 0 { print "Fizz" }
    else if n % 5 == 0 { print "Buzz" }
    else { print n }
}
```

```bash
make
./wvm compiler/wsc.whbc examples/hello.wsp   # compile + run
cargo test                                   # 153 Rust tests
```

---

## Selected work

Three projects, three directions — a product, a translator, and a distributed store. All the same conviction: complexity should be earned, never hidden.

### [WhispHub](https://whisphub.dev) — a living page for every project

[![Live](https://img.shields.io/badge/status-live-brightgreen)](https://whisphub.dev) [![Stack](https://img.shields.io/badge/stack-Rust%20%2B%20Astro-cyan)](https://whisphub.dev/about)

A social space for makers, where a project gets a *living page* — not just a code repo. Hearts instead of stars, echoes instead of forks, pulses instead of commits. Zero tracking, zero ads, GDPR by design. Built solo over six months in Rust + Astro; launched April 29, 2026. *Small ideas, big echoes.*

### [sussurro.cpp](https://github.com/whispem/sussurro.cpp) — offline neural translation, from scratch

[![Stack](https://img.shields.io/badge/stack-C%2B%2B%20%2B%20ggml-blue)](https://github.com/whispem/sussurro.cpp) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/sussurro.cpp/blob/main/LICENSE)

A voice-to-voice interpreter across English, Spanish, French and Italian — Marian / OPUS-MT reimplemented on [ggml](https://github.com/ggml-org/ggml), no server, no network at runtime. Twelve translation directions, speech-to-text via whisper.cpp, text-to-speech via sherpa-onnx, wrapped in a native Tauri app. *Sussurro* is Italian for whisper.

### [minikv](https://github.com/whispem/minikv) — a distributed store, built in public

[![Stack](https://img.shields.io/badge/stack-Rust-orange)](https://github.com/whispem/minikv) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/minikv)

A distributed key-value and object store in Rust: Raft consensus for the cluster, 2PC for distributed writes, a Write-Ahead Log for durability, virtual sharding for elasticity, and an S3-compatible API. Built entirely in the open — mono-node first, then a full distributed rewrite. Understanding the system over raw performance.

---

## Also building 🫧

- **[learn-assembly-with-em](https://github.com/whispem/learn-assembly-with-em)** — a learning-in-public descent into x86-64 assembly: coreutils, `printf`, `malloc`, a shell, a Forth, a bootloader… no libc, `syscall` or nothing. *Drowning in C? Dive deeper — after assembly, C feels like floating.*
- **[asm.kvstore](https://github.com/whispem/asm.kvstore)** — a single-node TCP key-value store in pure x86-64 assembly. `epoll` event loop, 200+ concurrent clients, a 13 KB static binary. Syscalls only.
- **[dprism](https://github.com/whispem/dprism)** — terminal-native data profiling in Rust. htop meets pandas-profiling: explore multi-GB datasets instantly, without leaving your terminal. Built with Polars and Ratatui.

---

*"The best way to learn is to build."*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/emilie-peretti) [![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/dZUtD9S2rT) [![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:contact.whispem@gmail.com)
