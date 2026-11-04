# digital-hygiene-course

The static copy of Cartman Systems' digital hygiene course: six short lessons
for a small business team. Served by GitHub Pages at
`cre3tr.github.io/digital-hygiene-course`. It sends nothing. The interactive
copy, which can send a team member's results to Cartman Systems, is at
https://cartman.systems/hygiene.

> Last verified 2026-11-04 against `f8ec418`, clean tree.

## Status

**Live, stable, generated.** <https://cre3tr.github.io/digital-hygiene-course/>
answered HTTP 200 on 2026-11-04, and `/zzz-nonexistent` answered 404. The
interactive copy at <https://cartman.systems/hygiene> answered 200. Last
content change 2026-10-23; last commit 2026-10-29 (`CLAUDE.md`). Public repo,
branch `main`.

## Where everything lives

| Question | File |
|---|---|
| Why does this exist? | [MISSION.md](MISSION.md) |
| Where could it go? Questions for Ian | [VISION.md](VISION.md) |
| What is open | [BACKLOG.md](BACKLOG.md) |
| How to report a problem | [SECURITY.md](SECURITY.md) |
| How it is built | [ARCHITECTURE.md](ARCHITECTURE.md) |
| Agent rules | [CLAUDE.md](CLAUDE.md) |

## Traps for a cold start

1. **Do not edit the lesson pages here.** They are overwritten by the next
   generator run, and the check reports a hand edit as drift.
2. **A new hand-written `.md` file is published by Jekyll** unless its name is
   in the generator's `exclude:` list (CLAUDE.md). See [BACKLOG.md](BACKLOG.md).
3. The generator lives in a different repo (`c-a-r-t-m-a-n`).

## Original README (unchanged below)

**Every page here is generated. Don't edit them in this repo.** The words come
from one copy source in Cartman's private planning repo, and
`c-a-r-t-m-a-n/scripts/hygiene/build.mjs` writes both copies from it:

    node scripts/hygiene/build.mjs            # in c-a-r-t-m-a-n: check, exit 1 on drift
    node scripts/hygiene/build.mjs --write    # regenerate both copies

Generated here: `index.md`, `lesson-1.md` to `lesson-6.md`, `monthly.md`,
`_config.yml` and `_layouts/default.html`. This README and `CLAUDE.md` are
hand-written and excluded from the site (`_config.yml`).

Until 2026-10-23 this repo held an earlier version for individuals, "Digital
Hygiene Pro". It is in git history.
