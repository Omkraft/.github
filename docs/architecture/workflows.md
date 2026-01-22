# Workflows & Reusable Actions

## Reusable Workflow Pattern

Repositories do NOT define logic directly.

Instead they call:

```yaml
uses: Omkraft/.github/.github/workflows/<workflow>.yml@main
```

---

## Available Workflows
| Workflow     | Purpose                |
| ------------ | ---------------------- |
| lint.yml     | Code linting           |
| pr-title.yml | Conventional PR titles |
| release.yml  | Automated release      |

---

## Why This Matters
- Centralized fixes
- No drift between repos
- Strong governance
- Easier audits

---

## Important Rules

- ❌ Do NOT copy workflows into app repos
- ❌ Do NOT edit reusable workflows from app repos
- ✅ Changes must happen in .github repo only

---
