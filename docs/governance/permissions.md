# 🛡️ Permissions and Access

## Ownership Boundaries

| Area | Source of truth |
| --- | --- |
| Shared CI guardrails | `Omkraft/.github` reusable workflows |
| Product build/deploy logic | Each app repository |
| Release publishing | Reusable `release.yml` workflow |

---

## GitHub Actions Permissions

Reusable release job requests:
- `contents: write`
- `pull-requests: read`

PR title check workflow requests:
- `pull-requests: read`

---

## Access Guidance

- Limit write access to workflow files.
- Route policy changes through reviewed PRs.
- Keep token scopes least-privilege.
