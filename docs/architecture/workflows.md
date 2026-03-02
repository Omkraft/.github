# 🔧 Workflows and Reusable Actions

## Reusable Workflow Pattern

Consumer repositories call shared workflows from this repository:

```yaml
uses: Omkraft/.github/.github/workflows/<workflow>.yml@main
```

---

## Shared Reusable Workflows

| Workflow | Purpose |
| --- | --- |
| `pr-title.yml` | Enforces Conventional Commit-style PR titles |
| `release.yml` | Runs `semantic-release` and publishes tag/release |

---

## Repo-Local Workflows (Current)

- `app-ui`
  - `ui-pr-checks.yml` for lint + build on PRs
  - `release.yml` for lint, reusable release, then Vercel deploy
- `app-api`
  - `lint.yml` for PR lint checks
  - `release.yml` for lint, Fly deploy, then reusable release

---

## Guardrails

- Do not duplicate shared workflow logic in app repos unless intentionally diverging.
- Update this `.github` repo reusable workflow first when global policy changes.
- Keep docs and workflow behavior in sync in the same PR.
