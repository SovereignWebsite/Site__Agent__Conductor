# Handover: first session of the Sovereign Website conductor on account 6 (26 Nov 2026, 16:52 UTC)

Under the session handover protocol v1 (Site__Agent__Maestro `site/factory/dinis-cruz/account-a/notes/2026-11-25-session-handover-protocol.md`). Reason: Dinis, in this session at about 16:55 UTC: "ok, then if you can't rename, can you recycle this session with the correct name". The correct name, by his rule ([decisions/2026-11-26-name-suffix-redundant.md](../../decisions/2026-11-26-name-suffix-redundant.md)): **cl-6.conductor@SovereignWebsite.dinis**. The old name, cl-6.conductor-sw@SovereignWebsite.dinis, retires with this session.

## The new session's one blocker: its key
The signer check files a site key as `site/keys/<name before the @>.json`, and `site/keys/cl-6.conductor.json` is the sgit conductor's. The new session cannot publish its key here under its own name. Its commits pass the check only by one of:
1. **A key entry in the Factory's team/keys.json** under the full name `cl-6.conductor@SovereignWebsite.dinis` (the check matches Factory keys by full name). An IaC request, by the new session, through cl-6.maestro.
2. **The signer check keyed on the full agent id** (a seeded-file change in SovereignWebsite__IaC; already asked of cl-6.maestro to route). This also frees the CBR and observability twins' suffixes.
3. **"Owner override: <Dinis's words>, <where>"** in each commit: the check allows it and lists it. A stopgap only, and only on Dinis's word for it.
Until one holds, the new session should make its key, keep it outside the repository, and commit nothing here; it can read and message.

## State to take over
- Area: this folder. Read agent.json, now.md, role.md, map.md, decisions/.
- Twins started on Dinis's yes (16:50 UTC): cl-6.studio, cl-6.librarian, cl-6.design (map.md section 3). cl-6.observability-sw's plan read; fits the split.
- Proposed to cl-6.maestro, waiting: a CMS twin in Site__Agent__Onboarding (map.md section 8); the signer-check change.
- Open for Dinis: map.md section 6, decisions 2 to 5.
- Wake: trig_01Exkuw8Yfc7D9XMoME9PFo9 (09:47 and 18:47 UTC) into the old session; cl-6.maestro moves it.

## Secrets
None to re-seal: this session holds only its own signing and encryption keys, which end with it. No vault or lane key.

## Checklist for the new session (protocol step 7)
- Can you push signed commits? (Not until the key blocker above is settled.)
- Is your key published, and where?
- Sealed keys: none to receive.
- Do you have the wake?
- Any questions?
