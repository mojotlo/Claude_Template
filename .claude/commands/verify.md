# Verify

Run full verification of the current state of the app. Always run this before committing.

## Steps

1. **Types** — run `npm run typecheck`. Fix any errors before continuing.
2. **Lint** — run `npm run lint`. Fix any errors before continuing.
3. **Tests** — run `npm test`, then read `test-results/summary.txt`:
   - All tests must pass
   - Coverage must be at 100% across lines, functions, branches, statements
   - If gaps exist, write tests to fill them before continuing
   - If tests fail, read `test-results/results.json` for full stack traces, fix, re-run
4. **Dev server** — run `npm run dev` in the background, then use Playwright to:
   - Open the app in a browser
   - Navigate to key pages/routes
   - Check for console errors
   - Verify the core user flow works end to end
5. **Report** — read `test-results/summary.txt` and include its output in your summary

## Rules

- Do not consider verification passed if `test-results/summary.txt` shows ❌ FAILED
- Do not consider verification passed if coverage is below 100%
- Never skip or comment out failing tests — fix them
- If the browser shows errors, investigate and fix before reporting done
