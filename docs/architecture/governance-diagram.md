---
layout: default
title: Governance & Branch Protection
---

```mermaid
flowchart TD
    Push[Direct Push] -->|Blocked| Main[main]
    PR[Pull Request] --> Checks[Required Workflows]

    Checks -->|Fail| Block[Merge Blocked]
    Checks -->|Pass| MergeAllowed[Merge Allowed]

    MergeAllowed --> Release[Automated Release]
```