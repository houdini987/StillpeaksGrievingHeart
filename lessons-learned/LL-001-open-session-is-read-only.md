# LL-001 — OPEN SESSION must be read-only

## Context

Early iterations allowed OPEN SESSION to potentially create or modify files.

## Gotcha / Failure Mode

Opening a session could accidentally create new session logs or mutate state, breaking session sequencing and introducing drift.

## Rule Going Forward

OPEN SESSION must be strictly read-only and perform only repo scanning, validation, and inference.

## Applies To

- DM Runtime Project

## Related Files

- bootstrap/SESSION_PROTOCOL.md
