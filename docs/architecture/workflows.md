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
| `ollama-review.yml` | Runs local Ollama-based automatic PR review |
| `release.yml` | Runs `semantic-release` and publishes tag/release |

---

## ?? Repo-Local Workflows

- `app-ui`
  - `ui-pr-checks.yml` for lint, Ollama review, and build on PRs
  - `release.yml` for lint, reusable release, then Vercel deploy
- `app-api`
  - `lint.yml` for PR lint checks and Ollama review on PRs
  - `release.yml` for lint, Fly deploy, then reusable release

---

## ?? Ollama Review Trigger Coverage

Configured events:
- `pull_request` on `opened`, `reopened`, `ready_for_review`, and `synchronize`

Review policy emphasis:
- correctness and regressions
- API and data contract drift
- auth, permission, and security issues
- performance and accessibility risks
- missing or weak tests

Execution model:
- GitHub-hosted `ubuntu-latest` runners
- Ollama installed at workflow runtime
- Local model pulled onto the runner and used without external LLM API calls

---

## ??? Guardrails

- Do not duplicate shared workflow logic in app repos unless intentionally diverging.
- Update this `.github` repo reusable workflow first when global policy changes.
- Keep docs and workflow behavior in sync in the same PR.
- Keep the selected Ollama model small enough for GitHub-hosted runners unless you move to self-hosted GPU runners.

---

## ?? Branch Protection Recommendation

For protected branches such as `main`, require the Ollama review status check before merge.

Recommended required check:
- `Ollama Review`

Recommended baseline required checks by repository:
- `app-ui`: `PR Title Check`, `UI PR Checks / Lint`, `Ollama Review`, `UI PR Checks / Build`
- `app-api`: `PR Title Check`, `Lint Check`, `Ollama Review`
- `.github`: `PR Title Check`

After the first workflow run in each repository, verify the exact check labels in GitHub and use those exact labels in branch protection or rulesets.
