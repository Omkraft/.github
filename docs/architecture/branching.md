# Branching Strategy

## Protected Branches

| Branch | Rules |
|------|------|
| main | Fully protected |

---

## main Branch Rules

- No direct pushes
- PR required
- Required workflows must pass
- Linear history preferred

---

## Feature Branches

Format:
```yaml
feature/<short-description>
fix/<short-description>
chore/<short-description>
```

---

## Merging Strategy

- Squash merge preferred
- Merge commit must follow Conventional Commits
