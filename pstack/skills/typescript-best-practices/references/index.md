---
audience: engineering
---

# TypeScript best practices intents

## Deciding whether typescript-best-practices fits the task

### Find out which TypeScript rules this skill states

surf references/about.md "Overview"

### Decide whether a .ts or .tsx edit needs these rules

surf references/about.md "When to use"

## Applying a rule while editing

### Apply the rule summary before changing a TypeScript file

surf references/procedure.md "TypeScript best practices"

## Looking up the pattern for a rule

### Brand a primitive so two values of the same shape cannot mix

surf references/patterns.md "Branded types"

### Model variants with a discriminant so an illegal state cannot be built

surf references/patterns.md "Discriminated unions"

### Build a shape that cannot represent the illegal value

surf references/patterns.md "Constructive modeling"

### Keep a total array until a call site forces a stronger type

surf references/patterns.md "Simplest total type"

### Treat external data as unknown instead of any

surf references/patterns.md '`unknown` over `any`'

### Infer the type from the repository schema before writing a guard

surf references/patterns.md "Schemas before hand-rolled guards"

### Refuse an as cast until the value has been validated

surf references/patterns.md 'No `as` casts'

### Prefer a discriminant switch over a cast when narrowing

surf references/patterns.md "Narrowing hierarchy"

### Make a type guard prove the claim its name makes

surf references/patterns.md "Type guards"

### Make a new variant fail the build in the default arm

surf references/patterns.md "Exhaustiveness"

### Validate a value with satisfies instead of widening it with as

surf references/patterns.md '`satisfies` over `as`'

### Parse at the boundary into a named domain type

surf references/patterns.md "Boundary validation"

### Derive a type from an existing one before declaring a new interface

surf references/patterns.md "Schema-derived types"

### Pass an object when argument order would otherwise be the documentation

surf references/patterns.md "Object args"
