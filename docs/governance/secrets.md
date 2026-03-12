# ?? Secrets and Tokens

## ?? Release Token Strategy

Reusable release workflow requires a `RELEASE_TOKEN` secret (fine-grained PAT) from each consumer repo.

Why:
- Workflow needs permission to create tags and GitHub Releases.
- Token scope is explicit and auditable.

---

## ?? Minimum Permissions

| Permission | Access |
| --- | --- |
| Contents | Read and Write |
| Pull Requests | Read |
| Metadata | Read |

`Releases` is covered under `Contents` permissions.

---

## ??? Storage Pattern

Store the release token as a repository secret:
- `RELEASE_TOKEN`

The reusable release workflow maps it to `GITHUB_TOKEN` only for `semantic-release` execution.

---

## ?? Ollama Review Secrets

The Ollama-based PR review workflow does not require an external LLM API secret.

Current usage:
- `.github/.github/workflows/ollama-review.yml`

Required GitHub Actions permissions for review comments:
- `contents: read`
- `pull-requests: write`
