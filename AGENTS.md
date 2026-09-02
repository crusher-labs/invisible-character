# AGENTS.md - Invisible Character

Single-purpose static tool: One-click copy of invisible Unicode characters (Hangul filler, zero-width space, braille blank and more) for blank usernames, empty messages and invisible text, with a generator and a paste-to-test checker. Part of the crusher-labs **static tools line**. Hosted on GitHub Pages at https://crusher-labs.github.io/invisible-character/

Workspace rules: `x:\crusher-labs\AGENTS.md`. Global rules: `~/.claude/CLAUDE.md`.

## What it is

- One `index.html`, no build step, no backend, fully client-side.
- Consumes `crusher-ui-kit` via the jsDelivr CDN (the workspace static contract).

## Static contract (must hold)

- `<html>` carries `data-default-theme="minimal" data-theme-lock="minimal" data-default-mode="dark" data-default-brand="#0ea5e9"`; `<body class="crusher-tool-page">`; one fixed `<crusher-style-switcher>`. No Tailwind CDN, no Font Awesome.
- The five kit CDN pins carry sha384 SRI hashes. Never bump the version by hand; `tools-hub/scripts/bump-kit.mjs` rewrites version + hashes fleet-wide.
- Validated by `tools-hub/scripts/check-static.mjs` (run `npm run check:static` from `repos/tools-hub`).

## What NOT to do

- Don't commit to `main` directly (`dev` -> manual QA -> fast-forward `main`). No `Co-Authored-By` / AI-attribution trailers.
- Don't edit `crusher-ui-kit`; request changes by appending to `x:/itxcrusher/INBOX.md`.
- Don't add Tailwind CDN / Font Awesome; use framework primitives + inline SVGs.
