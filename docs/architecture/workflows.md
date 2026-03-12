# ?? Workflows and Reusable Actions

## ?? Reusable Workflow Pattern

Consumer repositories call shared workflows from this repository:

```yaml
uses: Omkraft/.github/.github/workflows/<workflow>.yml@main
```

---

## ?? Shared Reusable Workflows

| Workflow | Purpose |
| --- | --- |
| `pr-title.yml` | Enforces Conventional Commit-style PR titles |
| `pr-agent-review.yml` | Runs Qodo PR-Agent for automatic PR review |
| `release.yml` | Runs `semantic-release` and publishes tag/release |

---

## ?? Repo-Local Workflows

- `app-ui`
  - `ui-pr-checks.yml` for lint, PR-Agent review, and build on PRs
  - `release.yml` for lint, reusable release, then Vercel deploy
- `app-api`
  - `lint.yml` for PR lint checks and PR-Agent review on PRs
  - `release.yml` for lint, Fly deploy, then reusable release

---

## ?? PR-Agent Trigger Coverage

Configured events:
- `pull_request` on `opened`, `reopened`, `ready_for_review`, and `synchronize`

Review policy emphasis:
- correctness and regressions
- API and data contract drift
- auth, permission, and security issues
- performance and accessibility risks
- missing or weak tests

Configuration source:
- Repository root `.pr_agent.toml` in each participating repository
- Local repo configuration can evolve independently later without editing the shared workflow

---

## ??? Guardrails

- Do not duplicate shared workflow logic in app repos unless intentionally diverging.
- Update this `.github` repo reusable workflow first when global policy changes.
- Keep docs and workflow behavior in sync in the same PR.
- Store the LLM credential as an organization Actions secret named `OPENAI_KEY` and grant it to all participating repositories.

---

## ?? Branch Protection Recommendation

For protected branches such as `main`, require the PR-Agent status check before merge.

Recommended required check:
- `PR Agent Review`

Recommended baseline required checks by repository:
- `app-ui`: `PR Title Check`, `UI PR Checks / Lint`, `UI PR Checks / Build`, `PR Agent Review`
- `app-api`: `PR Title Check`, `Lint Check`, `PR Agent Review`
- `.github`: `PR Title Check`

After the first workflow run in each repository, verify the exact check labels in GitHub and use those exact labels in branch protection or rulesets.
