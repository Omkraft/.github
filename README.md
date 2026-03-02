<p align="center">
  <img src="https://raw.githubusercontent.com/Omkraft/.github/main/assets/logo-primary-square.svg" alt="Omkraft Logo" width="240" />
</p>

<h1 align="center">Omkraft Org Infrastructure</h1>

<p align="center">
  <strong>Shared branding, templates, reusable workflows, and engineering governance</strong>
</p>

<p align="center">
  Systems, Crafted.
</p>

---

## 🧭 Purpose

This repository is the organization-level source of truth for:
- Shared GitHub workflows consumed by app repositories
- Issue and pull request templates
- Brand assets and usage guidance
- Engineering governance and architecture docs

It exists to keep cross-repo standards centralized and consistent.

---

## 📦 What Lives Here

```text
.github/
|-- .github/
|   |-- ISSUE_TEMPLATE/                 # Org issue templates
|   |-- PULL_REQUEST_TEMPLATE.md
|   `-- workflows/
|       |-- pr-title.yml                # Reusable PR title lint workflow
|       `-- release.yml                 # Reusable semantic-release workflow
|-- assets/                             # Production-ready brand assets
|-- brand/                              # Brand source and usage guide
`-- docs/                               # Engineering governance + architecture docs
```

---

## 🛠️ Reusable Workflows

Reusable workflows exported from this repo:
- `.github/workflows/pr-title.yml`
- `.github/workflows/release.yml`

Consumer repos currently:
- `app-ui` calls reusable `pr-title` and `release`, and defines local PR lint/build + deploy orchestration
- `app-api` calls reusable `pr-title` and `release`, and defines local PR lint + deploy orchestration

---

## 🎨 Branding Assets

Use assets from `/assets` in downstream repositories (READMEs, docs, app surfaces).

Example:

```html
<img src="https://raw.githubusercontent.com/Omkraft/.github/main/assets/logo-primary-square.svg" />
```

---

## 📚 Documentation

Engineering docs are under [`docs/`](docs/README.md), including:
- CI/CD architecture
- Workflow ownership model
- Release pipeline behavior
- Secret and permission guidance
- Onboarding and glossary

---

## ✅ Maintenance Notes

When changing workflow behavior:
1. Update reusable workflow file(s) in this repo.
2. Update corresponding docs under `docs/architecture`.
3. Verify consumer repos still call workflows correctly.

---

## 🏷️ License

MIT

---

<p align="center">Built by<br/><strong>Omkraft Inc.</strong><br/>Systems, Crafted.</p>
<p align="center"><img src="https://raw.githubusercontent.com/Omkraft/.github/main/assets/logo-small.svg" alt="Omkraft Logo Small" width="48" height="48" /></p>
