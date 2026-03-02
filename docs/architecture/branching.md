# 🌿 Branching Strategy

## Protected Branches

| Branch | Policy |
| --- | --- |
| `main` | Protected; direct push blocked; required checks enforced |

---

## Feature Branches

Recommended patterns:

```text
feature/<short-description>
fix/<short-description>
chore/<short-description>
```

---

## Merge Strategy

- Open PR into `main`.
- Ensure required checks pass.
- Use clean, conventional PR titles.
- Squash merge is preferred for readable history.
