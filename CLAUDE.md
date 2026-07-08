# CLAUDE.md

Guidance for working in this repository.

## What this is

*Causal Theory* — a mathematics monograph (book draft v0.2), written in **Markdown with LaTeX
math** (`$…$` inline, `$$…$$` display). There is **no code, no build, no test suite**. The
deliverable is prose and proofs. "Verification" means re-deriving claims and checking
cross-references, not running anything.

## Layout

- `front_matter.md` — title, conventions, audience reading paths.
- `part_1/ … part_6/` — `part_N.md` is the part title **and a contents list** for that part;
  chapters are `chapter_K.md`. Standalone sections (interludes) get their own descriptively
  named file, e.g. `part_1/category_of_causal_structures.md`.
- `appendices/appendix_A.md … appendix_H.md` — proofs (C), proof→location map (D),
  citation ledger (F); G–H park seed chapters (the logical boundary; related frameworks).

## House style (match it when editing)

- Numbered items with **bold lead-ins**: `**1.5 Definition (…).**`, `**§1 Definition (…).**`.
  Chapters number `K.x`; appendices `A–H`; standalone interludes use a self-contained scheme
  (e.g. `§1–§n`) so numbering never collides across files.
- Proofs are inline when ≤ 3 lines, otherwise deferred to App. C; close every proof with `$\square$`.
- Starred (`*`) sections and chapters are optional material (categorical or graded). `[verify]`
  marks a citation gated by the ledger in App. F.
- Terse, dense prose. Cross-reference by item number ("Def. 1.5", "12.1", "App. C").

## When you edit — keep the indexes in sync (IMPORTANT)

Any change to the set or naming of chapters/sections must be reflected in the index files in the
**same** change:

1. **`part_N/part_N.md`** — the contents list for that part. Add/rename/remove/reorder the entry,
   keeping each line as `Title — \`filename.md\``.
2. **`front_matter.md`** — update the audience reading paths if the change affects what a given
   audience reads (a new foundational/categorical section, a moved chapter, etc.).
3. **Cross-references** — when adding a section that another chapter should point to (or vice
   versa), add the back-reference. Verify every item number you cite (`Def. 1.5`, `12.1`, …)
   actually exists and is correctly numbered.

Before finishing any edit, re-read the touched index lines and cross-references to confirm titles,
filenames, and item numbers all still match the files on disk.
