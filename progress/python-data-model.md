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

## Next topics
- Functions, scope, *args/**kwargs, closures (esp. the mutable-default-arg trap,
  which builds directly on this lesson).
