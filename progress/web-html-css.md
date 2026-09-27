# Topic: Web — HTML/CSS Mental Models (Track E, anchor: personal-website)

Status: [~] in progress — session opened 2026-09-19

## Context
- Site lives in `../personal-website/` (index.html, css/style.css, images/, js/ is empty).
- The site is the learner's own build. Per the Golden Rule the tutor **coaches** here
  (explain → quiz → assign); the learner types the code.

## Session — 2026-09-19: front-end debugging + responsive design
Intent: "code + learn" on the real site — fix real bugs and learn the model behind them.

### Bug found (spot-the-bug quiz issued)
- `css/style.css`: `body { background-image: url('images/1-the-backwater.jpg') }`
- CSS relative URLs resolve against the **stylesheet's own location**, not the HTML.
  So the browser requests `css/images/1-the-backwater.jpg` → 404. Background never shows.
- Correct path: `../images/1-the-backwater.jpg`.
- Status: awaiting learner answer.

### Concepts queued
1. CSS relative URL resolution (the bug above).
2. Responsive design: fixed `.hero-text { width: 700px }` + flex row breaks on narrow screens.
3. `js/` is currently empty — entry point for a later JS concept.

### Quiz results
- 2026-09-19 — W1 Python warm-up: PARTIAL/MISS (see `progress/python-data-model.md`).
- Awaiting: W2 (client/server), bug Q1/Q2, and the re-teach cross-questions.
- W2 deferred by learner ("not for now"); stays in review queue.

## Feature log (project mode — opened 2026-09-19)
Working agreement: inside `personal-website/` the learner drives features; the tutor
 teaches "how", the learner implements, the tutor reviews the diff. The quiz ritual
 stays in `learn/`.

### F1 — spacing between "Kol, India" and "[ Gears ]"
- Request: even out the vertical gap in the hero sidebar.
- Taught: margin vs padding; the global reset (`* { margin: 0 }`) killed the h2's
  default margins; add space to the *following* element via `margin-top`; use a
  spacing scale in `rem`.
- Implementation on disk: `.hero-gears { margin-top: 1.5rem; }` (css/style.css:103) = 24px.
- Review: **PASS.**
  - ✅ correct selector + property, `rem`, targeted change, no layout side effects.
  - ✅ `1.5rem` = 24px (root/`html` default 16px base — **not** body's 18px).
  - ✔ cosmetic: two blank lines before `/* Utility Classes */`; one is enough.
- Earlier "said 1.5rem / file had 1rem" nit was a stale save — resolved 2026-09-19.
- Status: **accepted** 2026-09-19.

### F2 — responsive layout (in progress 2026-09-20)
- Taught: fixed vs fluid widths, flex shrink/wrap, media queries, `clamp()`.
- **Part 1 (base fluid changes) — learner implemented all:**
  - `.hero-text` → `max-width:700px; width:100%; min-width:0` ✅
  - `.hero-personal` → `flex:0 0 auto` (min-width removed) ✅
  - `.hero-section .container` → `gap:2rem; align-items:flex-start` ✅
  - `.navbar .container` → `flex-wrap:wrap; gap:1rem` ✅
  - `.navbar` padding → `clamp(1rem,3vw,2.5rem)` ✅
  - `.avatar-name` font-size/padding → `clamp()` ✅
  - removed `white-space:nowrap` from nav links ✅
- Review: **PASS.** Decisions/nits:
  - removing `justify-content: space-between` from the hero container changes right
    alignment (hero-text no longer flush right) — intentional?
  - below ~440px the nav menu can still overflow until Part 2/3 breakpoints land.
- Next: Part 2 (stack hero ≤900px) + Part 3 (navbar ≤480px).
- **Part 2 done 2026-09-20 — PASS.** Added at bottom of file:
  `@media (max-width: 900px) { .hero-section .container { flex-direction: column; align-items: stretch } .hero-text { max-width: 100% } }` ✅
  Learner also restored `justify-content: space-between` on the hero container (keeps the
  desktop right-flush look). Correct: in column mode `align-items: stretch` overrides the
  base `flex-start` so both blocks go full-width.
- Next: Part 3 — `@media (max-width: 480px)` navbar stacking + menu `flex-wrap`.

## Site audit — 2026-09-19 (brutally honest, vs kishaloyroy.com)
Fetched and inspected both sites live. Evidence: 0 `@media` queries, 0 `:hover`/`:focus`
 rules, 2 `<h1>`, 4 `href="#"` dead links, no meta description/OG, `background-image`
 404s, that image is **4.0 MB**.

Scorecard: identity A− · layout/responsive F · a11y D · semantics C− · perf D− ·
SEO/meta F · content depth D · code quality C.

**P0 bugs:** fix bg 404 + add `background-size`/`no-repeat` (4MB image would tile full-size);
kill/placeholder dead nav links; single `<h1>`; one font request + single preconnect;
width/height attrs on images.
**P1 responsive:** add media query breakpoint; fluid widths (`max-width`/`flex` instead of
 fixed 700px/250px); navbar collapse.
**P2 a11y/meta:** hover+focus states, link distinction, alt text, `<main>`/`<footer>`;
 meta description + OG/Twitter.
**P3 content:** real Projects page, About/footer, optimize images to webp.

Key lesson: don't copy Kishaloy's *look*; copy his *discipline* (tokens, landmarks,
media queries, meta, content depth). The terminal/pixel aesthetic is a real differentiator —
keep it.

## Other open items (not yet done in project mode)
- Background (2026-09-20): **resolved.** Learner chose no background image; flat
  `--primary-color` only, `reze.jpg` is the avatar. `background-image` line removed ✅.
  Nit (accepted): still uses `background:` shorthand instead of `background-color:`.
- Cleanup: `senjougahara.jpg` deleted (unstaged); `reze-bak.jpg` still present.
- Note: learner works directly on `main` (solo, no branches).
- `js/` is empty — no JS features yet.

### Next
- Confirm F1 value. Then next feature request.
