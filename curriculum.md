# Curriculum

Status: `[ ] todo`  `[~] in progress`  `[x] mastered`

Learner anchors (real projects, to be built with ZERO AI):
- Discord bot (Python) fetching top/helpful posts from subreddits (e.g. r/developersindia)
- Personal website (in progress, learning by breaking/fixing)
- Work stack: Python + Go (startups)
- Curiosities: GPUs (Minecraft optimization mods), low-level, Linux
- Non-technical: Indian Legal Research + business/market fundamentals

---

## Track A — Python (anchor: Discord bot) ⭐ suggested start
- [~] Python data model: objects, references, mutability (regressed 2026-09-19; re-teaching alias/mutation)
- [ ] Functions, scope, *args/**kwargs, closures
- [ ] Iterables, iterators, generators, comprehensions
- [ ] Error handling & the exception model
- [ ] Modules, packages, virtualenvs, dependency mgmt
- [ ] Async/await & the event loop (needed for discord.py)
- [ ] HTTP & REST clients (needed for Reddit API)
- [ ] JSON, data modeling, dataclasses/pydantic
- [ ] Testing basics

## Track B — Go (anchor: work)
- [~] Types, structs, slices, maps (Tour of Go Basics — in progress)
- [~] Interfaces & composition (Tour Methods up to Errors — in progress)
- [ ] Goroutines & channels (concurrency model) — deferred to Minecraft-pinger
- [~] Error handling idioms (Tour Errors — in progress)
- [~] Modules & tooling (go mod init/run/build — in progress)

## Track C — Low-level & Linux
- [ ] How memory works: stack/heap, pointers
- [ ] Processes, threads, syscalls
- [ ] Linux fundamentals: filesystem, permissions, processes, shells
- [ ] Compilation & linking; what a binary is
- [ ] A taste of C

## Track D — GPUs & graphics (anchor: Minecraft mods)
- [ ] CPU vs GPU: why GPUs exist, SIMD/parallelism
- [ ] The rendering pipeline (basics)
- [ ] What optimization mods actually do (Sodium/Iris etc.)
- [ ] Shaders at a conceptual level

## Track E — Web (anchor: personal website)
- [~] How the web works: DNS, HTTP, request/response (Pages vs net/http — in progress)
- [~] HTML/CSS mental models (site exists in personal-website/ — in progress)
- [~] Client vs server; where code runs (in progress)
- [ ] Static site generators / component builds (Astro) — evaluating
- [ ] Deployment basics (stretch: Fly/Render/VPS)

## Track F — Indian Legal Research + Business/Market
- [ ] Structure of Indian law & sources
- [ ] How to do legal research (statutes, case law, citations)
- [ ] Business fundamentals: markets, value, unit economics
- [ ] Reading the market: startups, competition, moats

## Track G — Rust (systems language; parallel, low intensity)
> Real engineering language, **NOT** the CP contest language.
- [ ] Toolchain, cargo, crates, project layout
- [ ] Ownership, borrowing, lifetimes (the core)
- [ ] Enums, pattern matching, Option/Result, error handling
- [ ] Traits, generics, iterators, closures
- [ ] Smart pointers (Box/Rc/RefCell), interior mutability
- [ ] Concurrency: threads, channels, Send/Sync, async/tokio
- [ ] Testing, workspaces, docs
- [ ] Unsafe, FFI, no_std (low-level bridge)
- Detail: [tracks/rust-roadmap.md](tracks/rust-roadmap.md)

## Track H — DSA (algorithmic theory backbone)
> CP language: **C++**. See the CP track for why.
- [ ] Phase 0 — complexity, arrays/strings, sorting, binary search, two pointers, prefix sums, basic math, bits
- [ ] Phase 1 — greedy, binary search on answer, difference arrays, recursion/backtracking, number theory & combinatorics
- [ ] Phase 2 — graphs (BFS/DFS, DSU, MST, shortest paths), intro DP, trees
- [ ] Phase 3 — Fenwick/segtree, binary lifting/LCA, intermediate DP, hashing/KMP/Z, CRT/totient, game theory
- [ ] Phase 4 — lazy segtree, Mo's, SCC/2-SAT, flows, suffix structures, FFT, DP optimisations
- Detail: [tracks/dsa-cp-roadmap.md](tracks/dsa-cp-roadmap.md)

## Track I — Competitive Programming (practice + Meta)
> Target: **Codeforces Candidate Master (1900+)**
- [ ] Learn C++ + STL to contest fluency
- [ ] Establish practice loop: contests, virtuals, upsolving, editorial discipline
- [ ] Build personal template + snippet library (by hand)
- [ ] Milestones: Pupil 1200 → Specialist 1400 → Expert 1600 → CM 1900
- [ ] Weak-tag repair cycles (drill gaps, re-solve failures on spaced repetition)
- Detail: [tracks/dsa-cp-roadmap.md](tracks/dsa-cp-roadmap.md)

## Track J — Engineering Physics (B.Tech 1st year)
> Anchor: university exam + genuine understanding. Depth-first, numericals included.

### Theme: Transformers (electromagnetic induction → AC machines)
- [~] Module 0 — Prerequisites (the gap-fillers): magnetic flux & flux density, B–H, MMF/reluctance, Faraday, Lenz, self & mutual inductance, AC RMS/phasors/power factor
- [ ] Module 1 — The ideal transformer: construction, working principle, turns ratio, why V and I trade off
- [ ] Module 2 — The real transformer: core loss (hysteresis + eddy), copper loss, leakage reactance, equivalent circuit, phasor diagram
- [ ] Module 3 — Performance: EMF equation, voltage regulation, efficiency, max-efficiency condition, all-day efficiency, OC/SC tests
- [ ] Module 4 — Types & systems: step-up/down, auto-transformer, three-phase connections (star/delta), CT/PT, parallel operation, cooling
- [ ] Module 5 — Physics deep-dives: magnetostriction (hum), inrush, skin effect, why kVA not kW, why ferrites/SMPS, grid power transmission

---

## Sequencing note
Tracks A + C + D + E all reinforce each other (Python teaches concepts; low-level
explains *why*; GPU/web give concrete targets). Recommended order:
**A → C (interleaved) → E → D → B → F**, but the learner drives.

**New thrust (DSA/CP/Rust):** DSA + CP are one combined effort — C++ is the CP
language, DSA is its theory, CP is the drilling. Run **H + I together** as the
primary new 10–12 hrs/week. Run **G (Rust)** separately at ~3–5 hrs/week, folded
into C, and ideally not from day one — start it once CP basics are stable
(~1200+) so the borrow checker doesn't eat contest momentum.

Honest route verdict: **Rust + DSA + CP all-at-once-from-scratch is not recommended.**
Do DSA/CP in C++; keep Rust as a parallel systems track; that combination is strong.
See [tracks/dsa-cp-roadmap.md](tracks/dsa-cp-roadmap.md) for the reasoning.
