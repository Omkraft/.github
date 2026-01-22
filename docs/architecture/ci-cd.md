# CI/CD Architecture (Omkraft)

## Overview

Omkraft uses **organization-level reusable GitHub Actions workflows** to enforce consistency across all repositories.

### Goals
- Enforce standards automatically
- Prevent accidental bypasses
- Centralize governance
- Minimize per-repo configuration

---

## High-Level Flow

1. Developer opens a PR
2. Required checks run automatically:
   - Lint
   - PR Title (Conventional Commits)
3. PR is merged into `main`
4. Release workflow runs automatically
5. Version, tag, and release notes are generated

---

## Centralized Workflows

All reusable workflows live in:

```yaml
Omkraft/.github/.github/workflows/
```

Repositories **call** these workflows instead of redefining logic.

---

## Enforced Checks
| Check | Purpose |
|----|----|
| Lint | Code quality |
| PR Title | Semantic versioning |
| Release | Automated tagging & changelog |

These checks are enforced using **Require Workflows** (not legacy status checks).

---

## Non-Goals
- **No** manual releases
- **No** per-repo release logic
- **No** bypassing CI via UI

---

## Architecture Diagrams

- [CI/CD Flow](ci-cd-diagram.md)
- [Reusable Workflows](workflows-diagram.md)
- [Release Pipeline](release-pipeline.md)
- [Secrets & Permissions](secrets-flow.md)
- [Governance Model](governance-diagram.md)