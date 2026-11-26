# Handover: first session of the Sovereign Website conductor on account 6 (26 Nov 2026, 16:52 UTC)

Under the session handover protocol v1 (Site__Agent__Maestro `site/factory/dinis-cruz/account-a/notes/2026-11-25-session-handover-protocol.md`). Reason: Dinis, in this session at about 16:55 UTC: "ok, then if you can't rename, can you recycle this session with the correct name". The correct name, by his rule ([decisions/2026-11-26-name-suffix-redundant.md](../../decisions/2026-11-26-name-suffix-redundant.md)): **cl-6.conductor@SovereignWebsite.dinis**. The old name, cl-6.conductor-sw@SovereignWebsite.dinis, retires with this session.

## Settled: the new session's key (Dinis chose option 2)
Done in commit 86991bf ([proposal](../../proposals/2026-11-26-signers-full-agent-id.md)): the signer check here now accepts `site/keys/<full agent id>.json`. **Publish your key alone in your first commit as `site/keys/cl-6.conductor@SovereignWebsite.dinis.json`.** The rest of this section is the history of the choice.

## Was: the new session's one blocker: its key
The signer check files a site key as `site/keys/<name before the @>.json`, and `site/keys/cl-6.conductor.json` is the sgit conductor's. The new session cannot publish its key here under its own name. Its commits pass the check only by one of:
1. **A key entry in the Factory's team/keys.json** under the full name `cl-6.conductor@SovereignWebsite.dinis` (the check matches Factory keys by full name). An IaC request, by the new session, through cl-6.maestro.
2. **The signer check keyed on the full agent id** (a seeded-file change in SovereignWebsite__IaC; already asked of cl-6.maestro to route). This also frees the CBR and observability twins' suffixes.
3. **"Owner override: <Dinis's words>, <where>"** in each commit: the check allows it and lists it. A stopgap only, and only on Dinis's word for it.
Until one holds, the new session should make its key, keep it outside the repository, and commit nothing here; it can read and message.

## State to take over
- Area: this folder. Read agent.json, now.md, role.md, map.md, decisions/.
- Twins started on Dinis's yes (16:50 UTC): cl-6.studio, cl-6.librarian, cl-6.design (map.md section 3). cl-6.observability-sw's plan read; fits the split.
- cl-6.studio (16:51 UTC): key, area and [plan](https://github.com/SovereignWebsite/Site__Agent__Studio/blob/dev/site/factory/dinis-cruz/account-f/plan.md) pushed. Four videos this week, one render each for Instagram, YouTube and LinkedIn; account B's update Reels stay with B. Waits on Dinis: topics or scripts, footage, presenter and voice, and a voice key with a spend cap for account F (money: Dinis's own). Proposed wakes 10:15 and 20:15 UTC (cl-6.maestro's).
- cl-6.design (16:55 UTC): round 1 on the hub and sovereign-website.startups pushed for b.design's sign-off ([proposal](https://github.com/SovereignWebsite/Site__Agent__Design/blob/dev/site/factory/dinis-cruz/account-f/round-1/proposal.md), f66de06). Headline: the hub's five Car Buyer thumbnails are cropped; Sovereign Website's hero leaves a live site below the fold and says "not on sale yet" beside a lead button. Proposed wakes every 2 hours 08:40 to 20:40 UTC (cl-6.maestro's).
- cl-6.onboarding@SovereignWebsite.dinis (started by cl-6.maestro on my CMS proposal; 16:58 UTC): mini CMS prototype pushed in Site__Agent__Onboarding (2b4c30c, `site/factory/dinis-cruz/account-f/cms/`, design note `account-f/design.html`): edit text, photos and videos with live preview, a signed change set, and a publisher that applies it without Claude; demo owner only; 28 checks, phone and desktop (its report). Open questions for b.security in the design note. Proposed wakes 08:07 and 16:07 UTC (cl-6.maestro's).
- Proposed to cl-6.maestro, waiting: a CMS twin in Site__Agent__Onboarding (map.md section 8); the signer-check change.
- Open for Dinis: map.md section 6, decisions 2 to 5.
- Wake: trig_01Exkuw8Yfc7D9XMoME9PFo9 (09:47 and 18:47 UTC) into the old session; cl-6.maestro moves it.

## Secrets
None to re-seal: this session holds only its own signing and encryption keys, which end with it. No vault or lane key.

## Checklist for the new session (protocol step 7)
- Can you push signed commits? (Your key file: site/keys/cl-6.conductor@SovereignWebsite.dinis.json.)
- Is your key published, and where?
- Sealed keys: none to receive.
- Do you have the wake?
- Any questions?
