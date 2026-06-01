# Clean Code Checklist

Use this checklist for reviews and refactors.

## Clarity

- Can the code be understood without tracing multiple files?
- Is the main flow obvious at the top level?
- Are names specific and behavior-aligned?

## Structure

- Does each function or class have one main responsibility?
- Is business logic separated from IO, persistence, and framework code?
- Did you avoid premature abstraction and unnecessary layers?

## Duplication

- Is repeated business logic centralized?
- Did you avoid copying code that only looks similar but serves different rules?

## Values and Comments

- Are important literals replaced with named constants?
- Do comments explain rationale instead of obvious mechanics?
- Are stale comments removed?

## Change Safety

- Did behavior stay covered by tests?
- Did the refactor keep the smallest useful scope?
- Would the change be easy to review in isolation?

## Common Smells

- Mixed responsibilities
- Vague names
- Deep nesting
- Hidden side effects
- Over-engineering
- Business logic mixed with implementation details
