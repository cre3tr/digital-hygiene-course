# CLAUDE.md — digital-hygiene-course

The public, static copy of Cartman Systems' six-lesson digital hygiene course,
served by GitHub Pages at `cre3tr.github.io/digital-hygiene-course`. The
interactive copy is `cartman.systems/hygiene`.

## The one rule: don't edit the pages here

Every page in this repo is **generated**. `README.md` lists which files and the
two commands, and it is the single copy of that list. Change the words in the
copy source (`haven-ea/ventures/cartman-systems/digital-hygiene-course-copy.md`),
then run `node scripts/hygiene/build.mjs --write` from `c-a-r-t-m-a-n`. A hand
edit here is overwritten on the next write, and the check mode (no `--write`)
reports it as drift, with exit 1.

The only hand-written files are `README.md` and this `CLAUDE.md`. Both are kept
off the site by `_config.yml`'s `exclude`. That file is generated too, so a new
hand-written file needs its name added to the `exclude:` line in
`c-a-r-t-m-a-n/scripts/hygiene/build.mjs`. Without that, Jekyll publishes it.
`CLAUDE.md` was added there on 2026-10-29.

## Checking it

- `node scripts/hygiene/build.mjs` in `c-a-r-t-m-a-n` exits 0 when both copies
  match the source. On 2026-10-29 it listed 12 outputs: 2 in `c-a-r-t-m-a-n`,
  10 here.
- No build step or test suite here. GitHub Pages runs Jekyll on push to `main`.
- The live site answered 200 on 2026-10-29.

## History

Until 2026-10-23 this repo held "Digital Hygiene Pro", an earlier course for
individuals. It is in git history; don't restore it over the generated pages.
