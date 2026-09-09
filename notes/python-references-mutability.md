# Python: References & Mutability
**Track:** A-Python   **Status:** solid   **Last reviewed:** session 1

## In one line
A variable is a name tag on an object, not a box — so mutation is shared, but
rebinding (`=`) just moves the tag.

## Explanation (my words)
> TODO: rewrite this section in your OWN words — that's what makes it stick.
Multiple names can point to the same object. Changing a mutable object in place
(`list.append`, `d[k]=v`, `x[0]=...`) is seen by every name on it. Assigning with
`=` (including `b = b + [4]`) creates/points to a (possibly new) object and only
moves that one name. Immutable types (int, str, tuple, bool, frozenset) can't be
mutated at all — operations always produce new objects.

## Gotchas / edge cases
- `b = b + [4]` does NOT change the shared list; `b.append(4)` does.
- `s[0] = "H"` on a string raises TypeError (immutable).
- `t[0] = 9` on a tuple raises TypeError (immutable).
- Identity vs equality: `is` (same object) vs `==` (same value).

## Links
- next: functions, scope, and the mutable-default-argument trap


## My own words
So far what I've understood is the fact that. Mutable object is like a box where everyone can
actually put the nametag on it. Like two names being "a" and "b". Some of the types of mutable
objects are lists, dictionaries. 

So whenever let's say im doing a = list. and b = a. So list will be a box which will have 2 stickers
on it. so a and b can access the list. But apart from that, if i do b = b + [4].
Firstly it'll create a new list of b (which is "a") and then add '4'.
Then finally the sticker of B will be placed on top of the newly made list!

Similarly, immutable objects exists too. Types being, int, str, bool, tuples and etc.
