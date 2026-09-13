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
- [x] Python data model: objects, references, mutability
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
- [ ] Deployment basics (stretch: Fly/Render/VPS)

## Track F — Indian Legal Research + Business/Market
- [ ] Structure of Indian law & sources
- [ ] How to do legal research (statutes, case law, citations)
- [ ] Business fundamentals: markets, value, unit economics
- [ ] Reading the market: startups, competition, moats

---

## Sequencing note
Tracks A + C + D + E all reinforce each other (Python teaches concepts; low-level
explains *why*; GPU/web give concrete targets). Recommended order:
**A → C (interleaved) → E → D → B → F**, but the learner drives.
