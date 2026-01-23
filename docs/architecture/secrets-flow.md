---
layout: default
title: Secrets & Permissions Flow
mermaid: true
---

```mermaid
flowchart LR
    PAT[Fine-grained PAT<br/>Org-owned]
    Secret[RELEASE_TOKEN<br/>Repo Secret]

    Secret --> CallerWF[Repo Release Workflow]
    CallerWF --> ReusableWF[Reusable Release Workflow]

    ReusableWF -->|env:GITHUB_TOKEN| SemanticRelease

    SemanticRelease --> GitHubAPI[GitHub API]
```