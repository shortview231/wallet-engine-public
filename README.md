# Wallet Engine Public

Docs-first public baseline for Luna's wallet ingestion and export layer.

This repo is based on the existing `Luna_Ingestion` workspace, which already models a local, air-gapped ingestion bridge for financial and operational data. The public baseline intentionally avoids shipping live data, raw exports, secrets, or personal financial records.

## What exists today

- Local file-based ingestion bridge
- Validation and quarantine model
- SQLite-backed local system of record
- Export/outbox model for downstream reporting
- Explicit security rules around what must never be committed

## What this repo does not include yet

- Live banking data
- Raw CSV imports
- Secrets or `.env` values
- Personal screenshots or uploads
- Automatic inbound cloud services

## Source of truth

The working implementation source lives in `~/Desktop/Projects/Luna_Ingestion`.
