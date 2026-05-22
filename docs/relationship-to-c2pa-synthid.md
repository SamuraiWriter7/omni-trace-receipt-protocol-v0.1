# Relationship to C2PA and SynthID

Omni Trace Receipt Protocol v0.1 is designed to complement media provenance and watermarking systems such as C2PA, Content Credentials, and SynthID-like technologies.

C2PA focuses on digital content provenance and authenticity. Its technical specification describes provenance as the history of an asset and its interaction with actors and other assets, represented through provenance data such as C2PA manifests. Authenticity is treated as a property of digital content supported by verifiable facts, such as provenance data and content bindings.

SynthID-like systems focus on watermarking and identifying AI-generated or AI-altered content. Google DeepMind describes SynthID as a tool for embedding imperceptible digital watermarks into AI-generated images, audio, text, and video so that such content can later be identified.

Omni Trace Receipt Protocol addresses a different but adjacent layer:

```text
C2PA / Content Credentials = What is the provenance and authenticity history of this media asset?
SynthID-like watermarking = Was this content generated or altered by AI?
Omni Trace Receipt Protocol = Which sources, structures, questions, concepts, or works contributed to this AI-mediated output?

In short:

C2PA and SynthID-like systems help verify the output.
Omni Trace Receipt Protocol helps record the source-output relationship.

1. Output Provenance vs. Source-Output Trace

C2PA and SynthID-like systems primarily operate on the generated or edited asset.

They can help answer questions such as:

Was this asset generated or modified by AI?
What tool or actor created or edited it?
What provenance metadata is attached?
Has the asset’s provenance metadata been tampered with?
Can this media object be verified through a watermark or manifest?

Omni Trace Receipt Protocol asks a different set of questions:

What sources may have contributed to this AI output?
Was the source explicitly cited?
Was the source summarized without a user click?
Was a structure, schema, method, or concept reused?
Was the source transformed into another medium?
Is attribution review required?
Is origin audit required?
Is the trace disputed?
Could this become an allocation-readiness candidate?

This distinction is central.

C2PA and SynthID-like systems are mostly about the output object.

Omni Trace Receipt Protocol is about the relationship between the output and its possible sources.

2. Why Provenance Alone Is Not Enough

Media provenance is essential, but it does not fully solve zero-click AI consumption.

A generated video may be clearly marked as AI-generated.

An image may contain content credentials.

A text or media object may carry a watermark.

Yet none of these automatically tells us:

Which article was summarized?
Which concept was transformed?
Which question shaped the output?
Which structure was reused?
Which source lost the click?
Which creator’s work became invisible fuel?

This is the gap Omni Trace Receipt Protocol is designed to address.

It adds a receipt layer for AI-mediated use.

3. Complementary Roles
Layer	Primary Function	Example Question
C2PA / Content Credentials	Media provenance and authenticity metadata	What happened to this asset, and who or what created or modified it?
SynthID-like watermarking	AI-generated content identification	Does this asset contain an AI-generation watermark?
Omni Trace Receipt Protocol	Source-output trace relationship	Which sources, concepts, structures, or works contributed to this AI-mediated output?
Origin Audit	Review of source-output claims	Is the claimed source relationship credible?
Royalty OS	Value-circulation layer	Should value flow back, and how?

These systems should not be treated as competitors.

They address different parts of the AI accountability stack.

4. Suggested Stack
Media Object / AI Output
↓
C2PA Manifest / Content Credentials
↓
SynthID-like Watermark Detection
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

This stack separates:

asset provenance,
AI-generation identification,
source-output trace recording,
origin audit,
attribution review,
dispute handling,
value allocation readiness.

Each layer has a different job.

5. Example Scenario

A user asks an AI system to generate a short video explaining a complex research topic.

The AI system creates a video.

The video may include:

C2PA / Content Credentials:
  Records that the video was generated or edited by a certain AI tool.

SynthID-like watermark:
  Indicates that the video contains AI-generated media.

Omni Trace Receipt:
  Records that the video appears to draw from several articles,
  one research paper, and a conceptual framework.

Origin Audit:
  Reviews whether those source-output relationships are credible.

Royalty OS:
  May later evaluate whether any source is an allocation candidate.

Without C2PA or SynthID-like systems, the user may not know the media is AI-generated.

Without Omni Trace Receipt, the user may not know which human sources, concepts, or structures contributed to the output.

Both are necessary.

6. Suggested Receipt Representation

In Omni Trace Receipt Protocol v0.1, C2PA or SynthID-like references may be represented through provenance_references.

Example:

{
  "provenance_references": [
    {
      "reference_type": "c2pa",
      "reference_value": "https://example.com/c2pa-manifest/asset-000001",
      "note": "Optional C2PA manifest associated with the AI-generated output."
    },
    {
      "reference_type": "content_credentials",
      "reference_value": "https://example.com/content-credentials/asset-000001",
      "note": "Optional Content Credentials record associated with the media output."
    },
    {
      "reference_type": "synthid_like",
      "reference_value": "synthid-detection-record-000001",
      "note": "Optional watermark detection reference for AI-generated content."
    }
  ]
}

These fields do not replace C2PA or SynthID-like systems.

They simply allow an Omni Trace Receipt to point to them.

7. What Omni Trace Receipt Does Not Do

Omni Trace Receipt Protocol does not:

verify C2PA manifests,
detect SynthID watermarks,
authenticate media assets,
determine whether media metadata has been tampered with,
replace content credentials,
replace watermark detection,
determine legal authorship,
determine copyright infringement.

It only records source-output trace relationships and related audit metadata.

8. Why This Matters for Generative Media

Omni-style AI environments increasingly transform inputs across media types.

For example:

article → video
question → image
research paper → explainer animation
code repository → generated tutorial
conceptual framework → multimodal presentation

In these cases, the final media object may be clearly marked as AI-generated.

But the deeper question remains:

What human sources, structures, questions, or works made this output possible?

C2PA and SynthID-like systems help us understand the media object.

Omni Trace Receipt Protocol helps us understand the value genealogy behind the media object.

9. Design Position

Omni Trace Receipt Protocol should be understood as a source-trace layer that can sit alongside media provenance and watermarking systems.

It is not an authenticity layer.

It is not an AI-detection layer.

It is not a watermarking layer.

It is a receipt layer.

Its purpose is to record that an AI-mediated output may have used or transformed external sources, structures, concepts, or works.

10. Summary

C2PA, Content Credentials, SynthID-like systems, and Omni Trace Receipt Protocol are complementary.

C2PA asks:
What is the provenance and authenticity history of this asset?

SynthID-like watermarking asks:
Was this content generated or altered by AI?

Omni Trace Receipt asks:
Which sources, structures, questions, concepts, or works contributed to this AI-mediated output?

In the zero-click and generative AI era, output authenticity is not enough.

We also need source-output traceability.

A watermark may tell us that AI generated the content.

A content credential may tell us how the asset was created or edited.

A trace receipt may tell us what human knowledge, structure, or creative work was consumed or transformed along the way.

That is the missing layer Omni Trace Receipt Protocol v0.1 is designed to provide.
