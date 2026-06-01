# Frontmatter

The frontmatter is the skill's identity card.

## Name

- Use a unique, lowercase, hyphenated name.
- Keep it descriptive and compact.
- Make it stable enough to use in logs, config, and package names.

## Description

The description is the most important trigger text in the file.

Include three things:

1. What the skill does.
2. When the agent should use it.
3. What the user might say to activate it.

## Good Description Pattern

```yaml
description: >
  Short summary of the capability.
  Use when the user asks for the task, mentions the workflow,
  or uses trigger phrases like "...".
```

## Bad Description Pattern

```yaml
description: Helps with agent tasks.
```

That is too vague to trigger reliably.
