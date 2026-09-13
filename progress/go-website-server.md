# Topic: Personal Website in Go (Track B + E)

Status: [~] in progress — Go refresh via Tour, then serve existing site with net/http

## Context
- Site already exists in `../personal-website/` (index.html + css/ + images/ + js/).
- Plan: 3-day build — Day 1 Tour refresh, Day 2 HTTP bridge, Day 3 serve locally.
- Deploy (Fly/Render/VPS) is stretch, not required for Day 3.

## Tour of Go scope (agreed 2026-09-11)
- Basics: full (packages → closures + 4 exercises).
- Methods/interfaces: up to + including Errors + exercise. STOP after Exercise: Errors.
- Deferred: Readers/Images, Generics, Concurrency (save for Minecraft-pinger).

## Covered (session 2026-09-11)
- GitHub Pages static model vs Go net/http dynamic model.
- Client vs server; where code runs; why secrets can't live on Pages.
- Handler/Mux concept at overview level only (no implementation given).
- Readiness quiz assigned (go mod, path→file mapping, concurrent requests).

## Quiz results
- Pending: 3 readiness questions assigned, awaiting learner answers.

## Assigned build task (solo, no AI) — not yet started
- Goal: `go run .` serves existing site on localhost:8080; `/` → index, static dirs work, 404 on bad path, runs from any cwd.
- Status: [ ] blocked on Tour refresh. Unblock when learner reports Tour done.

## Next
- Learner does Tour slice above, reports back.
- Then: full task brief (goal + acceptance + questionnaire per AGENT.md).
