# Ariadne's Thread

A research notebook, written as an [mdBook](https://rust-lang.github.io/mdBook/), on one question:

> As immersive simulations get more realistic, how does a person reliably find their way back out, to the place, the reality, the self and the time they started from?

It collects what is already known (VR research, psychology, security, cave diving, myth) and brainstorms designs for a "find my way back" thread.

## Read it

```sh
cargo install mdbook   # once
mdbook serve --open    # live preview at http://localhost:3000
mdbook build           # static site in ./book
```

## Layout

| Path | What |
|---|---|
| `src/problem/` | What "where you started" means, why it gets harder, threat models |
| `src/research/` | What research already knows, with citations |
| `src/elsewhere/` | Lessons from caves, fires, animals, security, minds, myth, philosophy |
| `src/brainstorm/` | Requirements, the idea catalogue, comparison, prototypes, open questions |
| `src/appendix/` | Bibliography, glossary, research log, idea template |

## Adding to it

- New idea: copy the card in `src/appendix/idea-template.md` into the right `src/brainstorm/ideas-*.md` page, then add a row to `src/brainstorm/comparison.md`.
- New source: add it to `src/appendix/bibliography.md` and note it in `src/appendix/research-log.md`.
- Mark anything unverified or speculative as such.
