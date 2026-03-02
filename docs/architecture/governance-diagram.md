---
layout: default
title: Governance and Branch Protection
---

```mermaid
flowchart TD
    Direct[Direct push to main] -->|Blocked by branch protection| Deny[Deny]
    PR[Pull Request] --> Checks[Required checks]

    Checks -->|Fail| Block[Merge blocked]
    Checks -->|Pass| Allow[Merge allowed]

    Allow --> Pipeline[Main pipeline]
    Pipeline --> Shared[Shared release workflow]
```
