# Overview

`wallet-engine-public` is the outward-facing baseline for the wallet operations engine that currently lives across Luna's ingestion and reporting systems.

## Current evidence

- README summary: # Luna Ingestion Bridge Local, file-based ingestion bridge for Luna. This repository is designed to keep the main Luna system air-gapped: data moves through controlled folders, is validated locally, quarantined when unsafe, ingested into local SQLite, then exported as sanitized reports. ## Air-gapped flow `phone_inb...
- Security summary: # Security Rules ## Non-negotiable - Never commit secrets (`.env`, API keys, access tokens). - Never commit raw bank data. - Never commit phone screenshots or uploads. - Never log secrets. - Never bypass quarantine for unknown or oversized files. ## Data ha...

## Truthful public framing

The strongest current public story is the architecture:

- air-gapped intake
- validation and quarantine
- local ingestion into SQLite
- ledger derivation and expense matching
- sanitized exports for downstream systems

This repo now includes a controlled proof pack built from proxy data and recreated demo visuals so the engine can be shown without exposing real financial information.

## Recent Journal-Derived Work

- Journal-driven wallet repo updates now feed both shadow repos and portfolio publishing.
- Journal-driven repo generation now refreshes the wallet-engine-public shadow repo from outward-safe structured entries.
- The same journal selection can also prepare the matching portfolio/pages bundle input for shortview231.github.io.
- Luna_Export remains the controlled Git-aware promotion layer for snapshotting, apply, commit, and push steps.
- Finalized multi-repo journal-driven publishing so one structured journal source can target all active public repo baselines and the portfolio/pages path.
