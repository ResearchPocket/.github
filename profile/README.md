<p align="center">
  <a href="https://researchpocket.github.io/">
    <img src="https://raw.githubusercontent.com/ResearchPocket/researchpocket.github.io/main/web/public/og.png" alt="ResearchPocket — Useful links, kept yours." width="100%">
  </a>
</p>

<p align="center"><strong>A human-first, local-first library for useful links.</strong></p>

<p align="center">
  <a href="https://researchpocket.github.io/">Explore ResearchPocket</a> ·
  <a href="https://researchpocket.github.io/app/">Open the owner app</a> ·
  <a href="https://github.com/ResearchPocket/researchpocket.github.io/releases/tag/v2.0.0-preview.4">Get the CLI</a> ·
  <a href="https://github.com/ResearchPocket/researchpocket.github.io/issues">Talk with us</a>
</p>

ResearchPocket helps you deliberately save, revisit, edit, and organize the
links that matter to you. It is not an autonomous memory feed for AI agents.
Your library stays readable, portable, and under your control.

> **V2 is available as an installable preview.** The current V2 preview is
> [`v2.0.0-preview.4`](https://github.com/ResearchPocket/researchpocket.github.io/releases/tag/v2.0.0-preview.4).

## What works today

- **Local CLI and TUI.** Save, search, edit, tag, favorite, delete, restore, and
  inspect links offline from a Rust command line or keyboard-first terminal
  interface.
- **A path out of V1.** Import an existing ResearchPocket SQLite library through
  a repeatable, read-only migration.
- **Fast browser capture.** Send the current Firefox page to the installed CLI
  and optionally enrich metadata directly or through the narrow Firecrawl API
  integration.
- **A private owner app.** Use the same domain rules in the browser through
  Rust/WASM, with an offline IndexedDB replica at
  [`researchpocket.github.io/app/`](https://researchpocket.github.io/app/).
- **Sync without a ResearchPocket server.** Exchange immutable updates through
  your private GitHub repository. Application-level CRDT semantics resolve
  concurrent edits; Git commits are transport and audit history, not the
  conflict-resolution model.

```text
CLI / TUI / browser capture        hosted owner app
           │                              │
      local SQLite                  local IndexedDB
           └──────── immutable CRDT updates ────────┐
                                                     ↕
                                      your private GitHub repository
```

Each device remains useful offline. Synchronization is periodic and explicit;
there is no always-on ResearchPocket backend and no required ResearchPocket
account.

## Start here

| I want to… | Go here |
| --- | --- |
| Understand the product | [ResearchPocket overview](https://researchpocket.github.io/) |
| Use my library in a browser | [Hosted owner app](https://researchpocket.github.io/app/) |
| Install the CLI or TUI | [Preview 4 release guide](https://github.com/ResearchPocket/researchpocket.github.io/blob/main/docs/releases/v2.0.0-preview.4.md) |
| Capture from Firefox | [Native capture and bookmarklet guide](https://github.com/ResearchPocket/researchpocket.github.io/blob/v2.0.0-preview.4/docs/v2/CLI.md#firefox-bookmarklet-capture) |
| Understand sync and privacy | [Sync protocol](https://github.com/ResearchPocket/researchpocket.github.io/blob/main/docs/v2/SYNC_PROTOCOL.md) · [Threat model](https://github.com/ResearchPocket/researchpocket.github.io/blob/main/docs/v2/THREAT_MODEL.md) |
| Follow or shape the work | [V2 roadmap](https://github.com/ResearchPocket/researchpocket.github.io/blob/main/docs/v2/ROADMAP.md) · [Delivery project](https://github.com/orgs/ResearchPocket/projects/2) |

## Repositories

| Repository | Status |
| --- | --- |
| [`researchpocket.github.io`](https://github.com/ResearchPocket/researchpocket.github.io) | Active V2 product, CLI/TUI, browser owner app, documentation, and releases |
| [`my-list`](https://github.com/ResearchPocket/my-list) | Legacy V1 GitHub Pages list; retained as a migration reference |
| [`ResearchGarden`](https://github.com/ResearchPocket/ResearchGarden) | Legacy research prototype; retained as a historical reference |

ResearchPocket is open source under Apache-2.0. Thoughtful bug reports, focused
feature proposals, and documentation fixes are welcome in the
[main issue tracker](https://github.com/ResearchPocket/researchpocket.github.io/issues).
