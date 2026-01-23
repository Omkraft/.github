---
layout: mermaid
title: Reusable Workflow Architecture
mermaid: true
---

```mermaid
flowchart LR
    AppAPI[app-api repo]
    AppUI[app-ui repo]

    AppAPI -->|uses| ReusableRelease
    AppUI -->|uses| ReusableRelease

    ReusableRelease[Omkraft/.github<br/>Reusable Workflows]

    ReusableRelease --> LintWF[lint.yml]
    ReusableRelease --> PRTitleWF[pr-title.yml]
    ReusableRelease --> ReleaseWF[release.yml]
```