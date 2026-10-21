# Product Release webhook PPE validation

This file validates the Learn Build Service Readonly GitHub App release webhook
and Product Release processing in PPE.

Validation sequence:

1. Baseline release: `v0.0.1-ppe`
2. Merge this pull request into `main`
3. Publish release: `v0.0.2-ppe`

This is a PPE-only validation change and does not modify vcpkg-tool behavior.

## 2026-10-21 validation

Smoke test for the Content Maintenance Categorization feature (ADR-0003) in PPE.

Validation sequence:

1. Baseline release: `2026-10-08`
2. Merge this pull request into `main`
3. Publish release: `2026-10-21`

Expected outcome: the Product Release signal analyzes the PR merged between the
`2026-10-08` and `2026-10-21` releases and creates an issue in
`OPS-E2E-PPE/vcpkg-docs` with suggestions rendered using the ChangeType/Topic/Priority/Impact
dimensions (not the old flat `Category` label).
