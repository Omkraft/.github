# Release Process

## Tooling

Omkraft uses:

- `semantic-release`
- Conventional Commits
- GitHub Actions

---

## When a Release Happens

A release is triggered when:

- A PR is merged into `main`
- The merge commit contains Conventional Commit messages

---

## Version Calculation

| Commit Type | Version Impact |
|-----------|---------------|
| feat | minor |
| fix | patch |
| feat! | major |
| BREAKING CHANGE | major |

---

## What Happens Automatically

On release:
- Git tag is created (e.g. `v1.2.0`)
- GitHub Release is created
- Release notes are generated
- Commit history is analyzed

---

## Where to See Releases

- **Actions → Release workflow**
- **Code → Releases**
- **Tags**

If nothing appears:
- No release-worthy commits were detected
- Or commit messages were invalid
