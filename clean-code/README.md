# Clean Code Skill Package

A package for applying clean-code principles during code writing, review, and refactoring.

## What's in it

| File                       | What it covers                                                                            |
| -------------------------- | ----------------------------------------------------------------------------------------- |
| `SKILL.md`                 | Skill metadata, trigger guidance, operating rules, and when to load references            |
| `references/principles.md` | Core clean-code principles like KISS, YAGNI, DRY, SRP, naming, and separation of concerns |
| `references/checklist.md`  | Quick review and refactor checklist                                                       |

## Installation

Install the package from npm:

```bash
npm install clean-code-skill
```

If you are installing from this repository locally, pack it first and install the tarball:

```bash
cd clean-code
npm pack
npm install ./clean-code-skill-1.0.0.tgz
```

## Verify

Confirm the package is installed and the files are present in `node_modules/clean-code-skill`.

## Usage

Use this skill when the task is about readability, maintainability, refactoring, naming, duplication, comments, boundaries, or code review feedback.

## Thanks

Thanks to the DevCom article on clean-code principles and the Nevo guide on writing AI agent skills for the source material and packaging guidance.
