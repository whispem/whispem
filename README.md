# Hi there 👋🏼

**I'm Emilie — Rust developer, distributed systems enthusiast, and passionate about language design.**  
*From literature & languages to building programming languages in Rust: curiosity drives innovation.*

[![GitHub](https://img.shields.io/badge/GitHub-whispem-181717?logo=github)](https://github.com/whispem) [![LinkedIn](https://img.shields.io/badge/LinkedIn-emilie--peretti-0A66C2?logo=linkedin)](https://www.linkedin.com/in/emilie-peretti) [![Discord](https://img.shields.io/badge/Discord-RAM-5865F2?logo=discord&logoColor=white)](https://discord.gg/dZUtD9S2rT) [![Email](https://img.shields.io/badge/Email-contact.whispem-EA4335?logo=gmail&logoColor=white)](mailto:contact.whispem@gmail.com)

---

I build systems that are meant to be read, understood, and taken apart. I work primarily in Rust, across two domains: **programming language design** and **distributed infrastructure** — both driven by the same conviction: complexity should be earned, never hidden.

Everything I ship is open source, MIT-licensed, and built in public.

---

## Projects 👩🏻‍💻

## whispem-lang

[![Version](https://img.shields.io/badge/version-5.0.0-cyan)](https://github.com/whispem/whispem-lang/releases) [![Tests](https://img.shields.io/badge/tests-167_passing-brightgreen)](https://github.com/whispem/whispem-lang) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/whispem-lang)

**[whispem-lang](https://github.com/whispem/whispem-lang)** is a small, self-hosted programming language. The compiler is written in Whispem itself and compiles itself, producing byte-identical output with the reference Rust implementation. It runs on a standalone C VM with no dependencies beyond a C compiler. Rust remains the reference implementation.

> *Whisper your intent. The machine listens.*

- **Self-hosted compiler** — `compiler/wsc.wsp`: 1724 lines of Whispem for the full pipeline. Source in, `.whbc` bytecode out—identical to Rust output.
- **Verified bootstrap** — The compiler compiles itself. Both outputs share the same SHA-1, ensuring a stable fixed point.
- **Standalone C VM** — `vm/wvm.c`: a single-file runtime (~2000 lines) with 34 opcodes, interactive REPL, and a `--dump` disassembler.
- **167 tests, zero warnings** — 130 Rust tests + 37 autonomous C VM tests with bootstrap verification.

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
cargo test                                   # 130 Rust tests
```

---

## Also

**[dprism](https://github.com/whispem/dprism)** — terminal-native data profiling tool in Rust. htop meets pandas-profiling. Explore multi-GB datasets instantly without leaving your terminal. Built with Polars and Ratatui.

**[minikv](https://github.com/whispem/minikv)** — distributed key-value store in Rust. Raft consensus, 2PC transactions, 256 virtual shards, S3-compatible API, 50 000+ writes/sec.

---

*"The best way to learn is to build."*

**[GitHub](https://github.com/whispem)** · **[LinkedIn](https://www.linkedin.com/in/emilie-peretti)** · **[Discord](https://discord.gg/dZUtD9S2rT)** · **[contact.whispem@gmail.com](mailto:contact.whispem@gmail.com)**
