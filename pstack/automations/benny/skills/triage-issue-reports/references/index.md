---
audience: engineering
---

# Triage issue reports intents

## Deciding whether triage-issue-reports fits the task

### Find out what the triage automation produces

surf references/about.md "Overview"

### Decide whether this run is the Benny triage automation

surf references/about.md "When to use"

## Protecting the source thread

### Classify one report and stop when the config is missing

surf references/procedure.md "Post one verdict and do not fix the bug"

### Keep Slack writes and guessed tickets off this run

surf references/procedure.md "Hard safety rules"

### Freeze source coordinates before any tracker write or verdict

surf references/procedure.md "1. Freeze source coordinates"

## Classifying the report

### Read the report and its attachments before deciding

surf references/procedure.md "2. Read the whole report"

### Trace cause before choosing an owner or a destination

surf references/procedure.md "3. Trace cause before routing"

### Choose bug, performance, feature request, question, or reroute

surf references/procedure.md "4. Classify"

### Apply a configured route and leave owner pings off by default

surf references/procedure.md "5. Apply configured routing"

### Copy the routing-map shape and keep private ids out of the example

surf references/routing.example.md "Routing map example"

## Deciding whether to file a ticket

### Use the tracker adapter and fail closed when a write is unavailable

surf references/procedure.md "6. Use the issue-tracker adapter"

### Dedupe against the source permalink and the symptom

surf references/procedure.md "7. Dedupe"

### Create a ticket only for a clear live bug

surf references/procedure.md "8. Decide whether to create"

## Posting the one verdict

### Post one thread reply that ends with exactly one marker

surf references/procedure.md "9. Post one verdict"

### Watch one follow-up window and do not emit a second marker

surf references/procedure.md "10. Watch one follow-up window"
