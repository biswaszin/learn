# 🧠 Learn — Second Brain & Learning Protocol

My personal learning system. Tutored sessions produce durable, searchable
knowledge here. Run `pi` from inside this folder so the tutor behavior
(`AGENT.md`) and the `teach` skill (`.pi/skills/teach/`) load automatically.

## Map

| File / dir | Purpose |
|------------|---------|
| [PROTOCOL.md](PROTOCOL.md) | The ritual: how every session runs. Read this first. |
| [curriculum.md](curriculum.md) | Roadmap of all tracks/topics + status. |
| [notes/](notes/) | **Second brain.** Atomic, durable concept notes I re-read. |
| [progress/](progress/) | Per-topic session logs: quiz results, gaps, build tasks. |
| [review.md](review.md) | Spaced-repetition queue — old items resurfaced to fight forgetting. |
| [AGENT.md](AGENT.md) | Auto-loaded tutor instructions for this repo. |

## Daily flow
```bash
git pull                 # start of session
# ...learn with pi...
git push                 # end of session
```

## Progress dashboard

`██` solid/mastered · `▒▒` in progress · `░░` todo. Score = (mastered + 0.5·wip) / topics.
Update this when a topic changes status.

```
TRACK                             PROGRESS BAR (28)              TOPICS         SCORE
A Python · Discord bot        ███░░░░░░░░░░░░░░░░░░░░░░░░░   1/9 mastered      11%
B Go     · website server     ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒░░░░░░   0/5 · 4 wip       40%
C Low-level & Linux           ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0/5 mastered       0%
D GPUs & graphics             ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0/4 mastered       0%
E Web    · personal site      ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒░░░░░░░   0/4 · 3 wip       38%
F Legal + business            ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0/4 mastered       0%
G Rust   · systems            ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0/8 mastered       0%
H DSA    · theory             ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0/5 mastered       0%
I CP     · Codeforces → CM    ░░░░░░░░░░░░░░░░░░░░░░░░░░░░   0/5 mastered       0%
J Physics· transformers       ▒░░░░░░░░░░░░░░░░░░░░░░░░░░░   0/6 · 1 wip        8%
OVERALL (wip counts half)     ██▒▒░░░░░░░░░░░░░░░░░░░░░░░░   1/55 mastered      9%
```

**Live blockers (as of 2026-09-14):**
- J Physics — transformers diagnostic quiz awaiting answers.
- B Go + E Web — Tour-refresh questionnaire awaiting written answers; build task blocked.
- H DSA + I CP — calibration answers (CF rating, volume, C++ level) outstanding.
- A Python — "Mutation Detective" build task assigned, not started.
- C/D/F — queued, no action yet. G Rust — parked until CP stabilises.
- E Web — front-end session open (2026-09-19): CSS relative-path bug + responsive design;
  warm-up + spot-the-bug quiz awaiting answers. See `progress/web-html-css.md`.

## Notes index
- [python-references-mutability.md](notes/python-references-mutability.md) — objects, aliasing, mutability vs rebinding
- [astro-basics.md](notes/astro-basics.md) — what Astro is + how this site maps onto it
