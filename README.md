# Project Name

> Replace this with your project description.

---

## Setup

```bash
npm install
npm run dev
```

## Tests

```bash
npm test
npm run typecheck
npm run lint
```

---

## AI-Assisted Development

This repository is configured for Claude Code.

Context files live in `ai/`. Claude reads `CLAUDE.md` first, which
directs it through the rest. When you clone this template:

1. Update `CLAUDE.md` — fill in stack details and project-specific notes
2. Update `ai/repo-map.md` — map your actual modules
3. Update `ai/allowed-changes.md` — add any frozen areas
4. Delete placeholder comments marked with `[fill in]` or `[example]`

The `ai/` files are checked into git and treated as living documentation.
Update them whenever Claude does something wrong so it won't repeat the mistake.
