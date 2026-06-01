# Testing

Test the skill before treating it as real.

## Trigger Testing

Ask prompts that should activate the skill and prompts that should not.

Should trigger:

- "Write a skill for API review"
- "Package this skill for reuse"
- "Create a skill for my agent"

Should not trigger:

- "Explain what skills are"
- "Write general documentation"
- "Help me with a random prompt"

## Execution Testing

Run the skill on a real task and check:

- Does it follow the intended structure?
- Does it stay concise?
- Does it add unnecessary steps?
- Does it use references only when needed?

## Iteration

- Tighten the description if it triggers too broadly.
- Add more concrete steps if the agent improvises.
- Move detail into references if the main file gets too large.
