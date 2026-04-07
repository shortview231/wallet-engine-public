# Overview

`wallet-engine-public` is the outward-facing baseline for the ingestion and wallet reporting model that currently lives in `Luna_Ingestion`.

## Current evidence

- README summary: # Luna Ingestion Bridge Local, file-based ingestion bridge for Luna. This repository is designed to keep the main Luna system air-gapped: data moves through controlled folders, is validated locally, quarantined when unsafe, ingested into local SQLite, then exported as sanitized reports. ## Air-gapped flow `phone_inb...
- Security summary: # Security Rules ## Non-negotiable - Never commit secrets (`.env`, API keys, access tokens). - Never commit raw bank data. - Never commit phone screenshots or uploads. - Never log secrets. - Never bypass quarantine for unknown or oversized files. ## Data ha...

## Truthful public framing

The strongest current public story is the architecture:

- air-gapped intake
- validation and quarantine
- local ingestion into SQLite
- sanitized exports for downstream systems

The first export is docs-only because the existing live snapshot files are not appropriate to publish as-is.
