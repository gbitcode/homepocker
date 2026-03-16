# Project Guidance

## Scope

This repository is a small static web app. Prefer minimal changes that preserve the current no-build setup.

## Structure

- `README.md`: product overview and user-facing setup notes
- `index.html`: full app shell and modal markup
- `game.js`: all game state, rendering, and event handling
- `styles.css`: layout and visual styling
- `manifest.json`: app metadata
- `assets/`: icons only

## Working Rules

- Start reviews from `README.md`, then confirm behavior in `index.html` and `game.js`.
- Avoid introducing frameworks, bundlers, or package managers unless the user explicitly asks.
- Keep dependencies optional. This app currently runs as plain static files.
- If you change game rules, trace the full flow: blinds, action order, round completion, showdown, split pots, save/load.
- When editing markup, check that referenced IDs/classes still match the selectors in `game.js`.
- Keep deployment assumptions simple; this app is a static site without service-worker caching.

## Validation

- There is no automated test suite yet.
- For behavior changes, validate by running the app in a browser and walking at least one hand through pre-flop to showdown.
- For persistence changes, verify save, reload, load-from-list, and clear-data flows.

## Codex Infra

- Use this `AGENTS.md` as the primary repo-specific instruction source.
- Do not add project-local skills unless a repeated maintenance workflow emerges; for this repo, that would be unnecessary overhead.
