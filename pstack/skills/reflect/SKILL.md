---
name: reflect
description: Spawn three parallel review subagents over the active transcript, surface learnings, and route each to a concrete edit on an existing skill. Use when the user says reflect.
disable-model-invocation: true
---

# Reflect

## Index

`surf --list references/index.md` lists this skill's intents. `surf references/index.md "<Heading>#<Subheading>#<Intent>"` returns the command for one: a path of parent headings joined by `#` reaches any heading, and a bare heading name returns its first match. Paths are relative to this skill's base directory. See `surf --help` for other options.
