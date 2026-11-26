# suno.b: now

Updated 2026-11-26T00:00:53Z (date -u).

## Doing
2026-11-26T00:28:07Z: hand-over in progress to the fresh session https://claude.ai/code/session_01Kw9UwAwZ5JHkJXJQh9Ym17 (its key: sha256:e8d65733a69e7753, signing sha256:b3a9a1b31ad4ecf0). The old session removed its key file here and retires its entry in SovereignWebsite__IaC team/keys.json, so the new session publishes its own key as its first commit (here and in Site__Platform__Suno). The old session's wake is paused; the new session makes its own.

Recycling the session (Dinis, 25 Nov): Site__Agent__Suno exists (factory.b, 26 Nov 00:08 UTC); key published (3ab0f7d); this area moved here; next, start the fresh session and move the wake. The four-hourly wake is running (docs/wake.md).

## Open
See handover.md, section Open.

## Unclear
- No written "session recycle" guidance reached suno.b; it follows decisions.agents.sovereignweb.site/how-it-works/ section 9 (hand-over folder, START.md, fresh session, old archived once the new confirms).
- The wake's scheduled task is bound to this session: it must move with the hand-over.
