# Repository Guidelines

## Project Structure & Module Organization
`README.md` is the source of truth for Engauge Learning's palette, typography, and icon tokens distilled from the Brand Guidelines PDF; consult it before adding UI surfaces. `header.html` houses the in-progress header markup and styles (logo block, CTA buttons, spacing rules) and doubles as the layout playground. Place supporting artifacts such as SVG exports or mockups under an `assets/` folder and reference them with relative links so static previews keep working.

## Build, Test, and Development Commands
The codebase is static, so a lightweight server is enough for feedback. Run `python3 -m http.server 4173` from the repo root to preview `header.html`, or use `npx serve .` when you need automatic MIME handling or HTTPS checks. Before committing, format-check files with `npx prettier --check header.html README.md` (run with `--write` to auto-fix spacing).

## Coding Style & Naming Conventions
Use four-space indentation across HTML/CSS, double quotes for attributes, and group CSS declarations logically: layout, box model, typography, then color/effects. Keep class names lowercase kebab-case (`.btn-primary`, `.search-container`), keep hex colors uppercase, and only introduce new tokens after documenting them in `README.md`.

## Testing Guidelines
There is no automated suite, so rely on fast manual passes. Run `npx htmlhint header.html` for structural linting, then inspect the header at 360px, 768px, and 1440px widths across current Chrome and Safari builds.

## Commit & Pull Request Guidelines
Follow the historical commit pattern `<scope>: <action>` (example: `update: add hero gradient`). Each PR should summarize the goal, include before/after screenshots or GIFs, list manual test coverage (browser + viewport), and link to any tracked issue. Rebase onto `main`, rerun the commands above, and request reviews from both a brand owner and a front-end maintainer.

## GitOps Workflow (Mandatory)
`gitops.md` defines the required close-out steps: run `bunx tsc --noEmit`, stage files explicitly with `git add <file>`, commit using the required `type: six-word summary` format, and push to the active branch. Treat that checklist as non-optional after every task so the branch stays type-safe and synchronized with remote.

## Branding & Asset Notes
Stick to the core colors (Cobalt `#0047AB`, Charcoal `#1D1D1D`, Pearl Grey `#EDEDED`) unless README guidance expands the palette. Reserve Glancyra for hero marks, use Poppins/Raleway/system sans for supporting copy, and when swapping logos preserve the `<img>` dimensions and document the source file path for designers.
