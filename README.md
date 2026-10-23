# digital-hygiene-course

The static copy of Cartman Systems' digital hygiene course: six short lessons
for a small business team. Served by GitHub Pages at
`cre3tr.github.io/digital-hygiene-course`. It sends nothing. The interactive
copy, which can send a team member's results to Cartman Systems, is at
https://cartman.systems/hygiene.

**Every page here is generated. Don't edit them in this repo.** The words come
from one copy source in Cartman's private planning repo, and
`c-a-r-t-m-a-n/scripts/hygiene/build.mjs` writes both copies from it:

    node scripts/hygiene/build.mjs            # in c-a-r-t-m-a-n: check, exit 1 on drift
    node scripts/hygiene/build.mjs --write    # regenerate both copies

Generated here: `index.md`, `lesson-1.md` to `lesson-6.md`, `monthly.md`,
`_config.yml` and `_layouts/default.html`. This README is excluded from the
site (`_config.yml`).

Until 2026-10-23 this repo held an earlier version for individuals, "Digital
Hygiene Pro". It is in git history.
