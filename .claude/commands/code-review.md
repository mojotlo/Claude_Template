# Code Review

Review the current changes for correctness, clarity, and consistency with project patterns.

## Steps

1. Run `git diff main` to see all changes
2. For each changed file, check:
   - Does it follow the architecture rules in `ai/ai-guide.md`?
   - Are there any TypeScript errors or `any` types?
   - Are there obvious bugs or edge cases not handled?
   - Is the naming clear and consistent with the codebase?
   - Are there any missing tests for new behavior?
3. Report findings grouped by severity:
   - **Must fix** — bugs, type errors, architecture violations
   - **Should fix** — missing tests, unclear naming, inconsistency
   - **Consider** — optional improvements

## Rules

- Be specific — reference file names and line numbers
- Do not suggest changes outside the scope of the current diff
- Do not rewrite working code just for style preference
