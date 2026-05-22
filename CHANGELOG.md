# Changelog

All notable changes to this project will be documented in this file.

This project follows a lightweight versioning model for early protocol drafts.

---

## v0.1.0 - 2026-05-22

Initial draft release of **Omni Trace Receipt Protocol v0.1**.

### Added

- Initial `README.md`
- Human-readable protocol specification:
  - `spec/omni-trace-receipt-v0.1.yaml`
- JSON Schema:
  - `schemas/omni-trace-receipt.schema.json`
- Example receipt objects:
  - `examples/explicit-source-use.example.json`
  - `examples/zero-click-summary.example.json`
  - `examples/generative-remix.example.json`
  - `examples/disputed-origin.example.json`
- Documentation:
  - `docs/relationship-to-rsl.md`
  - `docs/relationship-to-c2pa-synthid.md`
  - `docs/relationship-to-royalty-os.md`
  - `docs/zero-click-consumption-risk.md`
- Project metadata:
  - `CHANGELOG.md`
  - `CITATION.cff`
  - `LICENSE`

### Notes

This release defines the first minimal receipt layer for recording AI-mediated use in zero-click, multimodal, and generative AI environments.

The protocol does not determine copyright ownership, legal infringement, or final royalty allocation.

It creates structured trace evidence that may later support:

- origin audit,
- attribution review,
- dispute handling,
- allocation-readiness checks,
- Royalty OS or related value-circulation systems.
