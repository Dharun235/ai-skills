# Example Skill Layout

```text
skill-name/
  SKILL.md
  references/
    frontmatter.md
    structure.md
    testing.md
    examples.md
  scripts/
  assets/
```

## Example Frontmatter

```yaml
---
name: deployment-checklist
description: >
  Pre-deployment validation checklist for production releases.
  Use when the user asks to deploy, release, ship, or run the checklist.
---
```

## Example Body Pattern

```md
# Deployment Checklist

1. Verify prerequisites.
2. Apply the change.
3. Run validation.
4. Confirm the result.
```

## Example Package Rule

Keep the core workflow in `SKILL.md` and move the rest into references.
