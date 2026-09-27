# DSA + Competitive Programming Roadmap (target: Codeforces Candidate Master, 1900+)

**Track(s):** H (DSA) + I (CP)
**Language of choice for CP: C++17/20** (this is the default recommendation — see below)
**Practice budget:** ~10–12 of your ~15 hrs/week
**Honest timeline:** near-scratch → CM ≈ 2000–3000 focused hours (≈ 2.5–3.5 yrs at this pace).
From Specialist (1400) → CM ≈ 800–1200 hours (≈ 1–1.5 yrs). From Expert (1600) → CM ≈ 400–700 hours.

---

## Why C++ for CP (and where Rust fits)

Competitive programming at CM level is a **speed + volume** game. C++ wins because:

- Editorial/solution culture is C++-first; nearly every solution you read is C++.
- The standard library gives you exactly CP's primitives: `sort`, `lower_bound`,
  `map`/`set` (balanced trees), `priority_queue`, `bitset`, `next_permutation`.
- Time limits are calibrated with C++ in mind. Python TLEs around 1600–1700.
- Fast I/O, custom comparators, and 128-bit ints are easy.

**Rust for CP is hard mode.** It is possible (Codeforces supports Rust 2021), but
you pay for the borrow checker, verbose I/O, and the absence of a ready-made
library ecosystem. It is *not* the efficient route to CM.

**Recommendation:** Use **C++ for DSA/CP**. Learn **Rust separately** as the
systems-language track (see `rust-roadmap.md`), folded into your existing
low-level track — ideally in parallel at low intensity, or after you stabilise
around 1400–1600. Rust and C++ coexist fine long-term; just don't make Rust your
contest language.

---

## The Three-Sided System

DSA/CP progress is not a reading list. It is three loops running together:

1. **Theory (DSA)** — learn the topic, understand *why* it works, be able to prove it.
2. **Drilling (CP)** — solve problems in the topic until you can *recognise* when to use it.
3. **Meta (contest craft)** — upsolving, virtual contests, templates, stress tests, tie-breaking, interacting with the judge.

Most people fail by only doing (1). Recognition under time pressure is built by (2) and (3).

---

## Phases (theory + target rating)

Ratings are the CF band the *average* problem in that phase sits at. You are done
with a phase when you can routinely solve problems ~200 above your current rating.

### Phase 0 — Language & foundations — target 800–1200 (Newbie → Pupil)
- [ ] C++ basics, fast I/O (`ios_base::sync_with_stdio(false); cin.tie(nullptr);`)
- [ ] STL fluency: `vector`, `array`, `string`, `pair`, `map`/`set`/`unordered_*`,
      `priority_queue`, `sort`, `lower_bound`/`upper_bound`, custom comparators
- [ ] Complexity analysis (Big-O), reading limits → guessing intended complexity
- [ ] Arrays, strings, sorting, binary search (library + hand-rolled)
- [ ] Two pointers, prefix sums, sliding window
- [ ] Bit manipulation basics (`&`, `|`, `^`, `<<`, `>>`, popcount, subsets via masks)
- [ ] Basic math: gcd/lcm (Euclid), primality, sieve of Eratosthenes, fast exponentiation, modular arithmetic
- [ ] Implementation/simulation/casework discipline

### Phase 1 — Core techniques — target 1000–1400 (Pupil → Specialist)
- [ ] Greedy + exchange argument, classic greedy sorting
- [ ] Constructive problems and invariants
- [ ] Binary search **on the answer** (parametric search)
- [ ] Difference arrays, 2D prefix sums
- [ ] Recursion, backtracking + pruning, meet-in-the-middle intro
- [ ] Number theory: divisor enumeration, prime factorisation, sieve variants, nCr precompute with modular inverse
- [ ] Coordinate compression, offline sorting tricks
- [ ] Stacks: monotonic stack, next-greater-element; deques

### Phase 2 — Graphs & DP intro — target 1300–1600 (Specialist → Expert)
- [ ] Graph representation (adjacency list/matrix), edge lists
- [ ] BFS, DFS, connected components, bipartite check, grid traversal
- [ ] Topological sort, cycle detection (directed + undirected)
- [ ] DSU (union-find with path compression + union by size)
- [ ] MST: Kruskal, Prim
- [ ] Shortest paths: Dijkstra, 0-1 BFS, Bellman-Ford, Floyd-Warshall
- [ ] Trees: traversals, subtree sizes, diameter, Euler tour / tin-tout
- [ ] DP intro: 1D DP, coin change, knapsack (0/1 + unbounded), LIS (O(n²) → O(n log n)),
      LCS, grid DP, bitmask DP intro, DP on subsets
- [ ] Combinatorics: Pascal's triangle, stars and bars, inclusion–exclusion intro, Catalan

### Phase 3 — Intermediate DS & algorithms — target 1600–1900 (Expert → CM edge)
- [ ] Fenwick tree (BIT): point update, prefix/range sums, inversion counting
- [ ] Segment tree: point update, range query, merge functions, descent on tree
- [ ] Sparse table / RMQ, disjoint sparse table
- [ ] Binary lifting + LCA; K-th ancestor
- [ ] Advanced DP: interval DP, tree DP, DP on DAG, digit DP, SOS/subset-sum DP,
      DP + binary search, monotonic-queue optimisation
- [ ] Number theory: modular inverse (Fermat + extended Euclid), Euler's totient, CRT,
      Legendre's formula, Möbius intro, multiplicative functions
- [ ] Strings: polynomial hashing, KMP / prefix function, Z-function, prefix automaton
- [ ] Game theory: Nim, Sprague–Grundy
- [ ] Probability & expected value basics

### Phase 4 — CM-level topics — target 1900–2100+ (CM)
- [ ] Segment tree with lazy propagation; merge-sort tree; segment tree beats (intro)
- [ ] Sqrt decomposition; Mo's algorithm (with updates); offline queries
- [ ] Advanced graphs: SCC (Kosaraju/Tarjan), bridges & articulation points,
      2-SAT, max-flow / min-cut (Dinic), bipartite matching (Hopcroft–Karp), min-cost flow (intro)
- [ ] Advanced strings: suffix array, suffix automaton, Aho–Corasick, suffix tree (awareness)
- [ ] Math: matrix exponentiation, FFT/NTT (intro), Burnside/Polya, Lucas theorem, Gaussian elimination over GF(2)
- [ ] DP optimisations: divide & conquer, convex hull trick, Knuth optimisation, Aliens trick (intro)
- [ ] Persistent data structures (persistent segtree), Li Chao tree
- [ ] Computational geometry basics: vectors, cross/dot, convex hull, point-in-polygon

---

## The Practice Loop (this matters more than the topic list)

Per contest:
1. Compete (or virtual) — 2–3 virtual contests/week on top of real ones.
2. **Upsolve**: every unsolved problem gets solved within 48h, no exceptions.
3. **Editorial discipline**: genuinely struggle 30–60 min first. Then read the editorial,
   close it, and **re-implement from scratch**. Never copy-paste.
4. Write down *why you missed it*: wrong idea / unknown technique / implementation bug / misread.

Spaced repetition:
- Re-solve failed problems after ~1 week, then ~1 month.
- Keep a per-tag weakness list; when a tag is weak, drill 10–15 problems of that tag.

Volume reality check (CM): on the order of **1000–1500 solved problems**. Early on
4–6/day is normal; later 2–3/day of *harder* problems.

Personal template (build it yourself):
- Fast I/O, common typedefs (`ll`, `vi`, `pii`), `#define` helpers,
  debug macros (`dbg(...)`), modular arithmetic helpers, sieve, DSU, Dijkstra, segtree.
- A snippet library you can recall fast — but **write every snippet once by hand**.

---

## Resources

| Resource | Use |
|---|---|
| [USACO Guide](https://usaco.guide) | Best structured DSA→CP roadmap; follow Silver→Gold→Platinum |
| [CP-Algorithms](https://cp-algorithms.com) | Theory/reference for every algorithm |
| [CSES Problem Set](https://cses.fi/problemset/) | ~300 curated DSA problems; do it in full |
| [Competitive Programmer's Handbook](https://cses.fi/book/book.pdf) | Free, concise theory (Laaksonen) |
| [Codeforces EDU](https://codeforces.com/edu/courses) | ITMO pilot courses (binary search, two pointers, segtree, suffix array…) |
| [AtCoder ABC/ARC](https://atcoder.jp) | Higher-quality, calmer problems than CF Div2 |
| [Library Checker](https://judge.yosupo.jp) | Verify your implementations against a judge |
| YouTube: Errichto, Colin Galen, William Lin, SecondThread, Utkarsh Gupta | Technique walkthroughs + mindset |

---

## Milestones (checkpoints, not gates)

- [ ] Solved CSES Introductory + Sorting/Searching fully
- [ ] 100 problems solved on CF; comfortable in Div 4 / early Div 3 → **Pupil (1200)**
- [ ] CSES Graph + DP sections done; consistent Div 3 solves → **Specialist (1400)**
- [ ] Segment tree + LCA + intermediate DP solid; Div 2 C/D → **Expert (1600)**
- [ ] Phase 4 topics + 1000+ problems + strong contest consistency → **Candidate Master (1900+)**

---

## Start-of-track build task (do it solo, zero AI)

1. **What we're building** — a working C++ CP environment + first blood.
2. **Resources needed** — `g++` (or clang), an editor/IDE, a Codeforces account, a local test-file setup.
3. **Docs to read** — `cppreference` for `std::vector`, `std::sort`, `std::lower_bound`; CF "how to practice" blog by Errichto.
4. **Acceptance criteria (goal only, no implementation given):**
   - Compile and run a C++ file from the terminal with `-O2 -std=c++20`.
   - Solve the first 10 problems of the CSES *Introductory* section **and** 5 CF problems ≤ 1000.
   - For each, write one line on the intended complexity and why it fits the limit.
   - Build a `template.cpp` you will reuse — from your own fingers.
5. **Questionnaire** — answer these in writing before we go further:
   - Q1. `ios_base::sync_with_stdio(false)` — what does it change, and what breaks if you mix `printf`/`cout` after it?
   - Q2. You have `n = 2·10^5` and 2 seconds. Is an O(n²) solution safe? Show the arithmetic.
   - Q3. Given a sorted `vector<int> v`, what does `lower_bound(v.begin(), v.end(), x)` return when `x` is absent, and why is it not "not found"?
   - Q4. Explain in your own words why prefix sums turn O(n) range queries into O(1).
