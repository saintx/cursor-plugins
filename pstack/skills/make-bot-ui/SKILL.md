---
name: Make Bot UI
description: >-
  Use when building a custom UI (page, dashboard, buttons) that should wake a
  Grok Bot over a webhook, when the user must provide a webhook sender key, or
  when exposing that UI on Tailscale.
disable-model-invocation: true
---

# How to make a bot UI

## Index

`surf --list references/index.md` lists this skill's intents. `surf references/index.md "<Heading>#<Subheading>#<Intent>"` returns the command for one: a path of parent headings joined by `#` reaches any heading, and a bare heading name returns its first match. Paths are relative to this skill's base directory. See `surf --help` for other options.
