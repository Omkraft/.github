# 🏷️ Release Process

## Tooling

Omkraft release automation uses:
- `semantic-release`
- Conventional Commit semantics
- GitHub Actions reusable release workflow

---

## Trigger

Release runs on push to `main` through each app repo's release workflow, which calls:

```yaml
uses: Omkraft/.github/.github/workflows/release.yml@main
```

---

## Version Calculation

| Change type | Version impact |
| --- | --- |
| `fix` | patch |
| `feat` | minor |
| `feat!` or `BREAKING CHANGE` | major |

---

## Output

When release-worthy commits are present:
- New tag is created (example: `v1.7.0`)
- GitHub Release is created
- Release notes are generated

When no release-worthy commits exist:
- `semantic-release` exits without creating a new tag/release

---

## Repo Nuance

- `app-ui` deployment expects a release tag on the commit and fails deploy if missing.
- `app-api` deploy currently runs before release in its pipeline.
