# Source Policy

Provider: X

Policy snapshot: 2026-09-04. Reverify all live conditions before adapter work.

## Planned official surfaces

- read: recent_search
- read: user_timeline
- read: mentions
- read: conversation_lookup
- publication-plan target: post
- publication-plan target: thread
- publication-plan target: reply
- publication-plan target: quote
- publication-plan target: media
- deferred: full_archive_search
- deferred: unbounded_ingestion

## Admission rules

- Official provider APIs and authorized accounts only.
- Every observation records source identity, time, URL, and permission basis.
- Account allowlists and topic allowlists are explicit configuration.
- Rate, quota, cost, retention, deletion, and review obligations fail closed.
- HTML scraping, session-cookie automation, CAPTCHA bypass, and stealth collection are out of scope.
- API success does not establish public visibility or consumer acceptance.

## Current provider boundary

Search depth, quotas, and pricing are plan-dependent. Publication requires user-context authorization; full-archive and unbounded collection remain disabled until explicitly admitted with a cost budget.

Official documentation: https://docs.x.com/x-api/
