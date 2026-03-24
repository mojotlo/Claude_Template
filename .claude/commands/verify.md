# Verify

Run full verification of the current state of the app. Always run this before committing.

## Steps

1. **Types** — run `npm run typecheck`. Fix any errors before continuing.
2. **Lint** — run `npm run lint`. Fix any errors before continuing.
3. **Tests** — run `npm test`. All tests must pass.
4. **Dev server** — run `npm run dev` in the background, then use Playwright to:
   - Open the app in a browser
   - Navigate to key pages/routes
   - Check for console errors
   - Verify the core user flow works end to end
5. **Report** — summarize what passed, what failed, and what was fixed.

## Rules

- Do not consider verification passed if any step has errors
- If tests fail, fix them before reporting done
- If the browser shows errors, investigate and fix before reporting done
