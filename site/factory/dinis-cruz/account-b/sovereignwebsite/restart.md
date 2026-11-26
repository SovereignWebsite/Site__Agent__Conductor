# b.conductor: restart

For a fresh conductor.b session. Read in this order:
1. This repository's START.md and CLAUDE.md, then SovereignWebsite__IaC CLAUDE.md and policy/abp.json.
2. This area: agent.json, role.md, now.md.
3. SovereignWebsite__IaC board/conductor.b/restart.md and the state note it names, then status.json.

Then:
1. Make your key (START.md step 1, or SovereignWebsite__IaC board/workflow/2026-11-20__signing-with-your-key.md). If the session refuses the step that writes the signing file, stop and put it to Dinis: see board/incidents/2026-11-26__signing-key-step-refused.md in SovereignWebsite__IaC.
2. Ask the old session to retire its entry in SovereignWebsite__IaC team/keys.json; publish yours there in one commit that adds only your entry.
3. Update agent.json and now.md here, and SovereignWebsite__IaC board/conductor.b/agent.json.
4. Tell decisions.b and b.maestro the new session, by link to agent.json.
5. Carry on from status.json's asks and next. Hand over before about 300k context.
