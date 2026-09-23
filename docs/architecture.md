# Architecture

## Design principle

Transaction Care is an evidence-oriented decision-support system, not a fraud classifier.

## Core pipeline

```
INPUT
  ↓
TRANSACTION
  ↓
ENTITY EXTRACTION
  ↓
IDENTITY
  ↓
EVIDENCE
  ↓
CROSS-CHECK
  ↓
VERIFICATION RULES
  ↓
RISK SIGNALS
  ↓
DECISION SUPPORT
```

## Core domains

### Transaction

Represents the proposed transaction and its context.

Minimum conceptual fields:

- transaction_id
- vertical
- source_url
- transaction_type
- amount
- currency
- date/context
- submitted_at

### Entity

Represents people, organizations, properties, offers, platforms or other relevant objects.

### Evidence

Evidence must preserve provenance.

Conceptual fields:

- evidence_id
- transaction_id
- evidence_type
- source
- observed_value
- captured_at
- provenance
- confidence
- status

### Verification

A verification is a test applied to evidence.

Examples:

- identity consistency;
- address consistency;
- offer consistency;
- existence;
- document consistency;
- rule compliance.

### Risk Signal

A risk signal identifies something that deserves attention.

It is not itself a fraud verdict.

Each signal should contain:

- signal_type
- description
- supporting_evidence
- severity
- confidence
- unresolved_questions

### Decision Support

The output should separate:

1. positive evidence;
2. missing evidence;
3. inconsistencies;
4. risk signals;
5. recommended checks before commitment.

## Architecture rule

The core engine must not contain property-specific or seasonal-rental-specific logic when that logic can be expressed as configurable vertical rules.

## AI architecture

AI should assist with:

- extraction;
- classification;
- summarization;
- evidence normalization;
- comparison;
- natural-language explanation.

Critical verification claims should retain explicit provenance and deterministic rule evaluation where practical.

The architecture must remain AI-agnostic so that models can be replaced without redesigning the business logic.
