---
name: clean-code
description: >
	Improve code readability, maintainability, and changeability using clean-code principles.
	Use when the user asks to review, refactor, simplify, or write code with clearer names,
	smaller functions, separated responsibilities, less duplication, fewer magic values,
	better comments, or better boundaries between business rules and implementation.
	Also use for clean-code reviews, code smell cleanup, and requests mentioning KISS, YAGNI,
	DRY, SRP, refactoring, maintainability, readability, or code structure.
---

# Clean Code

Apply clean-code principles to make code easier to read, change, and review.

## Operating Rules

1. Prefer the smallest change that improves clarity without changing behavior.
2. Keep the first pass local. Fix the nearest code that controls the problem before widening scope.
3. Prioritize correctness, then readability, then structure.
4. Do not over-abstract or split code unless a clear boundary, reuse case, or change driver exists.
5. Keep business rules separate from IO, framework code, storage, and transport details.
6. Preserve behavior with tests whenever the change affects logic, edge cases, or public behavior.

## What To Check

- Simple solution first: prefer the clearest working path.
- Single responsibility: one function, class, or module should do one main job.
- No unnecessary duplication: extract shared rules, not incidental similarity.
- Intent-revealing names: names should match what the code does.
- No magic values: name policy, thresholds, and business constants.
- Comments only for rationale: explain why, constraints, or unusual cases; do not narrate obvious code.
- Right level of detail: top-level code should show what happens; helpers should show how.
- Continuous refactoring: clean as you go instead of deferring structural fixes.

## When Reviewing

- Report findings first.
- For each finding, include the exact location, why it matters, and the smallest fix.
- Focus on code smells that hurt changeability: mixed responsibilities, vague names, duplication, deep nesting,
  hidden side effects, premature abstraction, and business logic mixed with implementation details.

## When Refactoring

1. Identify the main smell or boundary violation.
2. Make one focused structural improvement.
3. Keep public behavior stable.
4. Update or add tests for changed behavior.
5. Stop when the code is clear enough to read and modify without extra tracing.

## On-Demand References

- Read [references/principles.md](references/principles.md) for the core clean-code rules and how to apply them.
- Read [references/checklist.md](references/checklist.md) for a quick review and refactor checklist.
