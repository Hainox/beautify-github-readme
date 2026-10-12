# AGENTS.md

## Unwritten
- Gotchas: this repo is a fork of `oil-oil/beautify-github-readme`; the install command, Skill URL, and showcase links in the READMEs intentionally point upstream, so do not rewrite them to `Hainox`.
- Checks: there are no tests or CI; run `python3 skills/beautify-github-readme/scripts/audit_readme.py <README>` on each README you touch to catch broken image paths and unsafe SVG tags.
- Conventions: the READMEs stay in parity: `README.md` (English) and `README.ja.md` embed `assets/readme/en/`, `README.zh-CN.md` embeds the Chinese assets in `assets/readme/`, so a visual change ships in both asset sets. The installable package under `skills/beautify-github-readme/` is English-only.
- Off-limits: `assets/readme/hero.gif` and `assets/readme/en/hero.gif` are rendered from the matching `hero.svg` with the shared `assets/readme/hero-motion.json` via `skills/beautify-github-readme/scripts/render_motion_gif.py` (needs Pillow, `ffmpeg`, and `rsvg-convert` or macOS `sips`); edit the SVG and re-render, never the GIF.

## Pointers
- **Writing** or reviewing code: apply `CODING_STANDARDS.md`; project config and linters win where they disagree.
- **Security**-sensitive change (auth, permissions, untrusted input, secrets): read `docs/agents/security.md` first.
- **Committing** or opening a PR: follow `docs/agents/git.md`.
- **Risky** change (spans modules, migrates data, alters a public API): propose a phased plan and get approval before editing.
- **Done** means you ran the project's own check commands and they are green, or you named the ones you could not run.
