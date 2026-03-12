# 🔐 Secrets and Tokens

## 🎫 Release Token Strategy

Reusable release workflow requires a `RELEASE_TOKEN` secret (fine-grained PAT) from each consumer repo.

Why:
- Workflow needs permission to create tags and GitHub Releases.
- Token scope is explicit and auditable.

---

## 🧾 Minimum Permissions

| Permission | Access |
| --- | --- |
| Contents | Read and Write |
| Pull Requests | Read |
| Metadata | Read |

`Releases` is covered under `Contents` permissions.

---

## 🗄️ Storage Pattern

Store the release token as a repository secret:
- `RELEASE_TOKEN`

The reusable release workflow maps it to `GITHUB_TOKEN` only for `semantic-release` execution.

---

## 🤖 PR-Agent LLM Secret

Reusable PR review workflow requires an `OPENAI_KEY` secret.

Recommended storage pattern:
- Create `OPENAI_KEY` as an organization Actions secret
- Grant it to `.github`, `app-ui`, and `app-api`

Current usage:
- `.github/.github/workflows/pr-agent-review.yml`
- Repository root `.pr_agent.toml` in `.github`, `app-ui`, and `app-api`

Minimum workflow permissions for PR-Agent:
- `contents: read`
- `issues: write`
- `pull-requests: write`
