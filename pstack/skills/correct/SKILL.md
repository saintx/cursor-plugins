---
name: correct
description: "Find the mistakes agents keep repeating in this repo and make each one impossible. Try architecture first, then types, then a lint whose error names the fix, then a test, and write docs last. Prove each check fails on a real past mistake. Repeat this each time the operator corrects you. Use for /correct."
disable-model-invocation: true
---

# Correct

## Index

`surf --list references/index.md` lists this skill's intents. `surf references/index.md "<Heading>#<Subheading>#<Intent>"` returns the command for one: a path of parent headings joined by `#` reaches any heading, and a bare heading name returns its first match. Paths are relative to this skill's base directory. See `surf --help` for other options.
