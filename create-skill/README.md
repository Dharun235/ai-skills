# create-skill

Package for writing AI agent skills.

## Install

```bash
npm install create-skill
```

If you are installing from this repository locally:

```bash
cd create-skill
npm pack
npm install ./create-skill-1.0.0.tgz
```

## Use

Use this package to write or package a skill with:

- clear frontmatter
- a short core workflow
- optional references for deeper detail
- trigger testing before release

## Package layout

- `SKILL.md` - metadata and core instructions
- `references/` - details, examples, and testing guidance

## Publish

1. Update the version in `package.json`.
2. Run `npm pack`.
3. Publish with `npm publish`.

## Thanks

Based on the Nevo guide on writing AI agent skills.
