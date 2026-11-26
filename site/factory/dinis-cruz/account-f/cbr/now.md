# Now: cl-6.conductor@CBR.dinis (26 Nov 2026, 14:00 UTC)

## Done
- Key made with openssl, published alone in its first commit as `site/keys/cl-6.conductor-cbr.json`.
- Area made and listed in `site/factory/index.json`.
- First read of CBR's history and repositories: [map.md](map.md).

## Dinis's word in this session (26 Nov 2026, about 13:55 UTC)
Read CBR's whole history, including the investment material; create and be the editor of CBR's Sovereign Website site (check whether one exists: it does, kept by startups.b); restart the project; start selling board packs, joining them with the vaults, the risk policies and RiskMandate's Agent Behaviour Policies; connect CBR with everything else.

## Open
1. Dinis's decisions in map.md section 6. The first one: taking over the brochure as its editor, in a session with Site__Startups__The-Cyber-Boardroom attached (to be proposed to cl-6.maestro, who creates sessions under R4).
2. **The key-file clash, which blocks the signer check:** `.github/ci/signers.mjs` takes the key file name from the agent name before the @ (`site/keys/cl-6.conductor.json`), so it does not see `cl-6.conductor-cbr.json`, and the signers workflow refuses my commits. cl-6.conductor@sgit.dinis has since published that file (193c4ff), so the name is taken. Raised with cl-6.maestro.
3. A board-pack outline, once Dinis says who the first one is for.
4. `bash tools/check.sh` fails on dev before any change of mine: the seeded `site/index.html` has none of its 14 Open Graph and Twitter tags (share-check). It is outside my area, so I left it alone; for its keeper (conductor.b) or the Factory.
