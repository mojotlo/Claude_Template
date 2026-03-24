# Commit, Push, and Open PR

Create a git commit, push the branch, and open a pull request.

## Steps

1. Run `git status` and `git diff --staged` to see what's changed
2. Write a concise, descriptive commit message summarizing the change
3. Run `git add -A` then `git commit -m "<message>"`
4. Run `git push -u origin HEAD`
5. Create a PR using `gh pr create` with:
   - A clear title matching the commit message
   - A body that describes: what changed, why, and how to test it
   - Link any related issues if mentioned in context

## Commit message format

```
<type>: <short description>

Types: feat, fix, refactor, test, docs, chore
```

## PR body template

```
## What
<what changed>

## Why
<why this change was needed>

## How to test
<steps to verify the change works>
```
