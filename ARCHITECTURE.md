# Architecture

> Last verified 2026-11-04 against `f8ec418`. No package versions apply: there is
> no manifest. Rules for agents: [CLAUDE.md](CLAUDE.md).

## Shape

A Jekyll site on GitHub Pages whose every page is **generated** from a single
copy file in Cartman's private planning repo. This repo is the output, plus two
hand-written files.

```
haven-ea/ventures/cartman-systems/digital-hygiene-course-copy.md   (the words)
        │
        ▼
c-a-r-t-m-a-n/scripts/hygiene/build.mjs   (check by default, --write to generate)
        ├─► c-a-r-t-m-a-n/public/hygiene.html + API   ──► cartman.systems/hygiene (interactive)
        └─► this repo: index.md, lesson-1..6.md, monthly.md, _config.yml, _layouts/default.html
                 │
                 ▼  push to main
           GitHub Pages (Jekyll) ──► cre3tr.github.io/digital-hygiene-course (static, sends nothing)
```

## Components

| Part | Role |
|---|---|
| `index.md`, `lesson-1.md` to `lesson-6.md`, `monthly.md` | Generated pages, each with Jekyll front matter. |
| `_layouts/default.html` | Generated layout, inline styles, no script. Canonical points to cartman.systems/hygiene. |
| `_config.yml` | Generated. Title, description and the `exclude:` list. |
| `README.md`, `CLAUDE.md` | The only hand-written files before the six-doc set; excluded from the site. |

## How data flows

Nothing flows at run time. The static site reads no data and sends none. A
reader who wants results reviewed follows a link to cartman.systems/hygiene,
a separate site and repo.

## External dependencies

| Dependency | Used for | If it goes away |
|---|---|---|
| GitHub Pages | hosting and the Jekyll build | static copy offline; interactive copy unaffected |
| `c-a-r-t-m-a-n` build script | the only writer of the generated files | edits would have to be made by hand and would read as drift |
| cartman.systems | the call to action link | the link breaks |

## Decisions

No ADRs live here. The decisions are in Cartman's planning notes and decision
log (2026-10-23): free supporting asset, two copies from one source. The
interactive endpoint's design is ADR-0009 in `c-a-r-t-m-a-n/docs/adr/`.
See also [MISSION.md](MISSION.md).
