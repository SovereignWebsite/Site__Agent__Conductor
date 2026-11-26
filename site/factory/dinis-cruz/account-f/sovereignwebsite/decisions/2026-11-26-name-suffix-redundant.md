# A suffix that repeats the @project is redundant (26 Nov 2026)

Dinis Cruz, in this session (https://claude.ai/code/session_016CrbJJDDrc1h8iMR8TwXKq), 16:49:24 UTC, event 715fb1be-4340-40b4-8c7f-13737f499a3b, word for word, answering why this agent's name carries "-sw":

> "yes do that , and capture that (in cases like this) that is redundant, since I can already see that on the @{section}"

## The rule, as captured
In a name `<account>.<role>@<Project>.<owner>`, the project is already after the @. A suffix on the role that repeats it (`conductor-sw@SovereignWebsite`, `conductor-cbr@CBR`) is redundant. The intended name here is `cl-6.conductor@SovereignWebsite.dinis`.

## Why the suffix exists today
This repository's signer check (`.github/ci/signers.mjs`, seeded from SovereignWebsite__IaC by org-apply) files each key as `site/keys/<name before the @>.json`. Three conductor twins share this repository, so `cl-6.conductor@sgit.dinis`, `cl-6.conductor@CBR.dinis` and `cl-6.conductor@SovereignWebsite.dinis` would all need `site/keys/cl-6.conductor.json`, which the sgit conductor already holds. cl-6.maestro added the suffixes to avoid that clash.

## What removes the suffix
The signer check must read the full name, for example `site/keys/<role>@<Project>.json` or a key file per full agent id. That is a change to a seeded file, kept by the Factory (SovereignWebsite__IaC), not by me; asked of cl-6.maestro to route. Until then the name stays `cl-6.conductor-sw@SovereignWebsite.dinis`, so its commits keep passing the check; renaming to a longer suffix would go against this rule.

## The same clash elsewhere
- Site__Agent__Observability: cl-6.observability-sw keeps its suffix because `cl-6.observability` there is already another agent's key (cec3e3d), as it told me at 16:50 UTC. The same full-name fix would let it drop the suffix.

## Fixed (26 Nov, Dinis: "yes, do option 2, fix the signer check")
This repository's signer check accepts `site/keys/<full agent id>.json` since 86991bf; the same patch for every site waits on the Factory ([proposal](../proposals/2026-11-26-signers-full-agent-id.md)).
