# 🔐 Secrets and Tokens

## Release Token Strategy

Reusable release workflow requires a `RELEASE_TOKEN` secret (fine-grained PAT) from each consumer repo.

Why:
- Workflow needs permission to create tags and GitHub Releases.
- Token scope is explicit and auditable.

---

## Minimum Permissions

| Permission | Access |
| --- | --- |
| Contents | Read and Write |
| Pull Requests | Read |
| Metadata | Read |

`Releases` is covered under `Contents` permissions.

---

## Storage Pattern

Store token as repository secret:
- `RELEASE_TOKEN`

The reusable workflow maps it to `GITHUB_TOKEN` only for `semantic-release` execution.
