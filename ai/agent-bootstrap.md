# Agent Bootstrap

You are working in an AI-assisted TypeScript/Node.js repository.

Before touching any code, read the context files in CLAUDE.md in order.
This file defines your working process once you have that context.

---

## Task Workflow

When given a task, follow these steps exactly:

1. **Identify the relevant module** using `repo-map.md`
2. **Read related tests** before reading implementation code
3. **Plan the smallest change** that satisfies the task
4. **State your plan** before writing any code — confirm if uncertain
5. **Implement the change**
6. **Run tests** — all must pass
7. **Summarize** what changed and why

Do not skip steps. Do not jump straight to implementation.

---

## Planning

Use Plan mode (Shift+Tab twice in Claude Code) before implementing.

A good plan:
- names the specific files to be changed
- describes what will change in each file
- identifies which tests cover the affected behavior
- flags any risk or uncertainty

A good plan enables 1-shot implementation. Invest in it.

---

## Scope Discipline

Before starting, check `allowed-changes.md`.

If the task requires work outside allowed scope:
1. Stop
2. Explain what would be needed and why it's out of scope
3. Request clarification before proceeding

Do not interpret tasks broadly. Do not do unrequested work.

---

## Verification

After every meaningful code change — not just at end of session:

1. Run `npm test` — this runs tests AND writes `test-results/summary.txt`
2. Read `test-results/summary.txt` — understand exactly what passed, failed, or has coverage gaps
3. Fix any failures before moving to the next change
4. Run `npm run lint` and `npm run typecheck` before committing

If tests fail:
- Read the full error in `test-results/results.json` for stack traces
- Fix the code or the test — never skip or comment out failing tests
- Re-run until summary.txt shows ✅ PASSED

Claude should never consider a task done until `test-results/summary.txt` shows all passing and 100% coverage.

---

## Architecture Decisions

If a task involves introducing a new library, framework, tool, or architectural
pattern not already in the codebase:

1. **Stop before implementing** — check `ai/decisions/` for an existing ADR
2. **If no ADR exists** — create one before writing any code
3. **If an ADR exists but the decision has changed** — update it before implementing
4. **After implementing** — update the ADR index in `ai/decisions/README.md`

Do not introduce new dependencies or architectural patterns without a documented decision.
This is not optional — undocumented decisions are not allowed changes.

---

## Style

- Small, focused commits
- One logical change per session where possible
- Do not refactor unrelated code while implementing a feature
- Prefer obvious code over clever code
