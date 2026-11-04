# Backlog

> Last verified 2026-11-04 against `f8ec418`. **This file is an index.** Each
> item is one line pointing to where its detail lives. Items found after this
> file was created are written in full. Close an item by striking it through
> and dating the strike. Never delete.

## Blocked on Ian

- [ ] **How will the course's use be measured?** [VISION.md](VISION.md)
  Question 1.
- [ ] **Licence or none?** [VISION.md](VISION.md) Question 2.

## Dependencies

- None. No `package.json`; GitHub Pages builds with Jekyll. Open Dependabot
  alerts: 0. Open PRs: none (`gh pr list -R cre3tr/digital-hygiene-course
  --state open` printed nothing on 2026-11-04).

## Bugs and defects

- [ ] **The six-doc files must be kept off the published site (new
  2026-11-04).** `_config.yml` excludes only `README.md` and `CLAUDE.md`, and
  CLAUDE.md says a new hand-written file "needs its name added to the
  `exclude:` line in `c-a-r-t-m-a-n/scripts/hygiene/build.mjs`. Without that,
  Jekyll publishes it." Add `MISSION.md`, `VISION.md`, `BACKLOG.md`,
  `SECURITY.md` and `ARCHITECTURE.md` there, run its `--write`, and merge both
  PRs, **before** this commit is pushed. Not done in this commit because
  `_config.yml` is generated and `c-a-r-t-m-a-n` is a different repo.

## Docs drift (new 2026-11-04)

- [ ] **CLAUDE.md says "The only hand-written files are `README.md` and this
  `CLAUDE.md`".** With this commit that is no longer true; the line needs
  updating when the exclude change lands. Not edited here (CLAUDE.md has no
  start-up list to extend).
- [ ] **`../haven-ea/context/repo-map.md` row for this repo says "No
  `CLAUDE.md`".** One has existed since `c429ec7` (2026-10-29).
- [ ] **Planning notes still show the old Pages title** ("Digital Hygiene Pro",
  `ventures/cartman-systems/digital-hygiene-course.md`, "What it is today").
  That section is dated 2026-10-23 and describes the state before the rewrite;
  later sections supersede it.

## Ideas (unprioritised, not commitments)

- A dated "facts last checked" line on lessons that quote phone numbers.
- Retire the static copy once the interactive copy shows use.
