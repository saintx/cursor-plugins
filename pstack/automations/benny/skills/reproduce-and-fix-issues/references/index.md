---
audience: engineering
---

# Reproduce and fix issues intents

## Deciding whether reproduce-and-fix-issues fits the task

### Find out what the repro automation produces

surf references/about.md "Overview"

### Decide whether this run is the Benny repro automation

surf references/about.md "When to use"

## Protecting the source thread

### Wait for a trusted triage marker and fail closed without config

surf references/procedure.md "Wait for triage and fail closed"

### Keep Slack writes on the coordinator

surf references/procedure.md "Hard safety rules"

### Freeze the source channel and thread before any work

surf references/procedure.md "1. Freeze source coordinates"

### Post status in an operations thread instead of a source root

surf references/procedure.md "4. Open an optional operations thread"

## Gating the run on triage and ownership

### Accept only a trusted bug or performance marker

surf references/procedure.md "2. Wait for the triage contract"

### Stop when a person owns the fix or a fix artifact already exists

surf references/procedure.md "3. Apply ownership and fix-artifact gates"

## Reproducing the symptom through the real UI

### Load the adapter and stop when a required capability is missing

surf references/procedure.md "5. Load and check the control adapter"

### Set the control skill name and feature map and fail closed when they are absent, ambiguous, or incomplete

surf references/control-adapter.md "Control-adapter contract"

### Require the seven control-adapter capabilities

surf references/control-adapter.md "Required capabilities"

### Hold the adapter to one environment across both builds

surf references/control-adapter.md "Adapter behavior"

### Translate a missing environment before calling the run blocked

surf references/control-adapter.md "Environment translation"

### Run the harmless adapter check before enabling repro

surf references/control-adapter.md "Setup check"

### Study the report and separate competing causes

surf references/procedure.md "6. Study the report"

### Reproduce the discriminating symptom twice through real UI actions

surf references/procedure.md "7. Reproduce"

### Capture evidence that shows the broken final state

surf references/procedure.md "8. Capture and review evidence"

### Report a confirmed repro and stay silent otherwise

surf references/procedure.md "9. Report the repro outcome"

### Match the report to the fields a feature-map section has to name

surf references/feature-map.example.md "Per-feature template"

### See a filled feature map for a fictional app

surf references/feature-map.example.md "Fictional example"

### Check a feature map against the completeness list

surf references/feature-map.example.md "Completeness checklist"

## Verifying a fix that already exists

### Switch to verify mode instead of authoring over an existing fix

surf references/procedure.md "10. Verify an existing fix"

### Require a pull request or commit before measuring a fix

surf references/verify-existing-fix.md "Qualify the artifact"

### Measure both revisions from a checkout that keeps user changes

surf references/verify-existing-fix.md "Protect the working tree"

### Show the symptom twice on the baseline before trusting the fix

surf references/verify-existing-fix.md "Measure the baseline"

### Show the broken state gone on the patched build

surf references/verify-existing-fix.md "Measure the patched build"

### Record a confirmed, insufficient, or inconclusive verification

surf references/verify-existing-fix.md "Outcomes"

### Clean up both builds without discarding user work

surf references/verify-existing-fix.md "Cleanup"

## Attempting a bounded fix

### Pass every bounded-fix condition before editing

surf references/procedure.md "11. Qualify a bounded fix"

### Fix the root cause inside the configured budget

surf references/procedure.md "12. Root-cause and implement"

### Prove the broken state is gone on the patched UI

surf references/procedure.md "13. Prove the fix"

### Open a draft pull request only after before-and-after proof

surf references/procedure.md "14. Open a draft pull request"

### Answer one follow-up and always clean up the adapter

surf references/procedure.md "15. Follow-ups and cleanup"
