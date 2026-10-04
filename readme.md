# Awesome Lean Programming [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Dependently typed functional programming language and interactive theorem prover.

[Lean 4](https://lean-lang.org/) is largely written in Lean, it compiles to C, and it can prove things about the programs you write in it. Most existing lists focus on formalized mathematics. This one looks at Lean from a programmer's point of view: libraries, tooling, program verification, interop, and software that people have actually built.

## Contents

- [Official](#official)
- [Learning Resources](#learning-resources)
- [Editors & Environments](#editors--environments)
- [Build, Packaging & CI](#build-packaging--ci)
- [Developer Tools](#developer-tools)
- [Testing](#testing)
- [Libraries](#libraries)
  - [Standard Library Extensions & Data Structures](#standard-library-extensions--data-structures)
  - [Parsing & Text](#parsing--text)
  - [Serialization](#serialization)
  - [Web & Networking](#web--networking)
  - [Databases](#databases)
  - [Cryptography & Compression](#cryptography--compression)
  - [Date & Time](#date--time)
  - [CLI & Terminal](#cli--terminal)
  - [Effects, Concurrency & Streams](#effects-concurrency--streams)
  - [Graphics, GUI & Games](#graphics-gui--games)
  - [Mobile](#mobile)
  - [Scientific Computing & Machine Learning](#scientific-computing--machine-learning)
  - [FFI & Language Interop](#ffi--language-interop)
  - [Hardware & Embedded](#hardware--embedded)
  - [Metaprogramming & DSLs](#metaprogramming--dsls)
- [Automation, Solvers & Tactics](#automation-solvers--tactics)
- [Program Verification](#program-verification)
- [Compilers, Kernels & Language Implementations](#compilers-kernels--language-implementations)
- [AI & Agent Tooling](#ai--agent-tooling)
- [Applications & Showcases](#applications--showcases)
- [Community](#community)

## Official

Core projects maintained by the Lean FRO and the Lean community.

- [Lean 4](https://github.com/leanprover/lean4) - The compiler, language server, the Lake build system, and the standard library (`Std`: async I/O, TCP, HTTP, `Std.Time`, hash maps, iterators, and more).
- [elan](https://github.com/leanprover/elan) - Toolchain manager for Lean, similar to `rustup`.
- [Reservoir](https://reservoir.lean-lang.org/) - Package registry and index for Lean packages.
- [Batteries](https://github.com/leanprover-community/batteries) - "Batteries included" extended library with data structures, utilities and tactics beyond core.
- [Lean 4 Web](https://live.lean-lang.org/) - Online Lean editor running in the browser ([source](https://github.com/leanprover-community/lean4web)).
- [Lean on Compiler Explorer](https://lean.godbolt.org/) - Inspect the IR, C and assembly that Lean generates on godbolt.org.
- [Verso](https://github.com/leanprover/verso) - Documentation authoring tool used for the Lean manual, books and websites, with elaborated and highlighted Lean code ([website](https://verso.lean-lang.org)).
- [doc-gen4](https://github.com/leanprover/doc-gen4) - API documentation generator for Lean 4 packages.
- [CSLib](https://github.com/leanprover/cslib) - The Lean Computer Science Library: algorithms, semantics, automata, and models of computation.

## Learning Resources

**Books & Guides**
- [Functional Programming in Lean](https://lean-lang.org/functional_programming_in_lean/) - The standard introduction to Lean as a programming language.
- [Theorem Proving in Lean 4](https://lean-lang.org/theorem_proving_in_lean4/) - Dependent type theory and proofs in Lean.
- [The Lean Language Reference](https://lean-lang.org/doc/reference/latest/) - The official reference manual.
- [Metaprogramming in Lean 4](https://github.com/leanprover-community/lean4-metaprogramming-book) - Book on macros, elaborators, tactics and the `MetaM` stack.
- [From Zero to QED](https://github.com/sdiehl/zero-to-qed) - Informal introduction to Lean 4 for programmers.
- [Lean by Example](https://github.com/lean-ja/lean-by-example) - Lean and its main libraries explained through code examples (Japanese).
- [Lean (meta-)programming Cookbook](https://leanprover-cookbook.github.io/lean-metaprogramming-recipes/) - Recipes for common programming and metaprogramming tasks.
- [Tactic Programming Guide](https://github.com/mirefek/lean-tactic-programming-guide) - Beginner's guide to writing tactics.
- [Lean Symbol Reference](https://quartztz.github.io/lean-symb) - Searchable list of Unicode symbols and their input abbreviations.
- [Lean Snippets](https://github.com/palladin/lean-snippets) - Functional programming patterns in Lean 4, from lazy evaluation and continuations to category-theory-inspired techniques.

**Programming Languages & Verification**
- [Software Foundations in Lean](https://github.com/plclub/sf-in-lean) - The Software Foundations textbooks, being translated from Rocq to Lean.
- [Programming Language Foundations in Lean](https://github.com/rami3l/PLFaLean) - Learn Lean 4 with PLFA.
- [Essentials of Compilation in Lean](https://github.com/keilambda/eocia-lean) - An incremental compiler following "Essentials of Compilation".
- [CPDT in Lean](https://github.com/hargoniX/cpdt-lean) - Lean implementations of material from "Certified Programming with Dependent Types".
- [Aeneas Tutorial](https://github.com/AeneasVerif/icfp-tutorial) - Verifying Rust programs in Lean with Aeneas (ICFP tutorial).
- [Human-eval-lean](https://github.com/leanprover/human-eval-lean) - Hand-written, verified Lean solutions to the HumanEval benchmark, useful as idiomatic examples.

**Practice**
- [leetproof.org](https://leetproof.org) - Practice platform with Lean challenges and community solutions.

## Editors & Environments

- [vscode-lean4](https://github.com/leanprover/vscode-lean4) - Official VS Code extension with infoview, widgets and Unicode input.
- [lean.nvim](https://github.com/Julian/lean.nvim) - Neovim support for Lean 4, including an infoview.
- [lean.vim](https://github.com/SamuelSchlesinger/lean.vim) - Port of lean.nvim to Vim.
- [lean4-mode](https://github.com/leanprover-community/lean4-mode) - Emacs major mode for Lean 4.
- [lean-ts-mode](https://github.com/lua-vr/lean-ts-mode) - Tree-sitter-based Emacs mode.
- [tree-sitter-lean](https://github.com/Julian/tree-sitter-lean) - Tree-sitter grammar for Lean 4.
- [lean4ij](https://github.com/onriv/lean4ij) - IntelliJ platform plugin for Lean 4.
- [acme-lsp-lean](https://github.com/maksym-radziwill/acme-lsp-lean) - Lean support for the Acme editor.
- [lean-tui](https://codeberg.org/wvhulle/lean-tui) - Terminal infoview built with Ratatui, driven by an LSP proxy.
- [xeus-lean](https://github.com/Verilean/xeus-lean) - Jupyter kernel for Lean 4 built on the xeus protocol.
- [lean4_jupyter](https://github.com/utensil/lean4_jupyter) - Jupyter kernel for Lean 4 using the REPL.
- [ProofWidgets4](https://github.com/leanprover-community/ProofWidgets4) - Build custom interactive UI widgets (React) for the infoview.
- [bubble](https://github.com/kim-em/bubble) - Open Lean projects and PRs in sandboxed VS Code containers so untrusted code can't touch your machine.
- [Paperproof](https://github.com/Paper-Proof/paperproof) - Infoview that shows proofs as pen-and-paper-style trees.
- [bare-devcontainer/templates](https://github.com/bare-devcontainer/templates/tree/main/src/lean) - Security-focused Lean 4 dev container with elan, persisted toolchains and Mathlib cache. The base image is available at [bare-devcontainer/images](https://github.com/bare-devcontainer/images/tree/main/src/lean).

## Build, Packaging & CI

- [lean-action](https://github.com/leanprover/lean-action) - GitHub Action to build, test and lint Lean projects.
- [LeanProject](https://github.com/leanprover-community/LeanProject) - Repository template with CI, docs and blueprint setup.
- [lean-update](https://github.com/leanprover-community/lean-update) - GitHub Action to keep Lean toolchains and dependencies up to date.
- [hopscotch](https://github.com/leanprover-community/hopscotch) - CLI that bisects a dependency version range to find where your project breaks ([action](https://github.com/leanprover-community/hopscotch-action)).
- [lev](https://github.com/Robertboy18/lev) - Package and toolchain manager for switching between Lean projects and versions, inspired by uv.
- [lean4-nix](https://github.com/lenianiva/lean4-nix) - Nix flake for Lean 4 and `lake2nix`.
- [rules_lean](https://github.com/pb64-lean/rules_lean) - Bazel rules for Lean 4 and Lake, focused on cross-language native builds.
- [setuptools-lean](https://github.com/leanprover/setuptools-lean) - Plugin for setuptools that packages Python modules written in Lean.
- [lean-churn-bot](https://github.com/FawadHa1der/lean-churn-bot) - Opens PRs that fix upstream breakage using only compiler suggestions, no LLM.
- [intentions](https://github.com/leanprover-community/intentions) - GitHub Action for claiming issues and reporting who is working on what.
- [lean-optimizations](https://github.com/danromik/lean-optimizations) - Proposed optimizations that speed up builds and interactive use ([paper](https://danromik.com/resources/papers/leanopt.pdf)).

## Developer Tools

**Documentation & Literate Programming**
- [Verso Slides](https://github.com/leanprover/verso-slides) - Verso genre for reveal.js slide decks with checked Lean code.
- [SubVerso](https://github.com/leanprover/subverso) - Extracts highlighted Lean code for use in Verso and other tools.
- [mdgen](https://github.com/Seasawher/mdgen) - Generates Markdown files from Lean sources.
- [LiterateLean](https://github.com/tani/literate-lean) - Files that are valid Markdown and valid Lean at the same time, with no preprocessor.
- [lean-slides](https://github.com/0art0/lean-slides) - Renders reveal.js slides from Markdown comments inside the infoview.
- [LeanTeX](https://github.com/kiranandcode/LeanTeX) - DSL for writing LaTeX Beamer presentations in Lean.
- [versotreedoc](https://github.com/richardlford/versotreedoc) - Generates a Verso document skeleton that mirrors a source tree.
- [doc-verification-bridge](https://github.com/NicolasRouquette/doc-verification-bridge) - Documentation tool that extracts verification relationships from Lean code.
- [lean-i18n](https://github.com/hhu-adam/lean-i18n) - Translate Lean projects with PO files.

**Formatting & Linting**
- [leanfmt](https://github.com/duckki/leanfmt) - Structure-preserving code formatter.
- [lean-fmt](https://github.com/jcreinhold/lean-fmt) - Code formatter and linter with editor and CI integration.
- [leaner](https://github.com/SrGaabriel/leaner) - Linter, formatter and whole-program dead-code eliminator.
- [lint-llm-proofs](https://github.com/jessealama/lint-llm-proofs) - Linters for patterns common in LLM-generated proofs.

**Analysis & Inspection**
- [import-graph](https://github.com/leanprover-community/import-graph) - Analyze and visualize a package's import structure (`lake exe graph`).
- [jixia](https://github.com/frenzymath/jixia) - Static analysis tool that extracts declarations, dependency graphs and tactic states.
- [FlameTC](https://github.com/hargoniX/Flame) - Flame graphs for debugging type class synthesis performance.
- [leaff](https://github.com/alexjbest/leaff) - Diff tool for Lean environments.
- [lean4export](https://github.com/leanprover/lean4export) - Plain-text export of declarations for external checkers and tools.
- [ast_export](https://github.com/digama0/ast_export) - Exports Lean 4 ASTs.
- [lean2sexp](https://github.com/andrejbauer/lean2sexp) - Converts `.olean` files to s-expressions.
- [NodeGraph](https://github.com/adamtopaz/NodeGraph) - Generates dependency graphs between declarations.
- [lean4-dep-audit](https://github.com/levzlotnik/lean4-dep-audit) - Traces a constant's transitive dependencies down to axioms, `extern`s and their C sources.
- [Lean Fuzz](https://github.com/kiranandcode/lean-fuzz) - Grammar-based fuzzing for Lean DSLs, using parser tables extracted from the compiler.

**Kernels & Proof Checking**
- [lean4checker](https://github.com/leanprover/lean4checker) - Replays an environment to check that the kernel accepts every declaration (archived).
- [Comparator](https://github.com/leanprover/comparator) - Checks that a solution proves exactly the stated challenge theorem, using only allowed axioms.
- [Lean Kernel Arena](https://arena.lean-lang.org/) - Test suite and leaderboard for independent Lean kernel implementations ([source](https://github.com/leanprover/lean-kernel-arena)).
- [SafeVerify](https://github.com/GasStationManager/SafeVerify) - Robustly checks submitted proofs and implementations against a reference.
- [axiom-audit](https://github.com/leanprover-community/axiom-audit) - Axiom allowlist check that fails CI on `sorry`, `native_decide` or custom axioms.

## Testing

- [Plausible](https://github.com/leanprover-community/plausible) - Property-based testing and counterexample search.
- [LSpec](https://github.com/argumentcomputer/LSpec) - Specification testing framework.
- [nest](https://github.com/hargoniX/nest-core) - Extensible test framework inspired by Haskell's tasty ([unit tests](https://github.com/hargoniX/nest-unit)).
- [LTest](https://github.com/alexf91/LTest) - Fixture-based test framework in the style of pytest.
- [LeanTest](https://github.com/tim-br/LeanTest) - Unit testing framework with a wide range of assertions.
- [lean4-assert-command](https://github.com/pnwamk/lean4-assert-command) - Simple `#assert` command for inline checks.

## Libraries

### Standard Library Extensions & Data Structures

- [LeanColls](https://github.com/JamesGallicchio/LeanColls) - Collections library with a uniform interface.
- [hashbrown4lean](https://github.com/SchrodingerZhu/hashbrown4lean) - Port of Rust's hashbrown SwissTable hash map.
- [CCtx](https://github.com/pandaman64/CCtx) - First-class constructor contexts for writing tail-recursive builders.
- [itertools](https://github.com/tydeu/lean4-itertools) - Iterator library.
- [ac-library](https://github.com/zer0-star/lean-ac-library) - Port of AtCoder Library for competitive programming.
- [Algorithm](https://github.com/astrainfinita/Algorithm) - Verified efficient algorithms.
- [pod](https://github.com/KislyjKisel/lean-pod) - Low-level utilities: single-precision floats, byte spans, unboxed vectors, finalizers.
- [bitmap](https://github.com/varosi/Bitmap) - Image utilities with verified PNG encoding and decoding.

### Parsing & Text

- [lean4-parser](https://github.com/fgdorais/lean4-parser) - Parser combinator library.
- [Megaparsec.lean](https://github.com/argumentcomputer/Megaparsec.lean) - Port of Haskell's Megaparsec.
- [prim-parser](https://github.com/janmasrovira/prim-parser) - Total parser combinators whose termination is guaranteed by graded monads.
- [leansec](https://github.com/remimimimimi/leansec) - Total parser combinators.
- [Partax](https://github.com/tydeu/lean4-partax) - Compiles Lean syntax and parser definitions into standalone parsers.
- [lean-regex](https://github.com/pandaman64/lean-regex) - Regular expression engine with correctness proofs.
- [Regex](https://github.com/bergmannjg/regex) - PCRE2-compatible regular expression engine.
- [UnicodeBasic](https://github.com/fgdorais/lean4-unicode-basic) - Basic Unicode character properties.
- [lean-markdown](https://github.com/paulbutcher/lean-markdown) - CommonMark and GFM implementation that passes the official test suites and is proved total and HTML-safe.
- [lean4-markdown](https://github.com/predictable-machines/lean4-markdown) - Typed DSL for building and rendering Markdown documents.
- [MD4Lean](https://github.com/acmepjz/md4lean) - Wrapper for the MD4C Markdown parser.
- [L4YAML](https://github.com/nasa-jpl/L4YAML) - YAML 1.2.2 parser and dumper with verified properties.
- [lean-url](https://github.com/ammkrn/lean-url) - URL parsing based on the WHATWG standard.
- [lean-semver](https://github.com/runbikeswim/lean-semver) - Semantic versioning.
- [printiest](https://github.com/ammkrn/printiest) - Pretty printer library.
- [BibtexQuery](https://github.com/dupuisf/BibtexQuery) - Command-line BibTeX query utility.

### Serialization

- [lean-json](https://github.com/paulbutcher/lean-json) - JSON library with no `partial` functions or panics, proved against the RFC 8259 grammar, with small binaries.
- [lean4-json-schema](https://github.com/predictable-machines/lean4-json-schema) - Derives JSON Schema from types, with kernel-checked proofs that serialization validates.
- [protobuf](https://github.com/Lean-zh/protobuf) - Protocol Buffers implementation.
- [binary](https://github.com/Lean-zh/binary) - Serialization and deserialization of binary data, inspired by Haskell's `binary`.
- [LeanSerde](https://github.com/oOo0oOo/LeanSerde) - Serialization framework with deriving handlers.
- [ln-messagepack](https://github.com/ItsMeForLua/ln_messagepack) - MessagePack serialization in pure Lean.
- [lean4-base64](https://github.com/predictable-machines/lean4-base64) - RFC 4648 Base64 encoding and decoding.
- [protovalidate-lean](https://github.com/pb64-lean/protovalidate-lean) - Turns CEL constraints on protobuf fields into refinement types.
- [leanxml2](https://github.com/paulbutcher/leanxml2) - libxml2 bindings: DOM parsing, namespaces, serialization and XPath.

### Web & Networking

**Servers & Frameworks**
- [LeanIO](https://github.com/ecyrbe/leanio) - HTTP router for `Std.Http` with compile-time checked routes, JSON handling and middleware.
- [LeanTEA](https://github.com/Verilean/lean-tea) - Full-stack web and TUI framework based on The Elm Architecture.
- [Qed](https://github.com/JacobAsmuth/qed) - Frontend framework with JSX-style components, typed events and state invariants proved at compile time.
- [lean-html](https://github.com/paulbutcher/lean-html) - Typed HTML5 ([lean-htmx](https://github.com/paulbutcher/lean-htmx) adds typed `hx-*` attributes).
- [lean-routing](https://github.com/paulbutcher/lean-routing) - Typed router and route table.
- [lean-middleware](https://github.com/paulbutcher/lean-middleware) - Sessions, sealed cookie store, anti-forgery, static files and request tracing.
- [lean-forms](https://github.com/paulbutcher/lean-forms) - Web forms library.
- [lean-authentication](https://github.com/paulbutcher/lean-authentication) - Magic-link authentication, sessions and rate limiting.
- [datastar-lean](https://github.com/carlohamalainen/datastar-lean) - Datastar SDK for real-time hypermedia apps over server-sent events, with optional compression.
- [LeanRPC](https://github.com/oOo0oOo/LeanRPC) - Expose Lean functions as JSON-RPC endpoints over HTTP with `@[rpc]`.
- [lithe](https://github.com/JoshuaPurtell/lithe) - Simple web service framework.
- [LeanAPI](https://github.com/theoriclabs/leanapi) - API server in the style of Express and FastAPI, with typed routing, field-level validation errors, middleware and auth (experimental).

**Protocols & Clients**
- [socket.lean](https://github.com/hargoniX/socket.lean) - BSD socket bindings.
- [http2-lean](https://github.com/pb64-lean/http2-lean) - HTTP/2 protocol foundation and managed transports.
- [ws-lean](https://github.com/pb64-lean/ws-lean) - WebSocket protocol and networking library.
- [LeanWs](https://github.com/theoriclabs/leanws) - WebSocket library (RFC 6455) in pure Lean over `Std.Http.Transport`, with a server and a client.
- [tls13-lean](https://github.com/pb64-lean/tls13-lean) - TLS 1.3 client and server built on HACL* verified crypto primitives.
- [grpc-lean](https://github.com/pb64-lean/grpc-lean) - Protobuf code generation and a gRPC client/server runtime.
- [lean-grpc](https://github.com/RileyBetts/lean-grpc) - Pure Lean gRPC stack (HTTP/2, HPACK, gRPC).
- [leancurl](https://github.com/paulbutcher/leancurl) - libcurl bindings (see also [leanCurl](https://github.com/bergmannjg/leanCurl)).
- [LeanHttp](https://github.com/theoriclabs/leanhttp) - HTTP and WebSocket client in `Std.Http`'s own types, backed by libcurl (TLS, redirects, HTTP/2).
- [lean-llmclient](https://github.com/paulbutcher/lean-llmclient) - Provider-agnostic LLM chat client with tool calling.
- [lean-mcp](https://github.com/paulbutcher/lean-mcp) - Model Context Protocol server library for writing MCP servers in Lean.

**Cloud & Observability**
- [lean-aws](https://github.com/paulbutcher/lean-aws) - AWS SigV4 signing ([lean-aws-lambda](https://github.com/paulbutcher/lean-aws-lambda) implements the Lambda runtime interface).
- [lean-telemetry](https://github.com/paulbutcher/lean-telemetry) - OpenTelemetry traces and logs.
- [otel-lean](https://github.com/pb64-lean/otel-lean) - OpenTelemetry logs API, proved batch SDK and OTLP exporters.
- [infra](https://github.com/typednotes/infra) - Terraform-style infrastructure as code with dependent types.
- [iam-lean](https://github.com/sufield/iam-lean) - Formal models of AWS IAM policies ([catalog](https://www.zerodrift.dev/iam-lean/catalog.html)).

### Databases

- [leansqlite](https://github.com/leanprover/leansqlite) - SQLite bindings from the Lean FRO.
- [leanpostgres](https://github.com/paulbutcher/leanpostgres) - libpq bindings with a connection pool, in the style of leansqlite ([leanmigrate](https://github.com/paulbutcher/leanmigrate) runs plain-SQL migrations).
- [pg-lean](https://github.com/pb64-lean/pg-lean) - PostgreSQL client with a pure Lean wire protocol, SCRAM, TLS, COPY and pipelining.
- [lean-pgx](https://github.com/pb64-lean/lean-pgx) - Checked Lean types and query runners generated from PostgreSQL DDL and SQL.
- [lean-linq](https://github.com/palladin/lean-linq) - Type-safe LINQ-style SQL query DSL that compiles to parameterized SQL.
- [LeanDB](https://github.com/theoriclabs/LeanDB) - Strongly typed SQL over SQLite: the compiler checks query inputs and result types, and schema changes produce migration plans.
- [LeanMySQL](https://github.com/arthurpaulino/LeanMySQL) - MySQL API.
- [lean-redis](https://github.com/ecyrbe/lean-redis) - Async Redis client written in pure Lean on the `Std` TCP stack.
- [redisLean](https://github.com/marcellop71/redis-lean) - Bindings to the hiredis Redis client.
- [mini-redis](https://github.com/hargoniX/mini-redis) - Implementation of the mini-redis server.

### Cryptography & Compression

- [leancrypto](https://github.com/paulbutcher/leancrypto) - Pure-Lean SHA-2, HMAC, RSA signature verification, DER and encodings, with proofs that the encodings round-trip.
- [leancrypto (Theoric)](https://github.com/theoriclabs/leancrypto) - OpenSSL-backed SHA-256, HMAC, secure random bytes and scrypt password hashing with a ready hash/verify API.
- [lean-crypto](https://github.com/joehendrix/lean-crypto) - Cryptographic routines.
- [lean-jose](https://github.com/paulbutcher/lean-jose) - JSON Web Signature, JSON Web Key and JSON Web Token in pure Lean.
- [jose-libcrypto](https://github.com/paulbutcher/jose-libcrypto) - OpenSSL backend for lean-jose that adds ECDSA, EdDSA and asymmetric signing.
- [lean-libcrypto](https://github.com/paulbutcher/lean-libcrypto) - Bindings to OpenSSL 3's libcrypto through its generic EVP interfaces.
- [Blake3](https://github.com/argumentcomputer/BLAKE3) - Bindings to the BLAKE3 hash function (see also [Blake3Lean4](https://github.com/BuildCoherence/Blake3Lean4), a pure Lean implementation).
- [OpenSSL.lean](https://github.com/argumentcomputer/OpenSSL.lean) - OpenSSL bindings.
- [lean-cryptolib](https://github.com/atrieu/lean-cryptolib) - Verified Montgomery and Barrett modular reduction.
- [lean-zip](https://github.com/kim-em/lean-zip) - Pure-Lean DEFLATE and zlib with a kernel-checked proof that decompression inverts compression ([blog post: "Why Lean is faster than Rust"](https://kim-em.github.io/blog/2026-7-24-why-lean-is-faster-than-rust/)).
- [lean-zlib](https://github.com/kim-em/lean-zlib) - Bindings to system zlib for zlib, gzip and raw DEFLATE streams, plus CRC-32 and Adler-32.
- [lean-zstd](https://github.com/kim-em/lean-zstd) - Zstandard decompression, via C bindings or a pure-Lean implementation with proofs.
- [lean-archive](https://github.com/kim-em/lean-archive) - Tar and ZIP archives, hardened against hostile input.
- [lean-brotli](https://github.com/JGalego/lean-brotli) - Brotli bindings with whole-buffer and streaming APIs.
- [LeanHuffmanCoding](https://github.com/AnirudhG07/LeanHuffmanCoding) - Huffman coding with correctness proofs.
- [LeanBWT-Bzip2](https://github.com/AnirudhG07/LeanBWT-Bzip2) - bzip2 via the Burrows-Wheeler transform, in pure Lean with proofs.

### Date & Time

- [Std.Time](https://lean-lang.org/doc/api/Std/Time.html) - Dates, times, time zones and formatting in the core standard library.
- [DateTime](https://github.com/T-Brick/DateTime) - ISO 8601 date and time utilities.
- [timelib](https://github.com/ammkrn/timelib) - Date and time library.
- [time](https://github.com/bergmannjg/time) - Port of Haskell's `time` library, with verified date calculations.

### CLI & Terminal

- [lean4-cli](https://github.com/leanprover/lean4-cli) - Configure command-line interfaces and parse arguments (used by Lake).
- [Leansi](https://github.com/schergen-org/Leansi) - Terminal formatting.
- [Pigment](https://github.com/RSoulatIOHK/Pigment) - Terminal colors and styling.
- [asciiplot](https://github.com/alok/AsciiPlot) - Plot functions as ASCII art in the infoview.

### Effects, Concurrency & Streams

- [flow](https://github.com/predictable-machines/lean4-flow) - Reactive streams (Flow, SharedFlow, StateFlow).
- [Straume](https://github.com/argumentcomputer/straume) - Streams library.
- [lean-eff](https://github.com/palladin/lean-eff) - Small extensible-effects library.
- [lean-effects](https://github.com/paulcadman/lean-effects) - Algebraic effects.
- [lean-reducers](https://github.com/palladin/lean-reducers) - Parallel, fused reducers.
- [EffSpec](https://github.com/Izzimach/EffSpec-lean) - Effect monads with specifications (Dijkstra monads).
- [lentil](https://github.com/pb64-lean/lentil) - Compile-time dependency injection.
- [lean-cloud](https://github.com/palladin/lean-cloud) - Parallel and distributed programming with monadic workflows over shared blob storage.

### Graphics, GUI & Games

- [lean-sdl3](https://github.com/ValorZard/lean-sdl3) - SDL3 bindings.
- [lean-sdl3 (philnguyen)](https://github.com/philnguyen/lean-sdl3) - Comprehensive SDL3 bindings ([lean-compose-ui](https://github.com/philnguyen/lean-compose-ui) is a cross-platform UI library built on them).
- [SDL.lean](https://github.com/Anderssorby/SDL.lean) - SDL2 bindings.
- [Raylib.lean](https://github.com/KislyjKisel/Raylib.lean) - Bindings to the raylib game library.
- [raylean](https://github.com/funexists/raylean) - Bindings to the raylib game library.
- [lean-vulkan](https://github.com/kuruczgy/lean-vulkan) - Proof-of-concept Vulkan bindings.
- [lean-wgpu](https://github.com/Kiiyya/lean-wgpu) - WebGPU bindings via wgpu-native.
- [Hesper](https://github.com/Verilean/hesper) - Verified GPU programming with type-safe WebGPU shaders.
- [LeanPlot](https://github.com/alok/LeanPlot) - Plotting with deterministic SVG and PNG backends.
- [Illuminate](https://github.com/leanprover/illuminate) - Compositional 2D diagrams rendered to SVG, with previews in the infoview (experimental).
- [vizagrams](https://github.com/arademaker/vizagrams) - Visualization library.
- [LeanReact](https://github.com/theoriclabs/lean-react) - Write React components in Lean that compile to JavaScript (experimental).
- [lean4-godot](https://github.com/kiranandcode/lean4-godot) - Experimental bindings to the Godot 4 game engine.

### Mobile

- [lean-ios](https://github.com/paulcadman/lean-ios) - Build iOS apps with Lean: patched runtime, SDL3 bindings and build scaffolding.
- [lean4-android](https://github.com/saviorand/lean4-android) - Cross-compiles the Lean runtime for Android (aarch64) with the NDK.
- [lean-compose](https://github.com/saviorand/lean-compose) - Typed DSL for authoring Jetpack Compose UI in Lean ([example app](https://github.com/saviorand/lean-android-compose) calling Lean over JNI).

### Scientific Computing & Machine Learning

- [SciLean](https://github.com/lecopivo/SciLean) - Scientific computing: arrays, automatic differentiation and numerical methods.
- [TorchLean](https://github.com/lean-dojo/TorchLean) - Neural networks with typed tensors, autograd, CUDA support and verification.
- [TensorLib](https://github.com/leanprover/TensorLib) - Verified tensor library.
- [Tables](https://github.com/pandaman64/Tables) - Dataframe library compatible with the B2T2 benchmark, with provable invariants.
- [Hex](https://github.com/leanprover/hex) - Verified computational algebra: matrices, row reduction, polynomial factoring, LLL, graph isomorphism.
- [lp](https://github.com/leanprover/lp) - Verified linear programming solver that returns proof-carrying results, plus an `lp` tactic.
- [LeanBLAS](https://github.com/lecopivo/LeanBLAS) - BLAS bindings with specifications.
- [EigenLean](https://github.com/lecopivo/EigenLean) - Eigen linear algebra bindings.
- [NumLean](https://github.com/arthurpaulino/NumLean) - Numerical matrix computations.
- [FloatLib](https://leandojo.org/floatlib.html) - Verified floating-point arithmetic across formats.
- [FloatSpec](https://github.com/Beneficial-AI-Foundation/FloatSpec) - Formally verified float implementation.
- [fp-lean](https://github.com/opencompl/fp-lean) - Floating-point semantics mechanization.
- [LeanCert](https://github.com/alerad/leancert) - Verified interval arithmetic: bounds, root finding and optimization.
- [interval](https://github.com/girving/interval) - Conservative floating-point interval arithmetic.
- [lean-units](https://github.com/ecyrbe/lean-units) - SI physical unit system.
- [lean-autograd](https://github.com/alok/lean-autograd) - Automatic differentiation following JAX's autodidax.
- [lean4-mlir](https://github.com/brettkoonce/lean4-mlir) - Neural architectures specified in Lean, with verified GPU codegen.
- [ginac-lean](https://github.com/utensil/ginac-lean) - GiNaC computer algebra bindings.
- [LeanSage](https://github.com/oOo0oOo/LeanSage) - Call SageMath from Lean.
- [Tgrad](https://github.com/theoriclabs/t-grad) - Demo bf16 matrix-multiply runtime on Apple Silicon Metal, owned by Lean and driven from Python.

### FFI & Language Interop

- [Alloy](https://github.com/tydeu/lean4-alloy) - Write C shims inline in Lean code.
- [lean-sys](https://github.com/digama0/lean-sys) - Rust bindings to the Lean runtime ([lean-rs](https://github.com/digama0/lean-rs) is a safe wrapper).
- [RustFFI.lean](https://github.com/argumentcomputer/RustFFI.lean) - Template for Lean-Rust FFI.
- [Nerodia](https://github.com/leanprover/nerodia) - Write Python modules in pure Lean, inspired by PyO3 (preview, Lean FRO).
- [lean.py](https://github.com/BasisResearch/lean.py) - Two-way Lean/Python interop with automatic marshalling.
- [Extism Lean SDK](https://github.com/extism/lean4-sdk) - Call WebAssembly plugins from Lean.
- [lean-bindgen](https://github.com/kiranandcode/lean-bindgen) - Generates `@[extern]` declarations and C shims from a concise spec of a C header.

### Hardware & Embedded

- [Sparkle](https://github.com/Verilean/sparkle) - Type-safe, verifiable HDL compiler inspired by Clash.
- [Circuitlib](https://github.com/matthunz/circuitlib) - Digital circuit verification using categorical semantics.
- [LNSym](https://github.com/leanprover/LNSym) - Armv8 native-code symbolic simulator.
- [MRiscX](https://github.com/JulsDE/MRiscX) - Certified RISC-V interpreter with Hoare logic.

### Metaprogramming & DSLs

- [Qq](https://github.com/leanprover-community/quote4) - Intuitive, type-safe expression quotations.
- [Thyme](https://github.com/frangio/thyme) - Typed, staged metaprogramming with dependent types and reasoning about metaprograms.
- [Leanduction](https://github.com/arthur-adjedj/Leanduction) - Generates usable induction principles for nested inductive types.
- [MutualInduction](https://github.com/ionathanch/MutualInduction) - Mutual induction tactic.
- [QPF](https://github.com/alexkeizer/QPFTypes) - (Co)datatype package built on quotients of polynomial functors.
- [Coinductive](https://github.com/ISTA-PLV/coinductive) - Library for coinductive types built on polynomial functors, used to define interaction trees.
- [leanses](https://github.com/VCA-EPFL/leanses) - Lenses with custom notation.
- [lean-subst](https://github.com/amarmaduke/lean-subst) - Substitution library inspired by Autosubst.
- [HexLuthor](https://github.com/alok/HexLuthor) - Hex color literal syntax with inline VS Code preview.
- [Imperia](https://github.com/tydeu/imperia) - Alternative `do` notation for imperative code over non-monadic types (experimental).
- [LeanBitsyntax](https://github.com/palladin/lean-bitsyntax) - Erlang-style `<<...>>` bit syntax for building and matching `BitVec` values (experimental).

## Automation, Solvers & Tactics

Tactics and solver integrations that are useful when proving properties of programs.

- [grind](https://lean-lang.org/doc/reference/latest/The--grind--tactic/) - Built-in SMT-style tactic combining congruence closure, E-matching and arithmetic.
- [bv_decide](https://github.com/leanprover/lean4/tree/master/src/Std/Tactic/BVDecide) - Built-in bit-blasting decision procedure for `BitVec` goals, backed by a verified SAT proof checker (LeanSAT).
- [Aesop](https://github.com/leanprover-community/aesop) - White-box, rule-based proof search.
- [lean-smt](https://github.com/ufmg-smite/lean-smt) - Discharge goals to SMT solvers with proof reconstruction.
- [lean-cvc5](https://github.com/abdoo8080/lean-cvc5) - FFI bindings to the cvc5 SMT solver.
- [lean-auto](https://github.com/leanprover-community/lean-auto) - Interface between Lean and automated theorem provers.
- [Duper](https://github.com/leanprover-community/duper) - Superposition-based automatic prover.
- [LeanHammer](https://github.com/JOSHCLUNE/LeanHammer) - Hammer combining premise selection, ATPs and proof reconstruction.
- [Canonical](https://github.com/chasenorman/CanonicalLean) - Exhaustive term search in dependent type theory.
- [Leanwuzla](https://github.com/hargoniX/Leanwuzla) - Connects `bv_decide` to SMT-LIB.
- [Blaster](https://github.com/input-output-hk/Lean-blaster) - SMT-based reasoning core.
- [egg](https://github.com/marcusrossel/lean-egg) - Equality saturation tactic based on egg (deprecated).
- [OptiSat](https://github.com/lambdaclass/truth_research) - Verified equality saturation engine.
- [Saturn](https://github.com/siddhartha-gadgil/Saturn) - SAT solvers with proofs.
- [trestle](https://github.com/FormalSAT/trestle) - SAT utilities: encodings, solver APIs, and file format parsers and printers.
- [CLeanGo](https://github.com/kiranandcode/cleango) - Bindings and DSL for the Clingo answer set programming solver.
- [waterfall](https://github.com/samth/waterfall) - ACL2-style proof search for inductive goals.
- [sos](https://github.com/leanprover/sos) - Sum-of-squares tactic for nonlinear real arithmetic.
- [SmtLibDsl](https://github.com/palladin/SmtLibDsl) - Typed SMT-LIB DSL with backends for Z3, cvc5, Kissat and CaDiCaL.
- [cpsat](https://github.com/paulbutcher/leancpsat) - Bindings to the OR-Tools CP-SAT constraint solver.
- [deriving such that](https://github.com/kiranandcode/deriving-such-that) - Port of Rocq's program derivation tactic.
- [BetterFind](https://github.com/kiranandcode/BetterFind.lean) - Extended `#find` for searching declarations by pattern, closer to Rocq's `Search`.

## Program Verification

**Frameworks**
- [Std.Do / mvcgen](https://lean-lang.org/doc/reference/latest/The--mvcgen--tactic/) - Built-in monadic program logic and verification condition generator for `do` code.
- [Loom](https://github.com/verse-lab/loom) - Framework for building multi-modal verifiers of effectful programs.
- [Velvet](https://github.com/verse-lab/velvet) - Auto-active program verifier.
- [Veil](https://github.com/verse-lab/veil) - Automated and interactive verification of distributed protocols and transition systems.
- [Iris-Lean](https://github.com/leanprover-community/iris-lean) - Port of the Iris higher-order concurrent separation logic framework.
- [Lentil](https://github.com/verse-lab/Lentil) - LTL reasoning infrastructure.
- [LeanSSR](https://github.com/verse-lab/lean-ssr) - SSReflect-style tactic language.
- [lean-machines](https://github.com/lean-machines-central/lean-machines) - Modelling and refinement of stateful systems.
- [leanSpec](https://github.com/paulch42/lean-spec) - Program specification in Lean 4.
- [WybeCoder](https://github.com/facebookresearch/wybecoder) - Agentic verified imperative code generation on Loom/Velvet.

**Verifying Other Languages**
- [Aeneas](https://github.com/AeneasVerif/aeneas) - Translates safe Rust to Lean for verification.
- [hax](https://github.com/cryspen/hax) - Extracts Rust code to Lean (and other backends).
- [Strata](https://github.com/strata-org/Strata) - Platform for formalizing language syntax and semantics through extensible dialects and building automated reasoning tools on them.
- [LemmaScript](https://github.com/midspiral/LemmaScript) - Verification toolchain for TypeScript (tech preview).
- [rust-lean-models](https://github.com/model-checking/rust-lean-models) - Lean models of Rust standard library functions.
- [ACL2Lean](https://github.com/OathTech/ACL2Lean) - Replay ACL2 proofs as kernel-checked Lean theorems.
- [Talos](https://github.com/cajal-technologies/talos) - WebAssembly interpreter and weakest-precondition calculus for verifying WebAssembly modules.
- [lean-mlir](https://github.com/opencompl/lean-mlir) - MLIR semantics and verified peephole rewrites.

**Semantics & Specifications**
- [Wasm.lean](https://github.com/argumentcomputer/Wasm.lean) - WebAssembly implementation.
- [lean-wasm](https://github.com/T-Brick/lean-wasm) - Formalization of the WebAssembly spec.
- [haskell-spec](https://github.com/haskell-spec/haskell-spec) - Formal specification of the Haskell Language Report.
- [graphql-lean](https://github.com/duckki/graphql-lean) - Formalization of the GraphQL specification.
- [ELFSage](https://github.com/draperlaboratory/ELFSage) - ELF parser and validator.
- [SHerLOC](https://github.com/leanprover/SHerLOC) - StableHLO analyzer.
- [TenCert](https://github.com/leanprover/TenCert) - Verified tensor compilation.
- [graphiti](https://github.com/VCA-EPFL/graphiti) - Verified graph rewriting for dataflow circuits.
- [lean-yjs](https://github.com/iasakura/lean-yjs) - Verification of the Yjs CRDT integration algorithm.
- [langlib](https://github.com/ilyasergey/langlib) - Esoteric programming languages, formally.

**Industrial & Security**
- [cedar-spec](https://github.com/cedar-policy/cedar-spec) - Lean specification and verification of AWS's Cedar authorization language, used for differential testing of the production implementation.
- [SampCert](https://github.com/leanprover/SampCert) - Verified differential privacy, used in production by AWS Clean Rooms.
- [VCVio](https://github.com/Verified-zkEVM/VCVio) - Machine-checked cryptographic proofs with oracle computations.
- [DyLean](https://github.com/BobDyLean/dylean) - Symbolic analysis of cryptographic protocols.
- [verified-3d-mesh-intersection](https://github.com/schildep/verified-3d-mesh-intersection) - Verified 3D constructive solid geometry.
- [bitrep](https://github.com/KyleClouthier/bitrep) - Rust crate for bit-identical float reductions, with the merge algebra proved in Lean.

**Blockchain & Zero Knowledge**
- [EVMYulLean](https://github.com/NethermindEth/EVMYulLean) - Executable formal model of the EVM and Yul.
- [evm-smith](https://github.com/leonardoalt/evm-smith) - Framework for AI systems to write EVM bytecode and prove it safe.
- [Blanc](https://github.com/skbaek/blanc) - Minimal EVM contract language, with proofs about the deployed bytecode.
- [Clean](https://github.com/Verified-zkEVM/clean) - DSL for ZK circuits with soundness and completeness proofs ([zk.golf](https://zk.golf)).
- [ArkLib](https://github.com/Verified-zkEVM/ArkLib) - Formally verified arguments of knowledge.
- [zkLean](https://github.com/GaloisInc/zkLean) - DSL for specifying zero-knowledge statements.
- [risc0-lean4](https://github.com/risc0/risc0-lean4) - Model of the RISC Zero zkVM.
- [aegis](https://github.com/lindy-labs/aegis) - Verify Cairo contracts.
- [btc-verified](https://github.com/ProofOfKeags/btc-verified) - Verified Bitcoin serialization, txids and Merkle commitments.

## Compilers, Kernels & Language Implementations

- [lean4lean](https://github.com/digama0/lean4lean) - Lean 4 kernel written in Lean 4.
- [nanoda](https://github.com/ammkrn/nanoda_lib) - Independent Lean 4 type checker written in Rust.
- [con-leche](https://github.com/leanprover/con-leche) - External Lean checker with a consistency proof ([con-ron](https://github.com/leanprover/con-ron) is a Rust port proved with Aeneas).
- [Metalean](https://github.com/intgrah/metalean) - Verified type checker for an idealized Lean type theory.
- [Lean4Less](https://github.com/Deducteam/Lean4Less) - Translates Lean into smaller theories by eliminating definitional equalities.
- [lean2agda](https://github.com/lyphyser/lean2agda) - Exports elaborated Lean code to Agda.
- [thales](https://github.com/jessealama/thales) - TypeScript compiler and JavaScript engine in Lean.
- [leanexe](https://github.com/jsmorph/leanexe) - Compiler for a Lean dialect that targets verified WebAssembly.
- [lean2wasm](https://github.com/T-Brick/lean2wasm) - Compile Lean to WebAssembly.
- [lean-vir](https://github.com/ejgallego/lean-vir) - Runs Lean in the browser via Lean's IR interpreter compiled to WebAssembly, with a runtime under 200 KiB (early, Lean FRO).
- [lean-gccjit](https://github.com/SchrodingerZhu/lean-gccjit) - Bindings to libgccjit, a basis for alternative backends.
- [QED64](https://github.com/FawadHa1der/QED64) - Lean and Mathlib running in the browser via wasm64.
- [yatima](https://github.com/argumentcomputer/yatima) - Zero-knowledge Lean 4 compiler and kernel.
- [ix](https://github.com/argumentcomputer/ix) - Zero-knowledge proof-carrying code for Lean 4.
- [mm-lean4](https://github.com/digama0/mm-lean4) - High-performance Metamath verifier.
- [Soma](https://github.com/SrGaabriel/soma) - Dependently typed language powered by interaction nets.
- [lapis](https://github.com/SrGaabriel/lapis) - Concurrent Language Server Protocol framework.
- [qdt](https://github.com/intgrah/qdt) - Query-based dependent type elaborator.
- [DeBruijnSSA](https://github.com/imbrem/debruijn-ssa) - Formalization of SSA.
- [verified-compiler](https://github.com/marcusrossel/verified-compiler) - Toy verified compiler.
- [Lyre](https://github.com/tydeu/lyre) - Write Lean IR as Lean syntax.
- [LRT](https://github.com/tydeu/lrt) - Model of Lean's runtime primitives in Lean, partly porting the C runtime (work in progress).
- [LeanPy](https://github.com/tydeu/leanpy) - Experimental implementation of Python in Lean.

## AI & Agent Tooling

**Agents & MCP**
- [lean-lsp-mcp](https://github.com/oOo0oOo/lean-lsp-mcp) - MCP server that gives agents diagnostics, goals, hovers and search through the Lean LSP.
- [lean4-skills](https://github.com/cameronfreer/lean4-skills) - Claude Code skills and plugins for Lean work.
- [Lean Beam](https://github.com/leanprover/lean-beam) - Extends the Lean LSP server for agent- and tool-driven workflows.
- [LeanTool](https://github.com/GasStationManager/LeanTool) - "Code interpreter" for Lean that LLMs can call.
- [AXLE](https://axle.axiommath.ai) - Axiom's Lean engine for proof verification, manipulation and runtime tasks ([MCP](https://github.com/Vilin97/axle-mcp)).
- [Archon Horizon](https://github.com/frenzymath/Archon-Horizon) - Workspace-first orchestration for long-running Codex or Claude Code sessions on Lean.
- [Archon](https://github.com/frenzymath/Archon) - Multi-agent coding and proving workflows over a Lean project, driven by blueprint DAGs.
- [Lean skills](https://github.com/leanprover/skills) - Official agent skills for proofs, toolchain setup, bisection and more.
- [LeanSlop](https://github.com/kiranandcode/leanslop) - Call LLMs from inside Lean code as black-box automation.
- [Aristotle](https://aristotle.harmonic.fun/) - Harmonic's formal reasoning agent, available via web, CLI and API.

**Programmatic Access to Lean**
- [REPL](https://github.com/leanprover-community/repl) - JSON REPL that reports errors, sorries and proof states.
- [Pantograph](https://github.com/leanprover/Pantograph) - Machine-to-machine interaction interface for Lean 4.
- [PyPantograph](https://github.com/stanford-centaur/PyPantograph) - Python interface to Pantograph.
- [leanclient](https://github.com/oOo0oOo/leanclient) - Drive Lean from Python via the LSP.
- [Kimina Lean Server](https://github.com/project-numina/kimina-lean-server) - Fast, scalable server for checking Lean code in batches.
- [LeanDojo](https://github.com/lean-dojo/LeanDojo) - Extract data from and interact with Lean repositories programmatically.
- [LeanCopilot](https://github.com/lean-dojo/LeanCopilot) - LLMs as copilots inside Lean.
- [llmlean](https://github.com/cmu-l3/llmlean) - LLM tactic suggestions from local or cloud models.

**Search**
- [Loogle](https://github.com/nomeata/loogle) - Search declarations by name, type pattern or constant ([web](https://loogle.lean-lang.org/)).
- [LeanSearchClient](https://github.com/leanprover-community/LeanSearchClient) - `#search` syntax for LeanSearch, Loogle and LeanStateSearch from the editor.
- [LeanExplore](https://github.com/justincasher/lean-explore) - Semantic search engine with an MCP server.

**Verified Code Generation Benchmarks**
- [Verina](https://github.com/sunblaze-ucb/verina) - Benchmark for verifiable code generation (code, specs and proofs).
- [CLEVER](https://github.com/trishullab/clever) - Curated Lean benchmark for verified code generation.
- [Vericoding](https://github.com/Beneficial-AI-Foundation/vericoding) - Tools and benchmarks for verified coding.
- [SorryDB](https://github.com/SorryDB/SorryDB) - Continuously updated benchmark built from `sorry`s in real projects.

## Applications & Showcases

**Apps & Services**
- [lean-todomvc-max](https://github.com/paulbutcher/lean-todomvc-max) - Production-style TodoMVC with passwordless sign-in, migrations, telemetry, an LLM panel and AWS Lambda deployment.
- [LeanToDo](https://github.com/pandaman64/LeanToDo) - Web app built with leansqlite, Verso and htmx.
- [lean-acme-widgets](https://github.com/pb64-lean/lean-acme-widgets) - CRUD service combining gRPC, refinement-typed protobuf validation, PostgreSQL and TLS.
- [viper](https://github.com/arthurpaulino/viper) - Python environment manager written in Lean.
- [lean4-raytracer](https://github.com/kmill/lean4-raytracer) - Simple raytracer.
- [Shirika-RPC](https://github.com/eluvane/Shirika-RPC) - TypeScript worker RPC library whose protocol layer is checked in Lean.

**Games**
- [flappy](https://github.com/paulcadman/flappy) - Clone of Flappy Bird built with raylean.
- [LeanDoomed](https://github.com/oOo0oOo/LeanDoomed) - Raycasting demo using SDL3.
- [lean4-maze](https://github.com/dwrensha/lean4-maze) - Maze game encoded in Lean syntax.
- [Chess.lean](https://github.com/dwrensha/Chess.lean) - Chess in Lean 4.
- [ChessProver](https://github.com/parabamoghv/ChessProver) - Chess engine with a theory for proving endgame statements.
- [PuzzleLean](https://git.olsak.net/mirek/PuzzleLean) - PuzzleScript engine: play grid puzzles in the infoview and prove them solvable.
- [EleanvatorSaga](https://github.com/Julian/EleanvatorSaga) - Elevator Saga played in the infoview.
- [lean-snakebird](https://github.com/marcusrossel/lean-snakebird) - Snakebird implementation.
- [Functorio](https://github.com/konne88/functorio) - Build Factorio factories in Lean with types, functions and recursion.
- [lean4game](https://github.com/leanprover-community/lean4game) - Engine and server for interactive Lean games ([live](https://adam.math.hhu.de)).
- [LeanChess](https://github.com/theoriclabs/leanchess) - Chess server where the rules are a Lean program and each game is a fold over its move log ([live](https://leanchess.org)).

## Community

- [Lean Zulip](https://leanprover.zulipchat.com/) - Main community chat; see the `#Project announcements`, `#Program verification` and `#lean4` channels.
- [Lean Community website](https://leanprover-community.github.io/) - Community resources, installation guides and documentation overview.
- [Leangineer Discord](https://discord.gg/ACKNs7ZJPj) - Chat for software engineers building with Lean, alongside [leangineer.com](https://leangineer.com).
- [Lean FRO](https://lean-lang.org/fro/) - The Focused Research Organization developing Lean, including [roadmaps](https://lean-lang.org/fro/roadmap/).
- [Awesome Logic Formalization](https://github.com/FormalizedFormalLogic/awesome-logic-formalization) - Related list about formalized logic.

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first.

## Footnotes

Most entries were collected from project announcements on the Lean Zulip, mainly the `#Project announcements`, `#AI authored projects`, `#Program verification` and `#General announcements` channels. Thanks to everyone who shares their work there. Many others come from the [Reservoir package index](https://github.com/leanprover/reservoir-index).
