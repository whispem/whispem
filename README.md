# Hi there 👋🏼

**I'm Emilie — Founder @ [WhispHub](https://whisphub.dev), Data Science Student @ Aix-Marseille School of Economics (AMSE), Rust developer, distributed systems enthusiast, and passionate about language design.**  
*From literature & languages to building programming languages in Rust: curiosity drives innovation.*

[![GitHub](https://img.shields.io/badge/GitHub-whispem-181717?logo=github)](https://github.com/whispem) [![LinkedIn](https://img.shields.io/badge/LinkedIn-emilie--peretti-0A66C2?logo=linkedin)](https://www.linkedin.com/in/emilie-peretti) [![Discord](https://img.shields.io/badge/Discord-RAM-5865F2?logo=discord&logoColor=white)](https://discord.gg/dZUtD9S2rT) [![Email](https://img.shields.io/badge/Email-contact.whispem-EA4335?logo=gmail&logoColor=white)](mailto:contact.whispem@gmail.com)

---

I build systems that are meant to be read, understood, and taken apart. I work primarily in Rust, across two domains: **programming language design** and **distributed infrastructure** — both driven by the same conviction: complexity should be earned, never hidden.

Most of what I ship is open source. WhispHub, my latest project, is a hosted product I keep private — but everything else lives on GitHub, MIT-licensed, built in public.

---

## Projects 👩🏻‍💻

## WhispHub

[![Live](https://img.shields.io/badge/status-live-brightgreen)](https://whisphub.dev) [![Stack](https://img.shields.io/badge/stack-Rust%20%2B%20Astro-cyan)](https://whisphub.dev/about) [![Solo](https://img.shields.io/badge/built-solo-blueviolet)](https://whisphub.dev/about)

**[WhispHub](https://whisphub.dev)** is a social space for makers — a place where a project gets a *living page*, not just a code repo. Built solo over six months in Rust + Astro. Officially launched April 29, 2026.

> *Small ideas, big echoes.*

- **A full page per project** — share the *why*, not just the code
- **Hearts instead of stars** — relational, not just a counter
- **Echoes instead of forks** — share the meaning, not duplicate the code  
- **Pulses instead of commits** — capture the rhythm of your work over time
- **Zero tracking, zero ads, GDPR by design** — quiet by intention

The product is hosted at **[whisphub.dev](https://whisphub.dev)** — free for everyone. Read the full story on the [About page](https://whisphub.dev/about).

---

## whispem-lang

[![Version](https://img.shields.io/badge/version-6.0.0-cyan)](https://github.com/whispem/whispem-lang/releases) [![Tests](https://img.shields.io/badge/tests-204_passing-brightgreen)](https://github.com/whispem/whispem-lang) [![License: MIT](https://img.shields.io/badge/license-MIT-yellow)](https://github.com/whispem/whispem-lang)

**[whispem-lang](https://github.com/whispem/whispem-lang)** is a small, self-hosted programming language. The compiler is written in Whispem itself and compiles itself, producing byte-identical output with the reference Rust implementation. It runs on a standalone C VM with no dependencies beyond a C compiler. Rust remains the reference implementation.

> *Whisper your intent. The machine listens.*

- **Self-hosted compiler** — `compiler/wsc.wsp`: 1724 lines of Whispem for the full pipeline. Source in, `.whbc` bytecode out—identical to Rust output.
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

## Also

**[dprism](https://github.com/whispem/dprism)** — terminal-native data profiling tool in Rust. htop meets pandas-profiling. Explore multi-GB datasets instantly without leaving your terminal. Built with Polars and Ratatui.

**[minikv](https://github.com/whispem/minikv)** — distributed key-value store in Rust. Raft consensus, 2PC transactions, 256 virtual shards, S3-compatible API, 50 000+ writes/sec.

---

*"The best way to learn is to build."*

**[WhispHub](https://whisphub.dev)** · **[GitHub](https://github.com/whispem)** · **[LinkedIn](https://www.linkedin.com/in/emilie-peretti)** · **[Discord](https://discord.gg/dZUtD9S2rT)** · **[contact.whispem@gmail.com](mailto:contact.whispem@gmail.com)**
