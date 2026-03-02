---
layout: default
title: CI/CD Overview
---

# CI/CD Architecture (Omkraft)

## Overview

Omkraft uses a hybrid model:
- Reusable workflows in `Omkraft/.github` for shared guardrails
- Repo-local workflows for product-specific lint/build/deploy behavior

This keeps standards centralized while preserving per-repo deployment logic.

---

## Current Shared Workflows

From `Omkraft/.github/.github/workflows`:
- `pr-title.yml` (semantic PR title lint)
- `release.yml` (semantic-release)

There is no reusable lint workflow currently.

---

## High-Level Flow

1. Developer opens PR.
2. PR checks run:
   - Reusable PR title lint
   - Repo-local lint/build checks
3. PR merges to `main`.
4. Repo release pipeline runs and calls reusable release workflow.
5. Deploy step runs based on each repo's local workflow design.

---

## Repo-Specific Differences

- `app-ui`: release happens before production deploy; deploy requires a release tag.
- `app-api`: deploy happens before release in current workflow.

---

## Diagrams

- [CI/CD Flow](ci-cd-diagram.md)
- [Reusable Workflows](workflows-diagram.md)
- [Release Pipeline](release-pipeline.md)
- [Secrets & Permissions](secrets-flow.md)
- [Governance Model](governance-diagram.md)
