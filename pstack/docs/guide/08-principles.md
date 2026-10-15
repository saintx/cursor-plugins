# Steer with principle names

pstack ships 24 principles as sections of the principles skill. `/poteto-mode` reads their index at the start of every multi-step task, applies the ones the task triggers, and names each applied principle in its reply along with the decision it changed.

You don't invoke principles. You use their names to steer. Each name points at a complete rule the agent has already read, so one phrase redirects the work more precisely than a paragraph of instructions.

## Steering in practice

Say the agent is about to bolt a new adapter onto three existing ones:

```text
use subtract before you add. delete the obsolete adapters first, then design what's left.
```

Say it claims success because the build passed:

```text
apply prove it works. run the real import flow and show me the written records.
```

Say two parallel attempts are about to write to the same branch:

```text
separate before serializing shared state. give each attempt its own worktree, no locks.
```

Each phrase lands because the rule behind it is specific. The agent still has to say, in its reply, which decision the rule changed. A principle citation with no decision behind it is the tell that it name-dropped instead of applying.

## The 24, briefly

The core principles decide how much to build and when to rethink the design:

- [Laziness Protocol](../../skills/principles/references/principles.md#laziness-protocol) prefers deletion and the smallest change that solves the problem.
- [Foundational Thinking](../../skills/principles/references/principles.md#foundational-thinking) chooses the core data structures before writing logic.
- [Redesign from First Principles](../../skills/principles/references/principles.md#redesign-from-first-principles) integrates a new requirement as if it had been there from day one.
- [Attack the Premise](../../skills/principles/references/principles.md#attack-the-premise) questions the premise that two or more failed fixes shared, after a census of which actors hold the imbalance.
- [Subtract Before You Add](../../skills/principles/references/principles.md#subtract-before-you-add) removes dead weight before building on top of it.
- [Minimize Reader Load](../../skills/principles/references/principles.md#minimize-reader-load) collapses layers and hidden state a reader must hold in their head.
- [Outcome-Oriented Execution](../../skills/principles/references/principles.md#outcome-oriented-execution) converges rewrites on the target design instead of preserving throwaway compatibility states.
- [Experience First](../../skills/principles/references/principles.md#experience-first) chooses the user's result over implementation convenience.
- [Exhaust the Design Space](../../skills/principles/references/principles.md#exhaust-the-design-space) builds two or three competing prototypes when there's no precedent.
- [Build the Lever](../../skills/principles/references/principles.md#build-the-lever) builds the script that does or proves the work, so a reviewer can rerun it. When an agent keeps doing the same thing by hand, have it write the tool or skill it wishes it had. If a script can do a step the same way every time, use the script, and save agents for the judgment calls.

The architecture principles decide where state, validation, and compatibility live:

- [Model the Domain](../../skills/principles/references/principles.md#model-the-domain) encodes repeated rules in one structure, not scattered conditionals.
- [Boundary Discipline](../../skills/principles/references/principles.md#boundary-discipline) validates at the boundary and trusts internal types.
- [Type System Discipline](../../skills/principles/references/principles.md#type-system-discipline) makes illegal states unrepresentable.
- [Make Operations Idempotent](../../skills/principles/references/principles.md#make-operations-idempotent) converges retries on the same end state.
- [Migrate Callers Then Delete Legacy APIs](../../skills/principles/references/principles.md#migrate-callers-then-delete-legacy-apis) migrates and deletes in one wave.
- [Separate Before Serializing Shared State](../../skills/principles/references/principles.md#separate-before-serializing-shared-state) removes the sharing before adding coordination.

The verification principles define what counts as proof:

- [Prove It Works](../../skills/principles/references/principles.md#prove-it-works) verifies the real artifact, not a proxy.
- [Fix Root Causes](../../skills/principles/references/principles.md#fix-root-causes) reproduces and traces to the cause before changing code.
- [Sequence Work into Verifiable Units](../../skills/principles/references/principles.md#sequence-work-into-verifiable-units) ends each small unit in a check before starting the next.
- [Test Behavior, Not Implementation](../../skills/principles/references/principles.md#test-behavior-not-implementation) calls the code the way its users do and asserts a literal expected value, and deletes a test that would still pass if every imported function returned `undefined`.
- [Explain the Number](../../skills/principles/references/principles.md#explain-the-number) names what limits a measured number and rules out that it measured something else, before anyone trusts or reports it. [`/benchmark-checklist`](../../skills/benchmark-checklist/SKILL.md) turns it into seven questions you answer from real runs.

The delegation principles keep parallel work sane:

- [Guard the Context Window](../../skills/principles/references/principles.md#guard-the-context-window) routes bulk reading to subagents and keeps findings in the main chat.
- [Never Block on the Human](../../skills/principles/references/principles.md#never-block-on-the-human) proceeds on reversible work and presents the result.

And one meta principle:

- [Encode Lessons in Structure](../../skills/principles/references/principles.md#encode-lessons-in-structure) turns advice you've repeated twice into a lint, check, or script. [`/correct`](../../skills/correct/SKILL.md) applies it to a whole repo, as shown in [Make it yours](./09-make-it-yours.md#fix-the-environment-with-correct).

Don't memorize the list. Skim it now, then come back when you catch the agent doing something a name here would have prevented. That's how the vocabulary sticks.

Next: [Make it yours](./09-make-it-yours.md).
