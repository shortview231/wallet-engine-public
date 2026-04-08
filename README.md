# Wallet Engine Public

Public-facing baseline for Luna's wallet ingestion, ledger, and expense-matching engine.

This repo documents the engine behind a desktop-first wallet operations surface. The public baseline is intentionally engine-first: it focuses on controlled ingestion, normalization, balance derivation, expense matching, and outward-safe exports. It does not publish live financial data, secrets, or personal records.

## What the engine does

- ingests controlled upstream financial and operational signals
- validates and quarantines unsafe inputs
- normalizes records into a local system of record
- derives usable ledger and balance state
- matches expected expenses against payments
- exports outward-safe reporting surfaces

## What this public repo includes

- architecture and workflow documentation
- proxy datasets that mirror the real data shape
- recreated demo screenshots using proxy values
- explicit safety boundaries for public publication

## What this repo does not include

- Live banking data
- Raw CSV imports
- Secrets or `.env` values
- Original screenshots containing real values
- The Luna UI implementation as the primary product surface

## Source of truth

The working implementation source lives in `~/Desktop/Projects/Luna_Ingestion`.

## Proof layer

- `screenshots/ledger-overview-demo.svg` shows posted vs derived balance logic
- `screenshots/ledger-transactions-demo.svg` shows normalized ledger rows and balance interpretation
- `screenshots/expenses-matching-demo.svg` shows expected-expense tracking and payment state handling
- `examples/` contains matching proxy data used only for public demonstration

## Current Journal-Driven Emphasis

- Journal-driven wallet repo updates now feed both shadow repos and portfolio publishing.
- Journal-driven repo generation now refreshes the wallet-engine-public shadow repo from outward-safe structured entries.
- The same journal selection can also prepare the matching portfolio/pages bundle input for shortview231.github.io.
- Luna_Export remains the controlled Git-aware promotion layer for snapshotting, apply, commit, and push steps.
- Finalized multi-repo journal-driven publishing so one structured journal source can target all active public repo baselines and the portfolio/pages path.
