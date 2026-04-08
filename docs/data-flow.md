# Data Flow

## Public-safe system story

The wallet engine is fed by upstream operational and financial collection systems. In the live workflow, source files move through a controlled intake path, are scanned, enriched with metadata, validated, and then imported into Luna's local data layer.

## High-level stages

1. Upstream capture systems produce source files or structured exports.
2. Intake folders receive those files in a controlled local workflow.
3. Validation and quarantine rules block unsafe or malformed inputs.
4. Approved records are normalized into the local system of record.
5. Ledger and balance logic derive usable wallet state from posted anchors and transaction history.
6. Expense-matching logic compares expected obligations against imported payment activity.
7. Outward-safe exports and reports are produced for review surfaces.

## What this repo emphasizes

- the engine and process design
- the movement from intake to normalized ledger state
- the safety boundaries around public demonstration

## What this repo intentionally omits

- secrets
- raw live financial records
- private automation credentials
- personal screenshots containing real values
