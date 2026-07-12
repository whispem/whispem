![Hi! I’m Emilie (Em’) 👋🏼](hi-emilie.svg)

**Founder of [WhispHub](https://whisphub.dev). 
I build programming languages and distributed systems in Rust — mostly to understand how they work.**

*A DESU in Data Science freshly in hand (Aix-Marseille School of Economics), and currently learning to swim in the [42](https://42.fr) piscine — curiosity does that to you. 🏊🏼‍♀️*

---

> *Around here, everything begins with a whisper.*

I came to code from the other side of language — literature and grammar, the human kind. 
Somewhere between conjugation tables and my first compiler error, something clicked: a programming language is just another grammar, one where intent becomes action. 
So instead of only learning languages, I started building them.

That curiosity became **whispem-lang**, a small compiler that now compiles itself. 
Rust taught me how machines like to be spoken to; distributed systems, what happens when thousands of them talk at once; a data-science degree, how to listen when the data answers back. 
These days, the 42 piscine is teaching me humility — one segfault at a time.

The whisper follows me everywhere — **whispem**, **WhispHub**, ***sussurro*** — because it *is* the philosophy: good software doesn't shout. 
It stays small, legible, and honest about what it does — complexity earned, never hidden — built to be read, understood, and taken apart. 
And whispers carry further than you'd think: *small ideas, big echoes.*

Most of what I ship is open source. 
WhispHub is a hosted product I keep private — but everything else lives on GitHub, MIT-licensed, built in public.

---

## Projects 👩🏻‍💻

### WhispHub

[![Live](https://img.shields.io/badge/status-live-brightgreen)](https://whisphub.dev) [![Stack](https://img.shields.io/badge/stack-Rust%20%2B%20Astro-cyan)](https://whisphub.dev/about) [![Solo](https://img.shields.io/badge/built-solo-blueviolet)](https://whisphub.dev/about)

**[WhispHub](https://whisphub.dev)** is a social space for makers — a place where a project gets a *living page*, not just a code repo. 
Built solo over six months in Rust + Astro. 
Officially launched April 29, 2026.

> *Small ideas, big echoes.*

- **A full page per project** — share the *why*, not just the code
- **Hearts instead of stars** — relational, not just a counter
- **Echoes instead of forks** — share the meaning, not duplicate the code
- **Pulses instead of commits** — capture the rhythm of your work over time
- **Zero tracking, zero ads, GDPR by design** — quiet by intention

The product is hosted at **[whisphub.dev](https://whisphub.dev)** — free for everyone. Read the full story on the [About page](https://whisphub.dev/about).

---

### whispem-lang

[![Version](https://img.shields.io/badge/version-6.0.0-cyan)](https://github.com/whispem/whispem-lang/releases) [![Tests](https://img.shields.io/badge/tests-204_passing-brightgreen)](https://github.com/whispem/whispem-lang) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/whispem-lang)

**[whispem-lang](https://github.com/whispem/whispem-lang)** is a small, self-hosted programming language. 
The compiler is written in Whispem itself and compiles itself, producing byte-identical output with the reference Rust implementation. 
It runs on a standalone C VM with no dependencies beyond a C compiler. 
Rust remains the reference implementation.

> *Whisper your intent. The machine listens.*

- **Self-hosted compiler** — `compiler/wsc.wsp`: 1724 lines of Whispem for the full pipeline. Source in, `.whbc` bytecode out — identical to Rust output.
- **Verified bootstrap** — The compiler compiles itself. Both outputs share the same SHA-1, ensuring a stable fixed point.
- **Standalone C VM** — `vm/wvm.c`: a single-file runtime (~2000 lines) with 34 opcodes, interactive REPL, and a `--dump` disassembler.
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

### sussurro.cpp

[![Version](https://img.shields.io/badge/version-0.7.0-cyan)](https://github.com/whispem/sussurro.cpp/releases) [![Stack](https://img.shields.io/badge/stack-C%2B%2B%20%2B%20ggml-blue)](https://github.com/whispem/sussurro.cpp) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/sussurro.cpp/blob/main/LICENSE)

**[sussurro.cpp](https://github.com/whispem/sussurro.cpp)** is an offline voice-to-voice interpreter across **English, Spanish, French and Italian** — type or speak in one language, read or hear it in another. 
Neural machine translation built from scratch on [ggml](https://github.com/ggml-org/ggml): no server, no network at runtime. *Sussurro* is Italian for whisper.

> *Whisper in one language. Listen in another.*

- **Marian / OPUS-MT reimplemented on ggml** — encoder–decoder Transformers with greedy & beam-search decoding, an incremental KV cache, and q8_0 / q4_0 / f16 weights.
- **Twelve translation directions, no pivoting** — one multilingual model for Romance ↔ Romance, bilingual models for English ↔ Romance.
- **Voice in, voice out** — speech-to-text via whisper.cpp, text-to-speech via sherpa-onnx with a Piper voice per language.
- **Native desktop app** — a Tauri v2 UI wrapping the whole pipeline; every stage also works from the CLI.

```bash
git clone --recurse-submodules https://github.com/whispem/sussurro.cpp.git
cd sussurro.cpp && cmake -B build && cmake --build build -j
./build/sussurro -m models/tc-en-it.gguf -p "Hello, how are you?"   # → Italian
```

---

### learn-assembly-with-em

[![Arch](https://img.shields.io/badge/x86--64-NASM-orange)](https://github.com/whispem/learn-assembly-with-em) [![libc](https://img.shields.io/badge/libc-none-red)](https://github.com/whispem/learn-assembly-with-em) [![Segfaults](https://img.shields.io/badge/segfaults-character--building-blueviolet)](https://github.com/whispem/learn-assembly-with-em)

**[learn-assembly-with-em](https://github.com/whispem/learn-assembly-with-em)** is my learning-in-public descent into **x86-64 assembly**: rebuilding userland from raw syscalls up. 
Linux, NASM, no libc, no external calls — `syscall` or nothing.

> *Drowning in C? Dive deeper — after assembly, C feels like floating.*

- **Coreutils, by hand** — `cat`, `wc`, `ls` and `grep` in pure assembly (filed under "warm-up")
- **`printf` and `malloc` from scratch** — varargs parsing, `brk`/`mmap`, free lists, alignment
- **A working shell** — `fork`, `execve`, pipes and redirections, all in raw syscalls
- **Boss fights ahead** — a Forth interpreter, a self-hosting assembler, a bootloader… and, eventually, a mini-kernel

The piscine teaches you to swim. This repo is the bottom of the pool.

---

### Also on the shelf

**[dprism](https://github.com/whispem/dprism)** — terminal-native data profiling tool in Rust. htop meets pandas-profiling. Explore multi-GB datasets instantly without leaving your terminal. Built with Polars and Ratatui.

**[minikv](https://github.com/whispem/minikv)** — distributed key-value store in Rust. Raft consensus, 2PC transactions, 256 virtual shards, S3-compatible API, 50 000+ writes/sec.

---

*"The best way to learn is to build."*


[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/emilie-peretti)

[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/dZUtD9S2rT)

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:contact.whispem@gmail.com)
