# aoa-x-connector

Policy-gated X evidence and publication-plan connector for AoA.

Phase 0 is an offline, policy-first skeleton. It makes no live API calls,
contains no credentials, and cannot publish content.

## Owned here

- X-specific source policy and capability discovery
- normalized evidence-packet and publication-plan contracts
- provider-specific parsing, preparation, validation, and local decisions
- a fail-closed local CLI and repository validator

## Owned elsewhere

- cross-network campaign orchestration and editorial policy
- live MCP/HTTP composition, scheduling, queues, retries, and secret injection
- final publication authority and operator approval
- heavy captures, media, indexes, and generated corpora

## Current boundary

Search depth, quotas, and pricing are plan-dependent. Publication requires user-context authorization; full-archive and unbounded collection remain disabled until explicitly admitted with a cost budget.

Official documentation: https://docs.x.com/x-api/

API terms, scopes, quotas, review requirements, and pricing can change. Recheck
the official documentation before implementing or admitting a live adapter.

## Bootstrap checks

```bash
python -m pip install -e ".[dev]"
python scripts/validate_connector.py
ruff check .
pytest
aoa-x doctor --json
```

A green bootstrap proves only the source skeleton. It does not prove API access,
OAuth, deployment, publication, or consumer acceptance.
