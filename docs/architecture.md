# Architecture

## Current system shape

The working implementation is a local ingestion bridge centered on a controlled file flow:

`phone_inbox -> luna_inbox/inbox -> validate -> (approved | quarantine) -> ingest -> sqlite -> export -> luna_outbox -> phone_outbox`

## Existing implementation truths

- The bridge is designed to keep the main Luna system air-gapped
- Unknown or oversized files are quarantined
- Approved inputs are ingested locally
- Exported outputs are intended to move outward as sanitized reports
- Security rules are already documented and strict about what must never be committed

## Public baseline boundary

This public repo should document the engine and its security model without shipping live datasets. Any future examples must come from separately prepared demo-safe artifacts.
