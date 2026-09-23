# Project Charter — Transaction Care

## 1. Purpose

Transaction Care explores whether consumers will pay for an independent care and verification layer immediately before a vulnerable transaction.

The first experiments are:

- **TC-01A — Property Care:** residential property sale/rental transactions.
- **TC-01B — Seasonal Rental Care:** vacation and seasonal rental transactions.

## 2. Core hypothesis

> There may be willingness to pay for independent evidence, verification and risk signaling immediately before a vulnerable transaction.

This is a hypothesis to validate, not an established market fact.

## 3. Product promise

**Evidence before you transfer your money.**

The system should help a user understand:

- what evidence exists;
- what evidence is missing;
- whether information is internally consistent;
- which risk signals deserve attention;
- what should be checked before committing.

## 4. Product boundaries

The initial system must not:

- declare a transaction fraudulent;
- certify that a transaction is safe;
- replace legal advice;
- guarantee financial recovery;
- operate a marketplace;
- process payments;
- provide escrow.

## 5. Shared architecture hypothesis

TC-01A and TC-01B should use the same core:

`Transaction → Entity → Evidence → Verification → Risk Signals → Decision Support`

Vertical-specific rules should be modular rather than duplicated.

## 6. Validation priorities

The first experiment should establish:

1. whether users have meaningful uncertainty before the transaction;
2. whether the system can produce useful evidence;
3. whether evidence changes or confirms a decision;
4. whether verification saves user time;
5. whether users would pay;
6. whether the workflow is repeatable;
7. whether the core can transfer between verticals.

## 7. Capital discipline

Development follows progressive validation:

`Signal → Hypothesis → Prototype → Validation → Pilot → MVP`

No significant infrastructure investment should precede evidence of user value.
