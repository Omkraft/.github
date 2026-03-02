# 🚀 Developer Onboarding

## What You Need to Know

- PR title must follow Conventional Commit format.
- Required CI checks must pass before merge.
- Releases are automated from `main`; no manual version publishing.
- Shared release and PR-title logic is maintained in `Omkraft/.github`.

---

## PR Checklist

- `PR Title Check` passes.
- Repo-specific lint/build checks pass.
- No direct push to protected `main`.

---

## Current Workflow Model

- `app-ui`
  - PR checks: local `UI PR Checks` + reusable `PR Title Check`
  - Main push: lint -> reusable release -> deploy to Vercel
- `app-api`
  - PR checks: local `Lint Check` + reusable `PR Title Check`
  - Main push: lint -> deploy (Fly) -> reusable release

---

## If a Pipeline Fails

1. Open the workflow run in Actions.
2. Check the failing step logs.
3. Fix code, config, or commit/PR title.
4. Push the fix and re-run as needed.
