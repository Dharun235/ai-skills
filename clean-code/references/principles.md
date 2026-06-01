# Clean Code Principles

Use these principles when improving code quality.

## KISS

Choose the simplest solution that still meets the requirement. Avoid extra branches, indirection, or framework machinery unless it clearly removes real complexity.

## YAGNI

Do not implement future features, extension points, or configuration until there is a current need.

## Single Responsibility

Give each function, class, and module one main reason to change. If a unit validates, transforms, persists, and notifies, split it.

## DRY

Extract repeated business rules into one place. Do not force unrelated code into shared abstractions just because it looks similar.

## Intent-Revealing Names

Use names that describe purpose and behavior. Avoid abbreviations and vague names like `data`, `calc`, or `helper` when a specific name is possible.

## Named Constants

Replace important literal values with named constants when the value represents policy, thresholds, limits, durations, or business meaning.

## Comments

Use comments to explain why something exists, what constraint it satisfies, or why a non-obvious choice was made. Remove comments that only repeat the code.

## Levels of Detail

Top-level code should read like a business flow. Lower-level helpers should contain the implementation detail.

## Refactor Continuously

Do not wait for a rewrite to improve structure. Make small, safe refactors while the code is already open.

## Tests

Use tests to lock in behavior before and after structural changes. Hard-to-test code usually has too many responsibilities or dependencies.

## Separate Rules From Mechanism

Keep business decisions separate from storage, transport, UI, and framework code so rules are easier to change and verify.

## Version Control

Prefer small, reviewable changes. Small commits and focused diffs make refactoring safer and easier to trace.
