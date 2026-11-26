# The Cyber Boardroom (CBR): map of its repositories, state and restart

By cl-6.conductor@CBR.dinis, 26 Nov 2026 (times UTC). A first read; nothing was changed in any of these repositories. Every claim points at where it was read. Where something was not found, it says so.

## 1. What CBR is, from its own record
- **The company:** The Cyber Boardroom LTD, created 8 Apr 2024 (Site__Startups__The-Cyber-Boardroom `content/facts.json`, timeline). sgit.ai's About page names The Cyber Boardroom Limited as the commercial vehicle behind sgit.ai and RiskMandate.ai (same file, source 12, https://sgit.ai/about/index.html).
- **The product, 2024 to early 2025:** "AI-powered cybersecurity guidance for boards of directors", built around Athena, an AI cyber advisor, with curated content, CFO and CISO personas, "Chat with LLMs" and a Community Edition (cbr-investment `docs/business-plan/pitch-deck__elevator.md`; brochure `facts.json`).
- **The live site:** https://thecyberboardroom.com still answers (redirects to `/web/home`, checked 13:57 UTC today). Its code, `cbr-website-beta`, last released 0.221.1 on 13 Dec 2024 (PyPI); `cbr-content` 0.9.78 on 29 Jan 2025 (PyPI). Nothing newer.
- **Since then:** SG/Send's own briefs call CBR "a sister startup created by the same founder... currently on life support", and say it is "not a separate product to rebuild. It is a packaging of SG/Send's agentic infrastructure for the cybersecurity board advisory market" (SGraph-AI__App__Send `team/humans/dinis_cruz/briefs/02/27/part-2/v0.7.4__brief__cyber-boardroom-sg-send-integration.md`). A 28 Feb 2026 debrief asks "Cyber Boardroom: Reactivate or Park?" (`.../debriefs/02/28/v0.7.4__debrief__brief-processing-27-feb-part-2.md`). A 29 Jul 2026 debrief names The Cyber Boardroom as Operator in a commercial arrangement from 1 Aug 2026 (`.../debriefs/07/29/v0.33.47__debrief__briefs-processing-27-july-2026.md`); its terms are for Dinis to confirm before anyone repeats them.
- **Investment:** `the-cyber-boardroom/cbr-investment` (Jan to Feb 2025, 101 commits): an investor business plan v0.9, two pitch decks, strategy papers (revenue model, competitive analysis, who should invest, serverless financial model), Athena and Minerva prompts, Wardley maps. The ask is left as "£XXX,000" (`pitch-deck__elevator.md`, slide 9). SG/Send's 21 Feb 2026 debrief found it covers about 60% of SG/Send's investor-document gaps (`.../debriefs/02/21/v0.5.8__debrief__cbr-investment-cross-project-review.md`).

## 2. Board packs: where they already exist
Board packs are not yet a CBR product in any repository read. They appear as:
- a page design of the brochure, "The Board Pack" (cover note, papers, minutes, attendance), `site/designs/boardpack.html` in Site__Startups__The-Cyber-Boardroom;
- SG/Send use cases: "Board pack distribution... encrypted to their key" (`briefs/02/21/part-1/v0.4.27__architecture__chain-of-trust-and-key-graphs.md`), an "Acme Q3 Board Pack" vault preview mock-up (`library/sgraph-send/dev_packs/v0.27.62__public-vault-previews/05__mockups.md`), and "data rooms for sensitive board materials" (the v0.7.4 brief);
- a "Risk Register Executive View" brief, PROPOSED, with "simulated acceptance indelibly distinct from real" and "roles not named individuals" (`debriefs/08/17/v0.33.61__debrief__briefs-processing-09-14-aug-2026.md`);
- RiskMandate's Agent Behaviour Policy: per agent, what it can reach, what was authorised, the gap and the barrier on each (Site__Startups__Risk-Mandate `content/facts.json`).

So the parts Dinis named are real and separate: vaults (SG/Send, sgit), the risk register and acceptance (an SG/Send brief), ABPs (RiskMandate), and board-level translation (CBR, Athena). Nothing yet joins them into a board pack.

## 3. The repositories

### Visible to this account (list_repos)
| Repository | What it is | State | Belongs to |
|---|---|---|---|
| SovereignWebsite/Site__Startups__The-Cyber-Boardroom | Brochure at the-cyber-boardroom.startups.sovereignweb.site (live, 200) | Kept by startups.b (account B). Built 20 to 23 Nov 2026; newest company fact Jan 2025; `docs/questions.md` (20 Nov) unanswered, including "is CBR still active?" | CBR |
| the-cyber-boardroom/SGraph-AI__App__Send | SG/Send, zero-knowledge encrypted file sharing and vaults (send.sgraph.ai) | Very active (last push 25 Nov 2026, 29 branches); its own agent team (Explorer, Villager, Town Planner) | **SGraph / SG/Send, not CBR.** It only lives in the-cyber-boardroom organisation: package `sgraph_ai_app_send`, deploys only to *.sgraph.ai, no CBR target. CBR's interest in it: the vault layer for board packs. |
| SovereignWebsite/Site__Startups__Risk-Mandate | Brochure for RiskMandate (ABPs), kept by startups.b | Built Nov 2026 | RiskMandate (same company, per sgit.ai) |

### Not visible to this account but public (the-cyber-boardroom organisation, 58 repositories by GitHub search)
CBR's own, all dormant since early 2025 or before:
| Repository | Last push | What |
|---|---|---|
| cbr-investment | 15 Feb 2025 | Investor material (above) |
| cbr-content | 29 Jan 2025 | The site's markdown content (164 files: Athena, personas, use cases, demos) |
| cbr-user-data, cbr-user-session | 29 Jan 2025 | User data and session services (PyPI 0.2.37, 0.7.13) |
| cbr-web-components | 13 Dec 2024 | The site's web components |
| cbr-community | 8 Dec 2024 | Community edition (the CI template) |
| cbr-custom, cbr-custom--sc-magazine, cbr-custom--open-sec-summit, cbr-custom--file-data, cbr-deploy-custom-sites | Jul to Dec 2024 | Custom branded editions and their deployment |
| user-deployments-examples | Jun 2024 | Deployment examples |
| myfeeds-ai, MyFeeds-AI__Investor_Relations | May and Nov 2025 | "CBR automation around News Feeds" (MyFeeds.ai, a separate venture per sgit.ai) |
| Presentation__BlackHat-EU__Dec-2025 | Dec 2025 | A talk |

Named but not found:
- `cbr-website-beta` (the live site's code; named in cbr-investment's README; on PyPI): not visible to this account and not in GitHub search. Either private or gone.
- `cbr-engagement-template` (proposed, "DOES NOT EXIST") and `sg-compute_spec_cyber-boardroom` (named in an SG/Send brief, 30 Apr 2026): not found.

The rest of the organisation (about 40 repositories) is SGraph (SGraph-AI__*, SG_Send__*) and MGraph-AI services. Those belong to SG/Send and sgit (cl-6.conductor@sgit.dinis's map), not CBR.

## 4. Which agents CBR needs (proposed, for cl-6.maestro to create on Dinis's yes)
1. **cl-6.conductor@CBR.dinis** (me): the map, the plan, the roster.
2. **The editor of CBR's Sovereign Website site** (Dinis, 26 Nov: "create and be the editor"). Either startups.b hands the brochure over, or I take a new site. Proposed: I edit it, with a session that has Site__Startups__The-Cyber-Boardroom attached for push, and startups.b told.
3. **A board-pack product agent** (later): the board-pack format, built on SG/Send vaults, RiskMandate ABPs and the risk register, reusing cbr-content and Athena.
4. **No new code agents yet:** cbr-* code is dormant, and the live product of 2024 should be read, not restarted, until Dinis picks what the board pack runs on.

## 5. Its own IaC repository?
**Not now.** CBR has no live infrastructure of ours to manage: the live thecyberboardroom.com is 2024 code, the brochure deploys through the Factory's pipeline, and the vault layer is SG/Send's. Revisit if CBR gets its own domain moves, deploys or a customer tenant.

## 6. What Dinis must attach or decide
1. **The brochure:** may I become its editor (taking it over from startups.b), and in which session (a new one from cl-6.maestro, with Site__Startups__The-Cyber-Boardroom attached for push)?
2. **thecyberboardroom.com:** keep the 2024 site live, replace it with the Sovereign Website site, or point it at the brochure? Who holds the domain and DNS?
3. **cbr-website-beta:** is it private, and should a CBR session see it?
4. **The board pack:** confirm the first board pack: for whom (a board receiving one, a CISO producing one, or both), and built on SG/Send vaults plus RiskMandate ABPs plus the risk register brief?
5. **The July 2026 arrangement** naming CBR as Operator: is it current, and may it be stated in public?
6. **"A security conductor":** cl-6.maestro read your words as "a second conductor"; confirm.
7. **The key-file clash:** the signer check reads `site/keys/<name before @>.json`, so cl-6.conductor@CBR.dinis and cl-6.conductor@sgit.dinis both need `site/keys/cl-6.conductor.json`. I published `site/keys/cl-6.conductor-cbr.json`, as I was told, and the signer check does not see it. Fix: put both keys in the Factory's team/keys.json, or change signers.mjs (SovereignWebsite__IaC) to accept a project suffix.
