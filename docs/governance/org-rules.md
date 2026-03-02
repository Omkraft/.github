# 🧱 Organization Rules

## Enforced Practices

- Conventional Commit-style PR titles.
- Required checks before merge to protected branch.
- Automated release publication from `main`.
- Shared guardrails managed centrally in `Omkraft/.github`.

---

## Things to Avoid

- Disabling workflows to force a merge.
- Manual release publishing that bypasses semantic-release.
- Editing reusable workflow behavior in consumer repos.
- Changing token permissions without review.

---

## Change Management

For any CI/CD or governance update:
1. Update workflow/template/docs in this repository.
2. Validate behavior in consumer repos.
3. Keep architecture docs and diagrams aligned.
