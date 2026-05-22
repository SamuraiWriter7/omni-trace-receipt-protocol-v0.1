# Changelog

All notable changes to this project will be documented in this file.

This project follows a lightweight versioning approach during the v0.1 development phase.

---

## [0.1.1] - 2026-05-23

### Added

- Added `docs/architecture-overview.md`.
- Added an architecture overview for positioning the receipt layer before trace claims, origin audit, allocation readiness, and Royalty OS.
- Added the following architecture flow:

```text
Receipt
↓
Trace
↓
Claim
↓
Origin Audit
↓
Allocation Readiness
↓
Royalty OS
```

- Added README references to `docs/architecture-overview.md`.
- Added `docs/architecture-overview.md` to the Repository Structure section.
- Added `docs/architecture-overview.md` to the Start Here reading order.

### Clarified

- Clarified that the receipt layer is the minimal evidence layer before stronger trace claims.
- Clarified that a receipt is not an ownership claim, legal judgment, attribution decision, or royalty allocation.
- Clarified the role of the receipt layer as a record-before-judgment layer.
- Clarified the relationship between the receipt layer and later review layers such as origin audit, attribution review, allocation readiness, and Royalty OS.

### Notes

This release keeps the core protocol unchanged.

The v0.1.1 update only adds architectural context around the existing protocol.

No schema-breaking changes were introduced.

---

## [0.1.0] - 2026-05-22

### Added

- Initial release of Omni Trace Receipt Protocol v0.1.
- Added `README.md`.
- Added human-readable protocol specification:

```text
spec/omni-trace-receipt-v0.1.yaml
```

- Added JSON Schema for validating receipt objects:

```text
schemas/omni-trace-receipt.schema.json
```

- Added example receipt objects:

```text
examples/explicit-source-use.example.json
examples/zero-click-summary.example.json
examples/generative-remix.example.json
examples/disputed-origin.example.json
```

- Added supporting documentation:

```text
docs/relationship-to-rsl.md
docs/relationship-to-c2pa-synthid.md
docs/relationship-to-royalty-os.md
docs/zero-click-consumption-risk.md
```

- Added project metadata files:

```text
CHANGELOG.md
CITATION.cff
LICENSE
```

### Defined

- Defined the Omni Trace Receipt object.
- Defined the concept of a minimal trace receipt for AI-mediated use.
- Defined zero-click AI consumption as a key risk.
- Defined receipt-before-judgment as the core design principle.
- Defined basic receipt fields including:
  - `receipt_id`
  - `protocol_version`
  - `created_at`
  - `ai_environment`
  - `output_context`
  - `source_traces`
  - `usage_assessment`
  - `transformation_profile`
  - `audit_status`
  - `royalty_readiness`
  - `dispute_status`

### Documented

- Documented usage types:
  - `explicit_reference`
  - `zero_click_summary`
  - `implicit_influence`
  - `structural_derivation`
  - `generative_remix`
  - `action_guidance`
  - `disputed_trace`

- Documented non-goals:
  - no copyright ownership determination,
  - no infringement judgment,
  - no automatic royalty calculation,
  - no replacement of human review,
  - no replacement of legal or institutional process.

### Notes

This release establishes Omni Trace Receipt Protocol v0.1 as a minimal evidence layer for traceability, origin audit, attribution review, dispute handling, and future value-circulation systems.

It does not define a royalty distribution system.

It does not define an ownership system.

It does not define a legal enforcement mechanism.

It creates a structured receipt before stronger claims, audits, or allocation decisions are made.
