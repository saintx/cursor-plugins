# Surf me

pstack skills on `pstack-chips` (`dd4fe35`, parent `1e5c90a`) load a short pointer instead of the whole procedure. The procedure is still in the tree. `surf` reads the one section a task needs.

The byte counts are in [skill-context-sizes.json](skill-context-sizes.json). They measure each `SKILL.md`, which is the file an invocation loads. A token column in that file is `ceil(bytes / 4)`, for comparison only. The same numbers are drawn in [skill-context-before-after.html](skill-context-before-after.html).

## What changed

Every skill under `pstack/` now has the same shape. `SKILL.md` keeps its frontmatter and a heading, then a fixed Index paragraph. The old body is `references/procedure.md`. `references/about.md` says what the skill is for. `references/index.md` is a list of intents. Each intent is a `surf` command that returns one section.

The 24 `principle-*` skills are gone. Their text is one skill, `skills/principles`. `references/index.md` has 24 intents, one per principle. `references/principles.md` holds the bodies. Opening `principles` loads the 529-byte pointer. Opening one principle is a `surf` of that heading.

Across every skill entry point, the loaded text went from 57 files and 232,300 bytes to 34 files and 22,547 bytes. The 33 skills that kept their names went from 198,587 bytes to 22,018 bytes. The 24 principle files were 33,713 bytes. `poteto-mode` went from 20,429 bytes to 662. `bro` and `in-your-own-words` grew, because the shared pointer is longer than the file it replaced.

## Why this loads less

An agent that invokes a skill receives `SKILL.md`. The old files put the procedure in that file, so the whole procedure entered context whether the task needed the first step or the last.

`surf` prints one heading and stops at the next heading of the same or higher level. The index names the headings worth reading. The agent runs the command for the intent it has, and the rest of `procedure.md` stays on disk. A parent heading returns its children, so a step that needs the nearby detail can ask for the parent.

The principles fold uses the same rule. The old layout gave each principle its own skill file, and invoking one loaded that file in full. The new layout gives each principle a heading. One intent returns that heading. The other twenty-three stay unread.

## Install surf from the git repo

The command is `surf`. The repository is [github.com/saintx/surf-cli](https://github.com/saintx/surf-cli). Python 3.12 or newer, and [uv](https://docs.astral.sh/uv/).

From a clone:

```bash
git clone https://github.com/saintx/surf-cli.git
cd surf-cli
uv tool install .
surf --version
```

In one step, without a checkout:

```bash
uv tool install git+https://github.com/saintx/surf-cli.git
```

With Nix, from the same repository:

```bash
nix profile install github:saintx/surf-cli
```

Add `?ref=` and a tag or commit when you want a pin. The README also publishes a package install, `uv tool install surf-cli`, which tracks the release on PyPI rather than a git checkout.

`surf --help` lists the flags. `surf --list references/index.md`, run from a skill directory, prints that skill's intents. `surf references/procedure.md "Heading"` prints that section.
