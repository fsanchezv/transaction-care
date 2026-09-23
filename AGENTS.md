# Codex Development Instructions

## Mission

Build the smallest testable Transaction Care system for TC-01A Property Care and TC-01B Seasonal Rental Care.

## Non-negotiable product rules

1. Do not build a marketplace in the initial validation stage.
2. Do not implement payments or escrow.
3. Do not produce a binary "safe/fraudulent" verdict.
4. Every material verification claim must retain evidence provenance.
5. Separate observed facts from inference and risk signals.
6. Prefer deterministic rules for explicit checks.
7. AI may assist extraction, normalization, comparison and explanation, but must not silently invent evidence.
8. Keep the core vertical-agnostic.
9. Prefer simple, testable components over premature infrastructure.
10. Add tests for domain logic before expanding UI.

## Core domain

Transaction → Entity → Evidence → Verification → RiskSignal → DecisionSupport

## TC-01B priority

Implement seasonal rental first as the first end-to-end vertical because it is expected to provide a compact, testable transaction workflow.

Initial verification categories:

- property existence;
- address/location consistency;
- offering-party identity;
- offer/content consistency;
- image/content consistency where technically and legally appropriate;
- payment conditions;
- cancellation/refund conditions;
- anomaly/risk signals.

## TC-01A

Reuse the same core and add property-specific rules only where required.

## Engineering principles

- Type-safe domain models.
- Explicit provenance.
- Deterministic fixtures for tests.
- No external API dependency required for unit tests.
- Configuration over duplicated vertical logic.
- Keep provider/model adapters isolated.
- Do not add credentials to the repository.
- Use environment variables for external services.
- Document external data-source assumptions.

## Experiment instrumentation

The system should make it possible to measure:

- verification completion;
- evidence coverage;
- report generation time;
- risk signals produced;
- decision impact;
- willingness-to-pay test exposure;
- repeat use.

Decision Impact is defined as a user changing, delaying or confirming a transaction decision because of the verification output.

## Delivery sequence

1. Domain model.
2. Fixtures.
3. Core verification engine.
4. TC-01B rules.
5. Report representation.
6. Tests.
7. Basic UI/API.
8. TC-01A reuse and rules.

Do not expand scope without evidence from the validation plan.
