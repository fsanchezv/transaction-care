# Transaction Care

AI-assisted infrastructure for verification, evidence, and risk signals immediately before vulnerable transactions.

## Initial verticals

- TC-01A — Property Care
- TC-01B — Seasonal Rental Care

## Product principle

The initial product does not decide whether a transaction is a scam or whether a property is "safe". It organizes evidence, identifies missing evidence and inconsistencies, surfaces risk signals, and helps the user make a better-informed decision before transferring money or committing.

## Initial scope

This repository starts as an experimental foundation. The first objective is to validate whether users obtain meaningful decision value from an independent verification layer immediately before a vulnerable transaction.

The first release intentionally excludes:

- marketplace functionality
- payment processing
- escrow
- financial guarantees
- definitive fraud verdicts

## Core architecture

`Transaction → Entity → Evidence → Verification → Risk Signals → Decision Support`

The core engine must be reusable across verticals.

## Repository structure

```text
transaction-care/
├── README.md
├── PROJECT.md
├── ROADMAP.md
├── docs/
│   ├── architecture.md
│   ├── hypotheses.md
│   ├── validation-plan.md
│   └── legal-questions.md
├── apps/
│   ├── tc-01a-property/
│   └── tc-01b-seasonal-rental/
├── packages/
│   ├── identity/
│   ├── evidence/
│   ├── verification/
│   ├── risk-engine/
│   └── shared/
└── tests/
```

## Development principle

Build the smallest testable system first. Prioritize observability, evidence quality, experiment design, and decision impact over visual complexity.
