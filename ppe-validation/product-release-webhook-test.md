# Product Release webhook PPE validation

This file validates the Learn Build Service Readonly GitHub App release webhook
and Product Release processing in PPE.

Validation sequence:

1. Baseline release: `v0.0.1-ppe`
2. Merge this pull request into `main`
3. Publish release: `v0.0.2-ppe`

This is a PPE-only validation change and does not modify vcpkg-tool behavior.
