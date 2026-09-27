# Rust Roadmap (systems language track)

**Track:** G
**Role:** real engineering language — **NOT** the CP contest language (see `dsa-cp-roadmap.md`)
**When to run it:** low-intensity in parallel, or after you stabilise around 1400–1600 CF.
Best folded into your existing **Track C (low-level)** — Rust is a better "systems
thinking" vehicle than a taste of C once you know memory/stack/heap.
**Budget:** ~3–5 hrs/week (it is a volume-heavy language; don't sprint it)

---

## Why learn Rust

- Forces correctness: ownership/borrowing kills whole classes of memory and
  concurrency bugs at compile time.
- Excellent tooling: `cargo`, `clippy`, `rustfmt`, built-in tests, docs.
- Growing use in infra/systems (and a strong contrast to Go for your work stack).
- After Rust, C/C++ and Go both look clearer.

**Trade-off to accept:** steep early friction (borrow checker). The first 3–4 weeks
feel slower than Go. Push through; it clicks.

---

## Phases

### Phase 0 — Toolchain & basics
- [ ] Install `rustup`; `cargo new/run/build/test`; `cargo add`
- [ ] Variables, mutability, shadowing, types, `const` vs `let`
- [ ] Functions, control flow, `match`, `if let`
- [ ] Compound types: tuples, arrays, slices, `String` vs `&str`
- [ ] `Vec`, `HashMap`, iterators intro
- [ ] [Rustlings](https://github.com/rust-lang/rustlings) exercises in full

### Phase 1 — Ownership (the core)
- [ ] Ownership rules, moves vs copies, `Clone`
- [ ] Borrowing: shared `&T` vs mutable `&mut T`, borrow rules
- [ ] Lifetimes: why they exist, elision, annotations, `'static`
- [ ] Structs, methods, associated functions, `impl`
- [ ] Enums, `Option<T>`, `Result<T, E>`, `?` operator, `panic!` vs recoverable errors
- [ ] Modules, visibility, `pub`, crate/workspace layout

### Phase 2 — Abstractions
- [ ] Traits, trait bounds, `impl Trait`, dynamic `dyn` dispatch
- [ ] Generics, associated types
- [ ] Closures (`Fn`/`FnMut`/`FnOnce`), iterator adaptors and `Iterator` impl
- [ ] Smart pointers: `Box<T>`, `Rc<T>`, `Arc<T>`, `RefCell<T>`, interior mutability
- [ ] Error handling idioms, custom error types
- [ ] Testing: unit, integration, doc tests; `cargo test`

### Phase 3 — Concurrency & async
- [ ] Threads, `move` closures, channels (`mpsc`)
- [ ] `Mutex`, `RwLock`, `Arc`, the `Send`/`Sync` model
- [ ] Async/await with `tokio`: tasks, `select`, timeouts
- [ ] When to use threads vs async

### Phase 4 — Systems / low-level bridge
- [ ] `unsafe` Rust: raw pointers, what the compiler cannot check
- [ ] FFI: calling C, `#[no_mangle]`, `bindgen` (awareness)
- [ ] `no_std` (awareness), memory layout, `size_of`/`align_of`
- [ ] Profiling & benchmarks (`cargo bench`, `perf`)

---

## Build tasks (solo, zero AI)

Small and real, roughly one per phase:

1. **CLI word-count** — read a file, count word freq, print top 10. (Phase 0–1)
2. **JSON-ish config parser** — parse a small file into structs, clear errors. (Phase 1–2)
3. **Concurrent TCP port scanner** — bounded parallelism, timeouts, tidy output. (Phase 3)
4. **A network tool** — e.g. a Minecraft server pinger in Rust (pairs with your Go
   Minecraft-pinger curiosity), speaking the handshake protocol. (Phase 4)

Acceptance criteria for each: builds with `clippy` clean, has tests, and handles
bad input without panicking (returns `Result`).

---

## Resources

| Resource | Use |
|---|---|
| [The Rust Book](https://doc.rust-lang.org/book/) | Primary text, read cover to cover |
| [Rustlings](https://github.com/rust-lang/rustlings) | Hands-on syntax/ownership drills |
| [Rust by Example](https://doc.rust-lang.org/rust-by-example/) | Bite-sized examples |
| [Rustnomicon](https://doc.rust-lang.org/nomicon/) | Unsafe / advanced (Phase 4) |
| [Async Book](https://rust-lang.github.io/async-book/) | Async/tokio (Phase 3) |
| [std docs](https://doc.rust-lang.org/std/) | Reference |

---

## Convergence note

Once Rust Phase 1 (ownership) is solid, revisit your **Track C** topics — stack/heap,
pointers, processes — and you'll understand them far more precisely. Rust is the
*theory made enforced* track; C++/CP is the *speed* track; Go is the *ship-it* track.
Three languages, three distinct jobs.
