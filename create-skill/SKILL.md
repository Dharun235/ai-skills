---
name: create-skill
description: >
  Write a clear, concise AI agent skill package.
  Use when the user wants to create or package a skill for an AI agent, including
  frontmatter, trigger wording, body structure, references, examples, or testing guidance.
---

# Create Skill

Write a skill package that is concise, correctly triggered, and easy to distribute.

## Core Rules

1. Encode knowledge the model does not already have.
2. Keep the skill focused on one task.
3. Put trigger information in frontmatter.
4. Use imperative, actionable instructions.
5. Keep the main file short and move detail into references.

## Body Shape

Use a rigid body when skipping a step could break the workflow. Use a flexible body when the task needs judgment.

## Skill Layout

Every skill should use this shape:

```text
my-skill/
  SKILL.md
  references/
  scripts/
  assets/
```

- Use `SKILL.md` for metadata and the core workflow.
- Use `references/` for details, examples, and edge cases.
- Use `scripts/` for deterministic automation.
- Use `assets/` for templates and output resources.

## Writing Process

1. Define the task the skill should own.
2. Write a narrow frontmatter description with exact triggers.
3. Write the body as a short workflow or decision framework.
4. Move long explanations into references.
5. Test expected and unexpected triggers.
6. Tighten the wording until it triggers correctly.

## When To Use This Skill

- The user asks to write a new AI agent skill.
- The user wants to package skill content for reuse.
- The user asks for a `SKILL.md` structure, frontmatter, references, or testing guidance.

## On-Demand References

- Read [references/frontmatter.md](references/frontmatter.md) for the exact name and description rules.
- Read [references/structure.md](references/structure.md) for rigid vs flexible skill bodies and progressive disclosure.
- Read [references/testing.md](references/testing.md) for trigger testing and execution testing.
- Read [references/examples.md](references/examples.md) for a complete sample skill layout.
