# Topic: Python Data Model — References & Mutability

Status: [x] mastered (core), keep in review rotation

## Covered
- Variables are name tags on objects, not boxes.
- Multiple names can tag the same object (aliasing).
- Mutable (list, dict, set) vs immutable (int, str, tuple, bool, frozenset).
- Mutation (in-place, all names see it) vs rebinding (`=`, points name at new object).
- Immutable types only support rebinding, never item assignment.

## Quiz results (session 1)
- Q1 (b = b + [4] on shared list): WRONG initially (said A, ans B) — gap: confused
  rebinding via `+` with in-place mutation.
- Q2 (dict aliasing): CORRECT.
- Q3 (string item assignment): WRONG initially — thought s[0]="H" works; gap:
  reading vs writing for immutable types.
- Q4 (append then rebind): CORRECT after re-teach.
- Q5 (tuple immutability): CORRECT after re-teach.
- Verdict: gaps closed same session. Re-test in ~3 sessions.

## Assigned build task (solo, no AI)
- "Mutation Detective" CLI — see below. Status: [ ] not started.

## Session 2 — 2026-09-19 (spaced-repetition re-test) — MISS
- W1 re-test: aliased list, `b.append(2)` then print a and b. Learner answered
  `b=[1,2]`, `a=[1]`.
  - HALF right: append result on `b` correct. **`a` is WRONG** — should be `[1,2]`.
  - Regression of the session-1 gap, new flavour: learner now thinks a mutation
    only affects "the name I used" — misses that both names share one object.
- Not yet answered: the `b = b + [2]` variant of W1.
- Action: re-teach (one object, two nametags), cross-question, extra written follow-ups.
- Re-teach #1 + cross-quiz (2026-09-19):
  - R1 `b.append(9); print(a)` → learner said `a = 1` ❌ (should be `[1, 9]`).
    Mutation branch STILL leaking after re-teach. Not advancing.
  - R2 explain-back "because it's the same list" — core intuition right, but vague.
  - R3 `b = b + [2]; print(a,b)` → `[1] [1,2]` ✅ (rebinding branch solid).
  - Diagnosis: rebinding ✅ / in-place-mutation application ❌. Recites aliasing but
    fails to apply it. Needs concrete trace + more reps.
- Re-teach #2 + re-quiz (2026-09-19):
  - Q1 dict aliasing `y["n"]=5` → said x shows 5 ✅ (core right; full output `{'n': 5}`).
  - Q2 `other += [30]` on an aliased list → said nums stayed `[10,20]` ❌
    (want both `[10,20,30]`). New gap: `+=` on a list is IN-PLACE (`__iadd__` → `extend`),
    NOT `x = x + y`.
  - Q3 explain-back: not answered yet.
- Next: teach `+=` vs `x = x + y` (and immutable contrast); cross-quiz; get Q3 in writing.
- Status: `[x] mastered` → back to `[~]`; re-test next session.

## Next topics
- Functions, scope, *args/**kwargs, closures (esp. the mutable-default-arg trap,
  which builds directly on this lesson).
