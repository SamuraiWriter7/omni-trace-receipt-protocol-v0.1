# Relationship to RSL

Omni Trace Receipt Protocol v0.1 is designed to complement RSL-style licensing and permission layers.

RSL defines machine-readable licensing, usage, and compensation terms for content access and AI-related use. According to RSL Collective materials, RSL can express permissions and payment conditions such as attribution, paid AI training, pay-per-use, and pay-per-output style licensing through machine-readable declarations.  

Omni Trace Receipt Protocol does not replace RSL.

Instead, it addresses a different layer:

```text
RSL = Permission and licensing conditions
Omni Trace Receipt Protocol = Record of AI-mediated use

In other words, RSL can say:

“This content may be used under these conditions.”

Omni Trace Receipt can say:

“This content, structure, question, or work appears to have been used in this AI-mediated output.”

1. Permission Layer vs. Receipt Layer

RSL-style systems are primarily concerned with permission, licensing, and compensation conditions.

They may express:

whether content may be crawled,
whether content may be used for AI training,
whether attribution is required,
whether payment is required,
whether use is limited to certain purposes,
whether a collective license applies.

Omni Trace Receipt Protocol is concerned with recording use after, during, or around AI-mediated consumption.

It records:

what source may have been used,
how it may have been used,
whether the use was explicit or implicit,
whether it was a zero-click summary,
whether it involved structural derivation,
whether it involved generative remix,
whether attribution review is needed,
whether origin audit is needed,
whether the trace may become an allocation candidate.

The distinction is important.

RSL is a permission signal.

Omni Trace Receipt is a use record.

2. Why Both Layers Are Needed

A permission layer alone is not enough.

Even if a source declares licensing or compensation conditions, an AI governance system still needs a way to record whether actual use occurred.

For example:

A publisher declares AI use conditions through RSL.
↓
An AI system summarizes the publisher's article in a zero-click answer.
↓
A trace receipt records that the article may have contributed to the AI output.
↓
Origin audit or attribution review can evaluate the relationship.
↓
Royalty OS or another value-circulation system may later evaluate allocation readiness.

Without the receipt layer, permission terms may exist but lack a concrete usage record.

Without the permission layer, trace receipts may record use but lack declared licensing context.

Together, the two layers form a more complete governance path.

3. Suggested Flow
RSL Declaration
↓
AI Access / AI-Mediated Use
↓
Omni Trace Receipt
↓
Origin Audit
↓
Attribution Review
↓
Dispute Handling
↓
Allocation Readiness
↓
Royalty OS / Value Circulation

This flow separates each stage clearly.

RSL defines permission and conditions.
Omni Trace Receipt records use.
Origin audit evaluates source-output relationships.
Attribution review determines whether disclosure or citation is needed.
Dispute handling manages contested claims.
Allocation readiness determines whether the trace is suitable for value allocation review.
Royalty OS or a similar system may perform value circulation.
4. Example Mapping
Layer	Role	Example Question
RSL	Permission / licensing	May this source be used by AI under these terms?
Omni Trace Receipt	Use record	Was this source used in this AI output?
Origin Audit	Source relationship review	What is the relationship between the source and the output?
Attribution Review	Disclosure / citation review	Should the source be cited or disclosed?
Dispute Registry	Conflict handling	Is the trace claim contested?
Allocation Readiness	Pre-allocation review	Is this trace suitable for value allocation review?
Royalty OS	Value circulation	Should value flow back, and how?
5. RSL-Compatible Fields

Future versions of Omni Trace Receipt Protocol may add explicit RSL bridge fields, such as:

permission_layer:
  protocol: RSL
  license_reference: https://example.com/rsl-license.xml
  declared_ai_usage:
    - ai-train
    - ai-input
    - ai-output
  payment_model:
    - attribution
    - pay_per_use
    - pay_per_output
  license_status: declared

These fields are not required in v0.1.0.

For now, RSL-related information may be represented through external_protocol_links or provenance_references.

Example:

{
  "external_protocol_links": [
    {
      "protocol_name": "RSL",
      "protocol_version": "unspecified",
      "reference": "https://example.com/rsl-license.xml",
      "relationship": "complements"
    }
  ]
}
6. What Omni Trace Receipt Does Not Do

Omni Trace Receipt Protocol does not:

define licensing terms,
collect royalties,
enforce crawler access rules,
determine whether an AI provider complied with RSL,
replace RSL,
replace legal contracts,
determine copyright ownership,
determine infringement.

It only records a structured trace of AI-mediated use.

That trace may later be compared with permission declarations such as RSL.

7. Why This Matters for Zero-Click AI

Zero-click AI consumption creates a gap between permission and visible user behavior.

A user may never click the original source.

The AI interface may summarize, transform, or remix source material directly.

In such cases, the source may lose traffic, attribution, and visibility even if its value contributed to the output.

RSL can help define how content may be used.

Omni Trace Receipt can help record when content appears to have been used.

Together, they provide a foundation for a more accountable AI content economy.

8. Design Position

Omni Trace Receipt Protocol should be understood as a downstream or adjacent layer to RSL.

It is not a competitor.

It is a receipt layer that can help answer:

Given a permission declaration,
what actual AI-mediated use occurred?

This makes the protocol useful for:

audit logs,
attribution review,
dispute handling,
royalty-readiness workflows,
creator economy infrastructure,
AI governance systems.
9. Summary

RSL and Omni Trace Receipt Protocol address different but complementary parts of the AI content-use problem.

RSL asks:
Can this content be used, and under what conditions?

Omni Trace Receipt asks:
Was this content, structure, question, or work used, and how should that use be reviewed?

In the zero-click AI era, both layers are needed.

Permission without receipts is difficult to audit.

Receipts without permission context are difficult to govern.

Together, they can support a future where AI systems are not only powerful, but traceable, accountable, and capable of participating in fair value circulation.
