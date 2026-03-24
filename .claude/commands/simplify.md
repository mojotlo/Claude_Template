# Simplify

After a feature is complete and tests pass, simplify the code without changing behavior.

## Steps

1. Run `npm test` first to confirm tests pass — do not simplify broken code
2. Look for:
   - Functions doing more than one thing — split them
   - Duplicated logic — extract to a shared helper
   - Overly complex conditionals — flatten or simplify
   - Dead code or unused variables — remove them
   - Files approaching 300 lines — consider splitting
3. After each change, run `npm test` again to confirm nothing broke
4. Do not change public interfaces or behavior — only internal implementation

## Rules

- Behavior must be identical before and after
- All tests must pass after simplification
- Do not simplify code in unrelated files
