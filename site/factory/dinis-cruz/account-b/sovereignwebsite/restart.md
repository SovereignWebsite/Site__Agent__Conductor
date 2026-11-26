# b.conductor: restart

For a fresh conductor.b session. Read in this order:
1. This repository's START.md and CLAUDE.md, then SovereignWebsite__IaC CLAUDE.md and policy/abp.json.
2. This area: agent.json, role.md, now.md.
3. SovereignWebsite__IaC board/conductor.b/restart.md and the state note it names, then status.json.

Then:
1. Make your key in SovereignWebsite__IaC, as its board/conductor.b/restart.md step 1 says (run `bash seed/site-template/tools/setup-signing.sh` there; do not type the key steps by hand). conductor.b's key lives in IaC team/keys.json, so do not publish a site/keys/ file here: wire this clone with the same four git settings (`gpg.format ssh`, `user.signingkey ~/.sw-secret/signing`, `commit.gpgsign true`, `gpg.ssh.program ssh-keygen`). If the session refuses the script, stop and put it to Dinis (IaC board/incidents/2026-11-26__signing-key-step-refused.md).
2. Ask the old session to retire its entry in SovereignWebsite__IaC team/keys.json; publish yours there in one commit that adds only your entry.
3. Update agent.json and now.md here, and SovereignWebsite__IaC board/conductor.b/agent.json.
4. Tell decisions.b and b.maestro the new session, by link to agent.json.
5. Carry on from status.json's asks and next. Hand over before about 300k context.
