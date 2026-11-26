# Now: cl-6.conductor-cbr@CBR.dinis (26 Nov 2026, 16:40 UTC)

Started as cl-6.conductor@CBR.dinis; named cl-6.conductor-cbr@CBR.dinis in this repository by cl-6.maestro (13:59 UTC), so the signer check finds my key.

## Dinis's words in this session
- **About 13:55 UTC:** read CBR's whole history, including the investment material; create and be the editor of CBR's Sovereign Website site; restart the project; start selling board packs, joining them with the vaults, the risk policies and RiskMandate's Agent Behaviour Policies; connect CBR with everything else.
- **About 14:05 UTC:** "take that brochure and go to town on it"; build it as the replacement for the main URL (thecyberboardroom.com), which he controls; "all of this is public"; The Cyber Boardroom is the legal entity underneath, so the about page should connect the dots.
- **About 14:20 UTC:** it is fine to create new repositories from the cyber-boardroom ones, since they can be moved later. (His message was cut off after that.)

## Done
- Key published here (894c46d) and in Site__Startups__The-Cyber-Boardroom (a6a08de).
- [map.md](map.md) of CBR's repositories.
- **Editor of Site__Startups__The-Cyber-Boardroom** (attached to this session for push at Dinis's word). New main pages built from `content/cbr.json` by `tools/cbr_site.py`: home, /board-packs/, /about/ (The Cyber Boardroom Limited, Companies House 15623827, and how sgit.ai, RiskMandate.ai and SG/Send connect), /history/, /athena/. The five earlier designs stay under /designs/. All checks pass (6c47722).

## Open
1. **Moving thecyberboardroom.com here:** Dinis controls the domain. When he says go: change `host` in `content/cbr.json` and `site/CNAME`, rebuild, then he points DNS at GitHub Pages. Until then, the 2024 platform stays live there.
2. **startups.b** (account B) built the brochure and keeps the shared kit (`tools/build.py`, `tools/designs2.py`); told through cl-6.maestro that I am now its editor.
3. **New repositories from the cyber-boardroom ones** (Dinis allows it): none made yet. Candidates once the board pack is defined: a board-pack spec and template repository. New repositories go through the Factory (SovereignWebsite__IaC `requests/`) or cl-6.maestro.
4. The board pack's first outline is on /board-packs/, labelled as a proposal. It still needs Dinis's view on who the first pack is for.
5. `tools/check.sh` here fails only on this repository's own site/index.html (no Open Graph tags; predates me; not my area).
