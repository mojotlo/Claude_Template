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

After implementing, verify your work:
- Run the test suite
- Run the linter: `npm run lint`
- Run the type checker: `npm run typecheck`
- If a dev server is available, test the affected behavior manually

Claude should never consider a task done until verification passes.

---

## Style

- Small, focused commits
- One logical change per session where possible
- Do not refactor unrelated code while implementing a feature
- Prefer obvious code over clever code
