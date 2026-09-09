# Learning Protocol

The systematic ritual every session follows. Both the human and the tutor
(agent) adhere to this. It exists so knowledge compounds instead of evaporating.

## Core principles
1. **Active recall over re-reading.** Being quizzed beats re-reading notes.
2. **Spaced repetition.** Old material resurfaces via `review.md`, not just new.
3. **Build with zero AI.** The tutor never writes the learner's project/practice
   code. It explains, quizzes, diagnoses, and assigns — hints only.
4. **Atomic notes.** Each durable idea gets its own small note in `notes/`,
   written in the learner's own words, linkable and searchable.
5. **Everything on disk.** No progress lives only in chat.

## Session lifecycle
1. **Open** — `git pull`. Tutor reads `curriculum.md`, relevant `progress/*`,
   and pulls 1–2 due items from `review.md` as warm-up quiz.
2. **Learn loop** (repeat per concept):
   - Explain one small chunk.
   - Quiz (MCQ / predict-output / spot-the-bug / explain-back).
   - Grade honestly; re-teach from a new angle if shaky; re-quiz.
   - Capture a durable **atomic note** in `notes/<slug>.md`.
3. **Apply** — Tutor assigns an *adjacent* build task (related to a real project,
   not identical). Learner builds it solo, later, with zero AI.
4. **Close** — Update `progress/<topic>.md`, `curriculum.md` status, add misses
   to `review.md`, update the notes index. `git push`.

## Note format (notes/<slug>.md)
```markdown
# <Concept>
**Track:** A-Python   **Status:** learning|solid   **Last reviewed:** YYYY-MM-DD

## In one line
<the idea compressed to a sentence>

## Explanation (my words)
<learner-phrased explanation — this is what makes it a second brain>

## Gotchas / edge cases
- ...

## Links
- related: [other-note](other-note.md)
```

## Status markers
`[ ] todo`   `[~] in progress`   `[x] mastered`

## Review scheduling (simple SM-2-lite)
- Missed or shaky → re-test next session.
- Got it → re-test in ~3 sessions, then ~1 week, then ~1 month.
- Record `last tested` date on each review item.
