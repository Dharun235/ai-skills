# clean-code

Package for applying clean-code principles during writing, review, and refactoring.

## Install

```bash
npm install clean-code-skill
```

If installing locally from this repo:

```bash
cd clean-code
npm pack
npm install ./clean-code-skill-1.0.0.tgz
```

## Use

Use this package when reviewing or refactoring code for readability, naming, duplication, structure, tests, or separation of concerns.

## Package layout

- `SKILL.md` - metadata and core guidance
- `references/` - principles and a review checklist

## Publish

1. Update the version in `package.json`.
2. Run `npm pack`.
3. Publish with `npm publish`.

## Thanks

Based on DevCom clean-code guidance and the Nevo skill packaging guide.
