# sgit: map of the project's repositories and sessions

By cl-6.conductor@sgit.dinis. First version 26 Nov 2026, 13:57 UTC; revised 15:55 UTC to add account 6's older sgit sessions (cl-6.maestro's ask) and the 17 site repositories those sessions revealed. First piece of work, before changing anything: nothing below has been changed by me. Every fact comes from a repository, PyPI, a public page or a session's own record (title, repositories, status, its one-line summary), read on the day; no transcript was read. Revised again 27 Nov, 01:36 UTC, with the two new sessions, and at 01:37 UTC: SGit-AI is read only from account 6. What I could not see is marked so.

## How I looked

- `list_repos` on account 6 (queries: sgit, sgraph, send, vault, cyber-boardroom), and the full list.
- The project's own public pages: https://sgit.ai/llms.txt, https://sgit.ai/llms-full.txt (every page of the site in one file), https://sgit.ai/.well-known/sgit-agents.json, https://newsroom.sgit.ai/llms.txt, and the PyPI record for `sgit-ai` (https://pypi.org/project/sgit-ai/).
- `git ls-remote` and a shallow, read-only clone of each public repository found (default branch only).
- `list_sessions` and `get_session` (metadata only) for account 6's sessions from August to October 2026 whose titles or repositories are sgit's; costs from cl-6.accountant's analysis: https://github.com/SovereignWebsite/Site__Agent__Accountant/blob/dev/site/factory/dinis-cruz/account-f/analysis.md

## The short version

- **The code is `SGit-AI/SGit-AI__CLI`** (PyPI names it as the repository). It is public but not attached to account 6, so I can read it and cannot push to it.
- **The project is its own GitHub organisation, `SGit-AI`**, with at least **24 public repositories**: the CLI, sgit.ai, the newsroom and its API, and 20 more sites under *.sgit.ai. None is visible to account 6 through `list_repos`, yet **26 older sessions on account 6 worked on them** (August to October, about $1,346 in all), so the account had access then and does not list it now.
- **One repository it depends on is visible here:** `the-cyber-boardroom/SGraph-AI__App__Send` (the SG/Send server sgit speaks to). Since 27 Nov it has its own conductor, cl-6.conductor@SGSend.dinis (below).
- **Nothing in the sgit repositories follows the current way yet**: no per-agent keys, no `Agent:` trailers, work on `claude/*` branches, and no agent areas, with one exception: the newsroom, whose agents keep areas (below).
- **One rule clash to settle first:** in SGit-AI__CLI a push to dev publishes a pre-release to PyPI. "Dev only" there still ships a package.
- **None of the 26 older sessions needs to keep running.** Two should wait for an answer and four have open items to hand over (below); the other 20 can be archived once Dinis agrees.

## Repositories

### Visible to account 6 (can push)

| Repository | What it is | State on 26 Nov 2026 |
|---|---|---|
| SovereignWebsite/Site__Startups__Sgit | The independent brochure at sgit.startups.sovereignweb.site, made from sgit's public pages. Kept by startups.b on account B. Not the project. | dev last moved 25 Nov (Factory org-apply refreshes). Already on the current way (CLAUDE.md, signed keys, dev only). Its facts.json stops at 28 Oct 2026 (0.27.0). |
| the-cyber-boardroom/SGraph-AI__App__Send | SG/Send: the zero-knowledge storage and transfer API (Python) and its web UIs (SG/Vault, share, admin, workspace). sgit's default server is `dev.send.sgraph.ai`. | Active: dev last commit 25 Nov 2026 21:24 UTC; 28 branches, many `claude/*`. Commits carry `Claude-Session:` but no `Agent:` trailer and no per-agent key. Has its own `team/` folder of role files. |
| SovereignWebsite/SovereignWebsite__Vault, Site__Agent__Vault-Keeper | Names match "vault"; they are SovereignWebsite's own, not sgit's. | Not part of sgit as far as I can tell; listed so nobody else wonders. |

### SGit-AI: the core (public, not attached to account 6)

| Repository | What it is | State |
|---|---|---|
| SGit-AI/SGit-AI__CLI | **The sgit code**: package `sgit-ai`, Python 3.11+, Apache-2.0, author "The Cyber Boardroom" on PyPI. | dev last commit 15 Nov 2026; dev carries v0.27.1, PyPI's latest release is 0.27.0 (28 Oct). 19 branches, mostly `claude/*`. CI: a dev push publishes a PyPI pre-release; a main push publishes the release and to Docker Hub. Has CLAUDE.md (Type_Safe rules), `team/` (assessment, decisions, explorer, humans, villager), `review/`, `_to_review/`. |
| SGit-AI/SGit-AI__Website | sgit.ai, the official documentation site, itself served from a vault. | dev last commit 13 Oct 2026 (site v0.7.87, "the newsroom has moved"). Pages deploy from dev. |
| SGit-AI/SGit-AI__Website__Newsroom | newsroom.sgit.ai, the SGit Newsroom. | **The most active**: last commit 24 Nov 2026 (site v0.14.214). Its agents already keep areas: the last commit is "d.newsroom (writer-11) keeps its area current: agent.json, now.md, role.md". So it is already being retrofitted, apparently from account D. |
| SGit-AI/SGit-AI__Website__Newsroom__API | api.newsroom.sgit.ai, the newsroom's API site. | dev last commit 17 Oct 2026. |

### SGit-AI: the other sites (public, not attached to account 6)

| Repository | Address | dev last commit |
|---|---|---|
| SGit-AI__Website__PKI | pki.sgit.ai | 23 Nov 2026 (v0.2.36); the only one of these still moving |
| SGit-AI__Website__Ruv | (no CNAME file) | 21 Oct 2026 (v0.2.0, "the service site") |
| SGit-AI__Website__Secrets | secrets.sgit.ai | 6 Oct 2026 (v0.1.13) |
| SGit-AI__Website__ABP | abp.sgit.ai | 4 Oct 2026 (v0.12.1); the session calls it "(RiskMandate)" |
| SGit-AI__Website__Graphs | graphs.sgit.ai | 20 Sep 2026 (v0.6.22) |
| SGit-AI__Website__Store | (no CNAME file) | 17 Sep 2026 (v0.3.24) |
| SGit-AI__Website__Chrome-Extensions | chrome-extensions.sgit.ai | 9 Sep 2026 (v0.1.0) |
| SGit-AI__Website__Teams | teams.sgit.ai | 8 Sep 2026 (v0.1.0) |
| SGit-AI__Website__Threat-Modeling | threat-modeling.sgit.ai | 8 Sep 2026 (v0.1.0) |
| SGit-AI__Website__Open-Source | open-source.sgit.ai | 6 Sep 2026 (v0.2.2) |
| SGit-AI__Website__Skills | skills.sgit.ai | 26 Aug 2026 (v0.1.0) |
| SGit-AI__Website__Twins, __NFRs, __LLMs, __Coding, __SG-Compute, __Standards | twins, nfrs, llms, coding, sg-compute, standards .sgit.ai | 25 Aug 2026 (v0.1.x to v0.2.0) |
| SGit-AI__Website__Infographics | infographics.sgit.ai | 24 Aug 2026 (v0.1.0) |
| SGit-AI__Website__NHI | nhi.sgit.ai | 19 Aug 2026 (v0.1.19) |
| SGit-AI__Website__SG_Sentinel | sg-sentinel.sgit.ai; the site says SG/Sentinel is a May 2026 design, not built | 20 Aug 2026 (v0.1.1) |

So 19 of the 20 have not moved for five weeks or more. sgit.ai names a few more subdomains (risks, wardley-maps, issues-fs, subscriptions, providers, games and others) whose repositories I have not found; some may be vaults served as apps.

### Named by the project's pages, not public (or not existing)

`SGit-AI/SGit-AI__Newsroom__API` (a villager brief names it; probably an older name for SGit-AI__Website__Newsroom__API, which is public), `SGit-AI/SGit-AI__SG-Meter` (the reading meter), `SGit-AI/SGit-AI__Reader`, `SGit-AI/SGit-AI__Newsroom__Reader`, and `SGraph-AI__Tools` (owner not stated). I cannot tell private from absent without access.

## Account 6's older sgit sessions (August to October 2026)

26 sessions, all idle, none running. "Status" and "last said" are the session's own record; cost from cl-6.accountant. My recommendation per session, for Dinis: **archive** (nothing left in it), **hand over** (its open item goes to the team member named, as a note in their brief; the old session is then archived, never continued, since none has a key or an area), or **keep for now** (holds something not yet safe elsewhere).

### The code

| Session | Repositories | Status, last said | Cost | Recommendation |
|---|---|---|---|---|
| sgit-ai cli / security review (11 to 13 Oct) | SGit-AI__CLI, sgit-ai__website__threat-modeling | blocked: "4 reported bugs fixed with attack tests, coverage 89% to 90%"; needs "the Anthropic key for the AI gate, then push this branch to dev". Branch `claude/youthful-feynman-bpunv5` is on GitHub. | $191.89 | **Hand over** to the CLI dev: review and merge that branch to dev under the new rules. The AI gate's key is a credential for Dinis to give the new session, never this one. Then archive. |

### sgit.ai

| Session | Repositories | Status, last said | Cost | Recommendation |
|---|---|---|---|---|
| sgit.ai / add vaults (22 to 24 Aug) | SGit-AI__Website | review ready: a new vault with BBC and DuckDuckGo scripts, "tokens/IPs/hostnames stripped"; branch `claude/site-access-branch-commit-6h2bix` | $85.56 | **Hand over** to the sgit.ai keeper: check whether the branch was merged; then archive. |
| sgit.ai / fable / website refactor (11 Oct) | SGit-AI__Website | completed: transition brief and 54-page mapping drafted; "seven decisions and 0.19 to 0.21 changelog pending" | $12.76 | **Hand over** the seven decisions to the sgit.ai keeper (they may be Dinis's); then archive. |

### The newsroom (8 sessions)

| Session | Repositories | Status, last said | Cost |
|---|---|---|---|
| newsroom.sgit.ai (22 to 24 Aug) | Website__Newsroom | review ready: CSS gutter fix, 3 defects flagged | $50.23 |
| @newsroom.vault (13 to 17 Oct) | Website__Newsroom | completed: vault viewer and debrief live; "test_wire red on dev" | $88.81 |
| newsroom.sgit.ai / industry wire (13 to 16 Oct) | Website__Newsroom | review ready: "Wire published nothing; agent rechecks in 45m" | $168.13 |
| api.newsroom.sgit.ai (13 to 17 Oct) | Website__Newsroom, Website__Newsroom__API | completed: API article and figures, 15 tests passed | $130.77 |
| @newsroom.ux (13 to 18 Oct) | Website__Newsroom, Website__Newsroom__API | completed: reading-progress line shipped, v0.12.110 | $187.64 |
| newsroom.sgit.ai / write article (13 to 14 Oct) | Website__Newsroom | completed: branch level with dev at v0.12.40 | $21.93 |
| @newsroom.accountant: the wires' run costs (16 Oct to **26 Nov 07:40 UTC**) | Website__Newsroom | **failed**: hit the 5-hour limit; its record says **unpushed work**. A child of the industry wire session. | $84.05 |
| (the newsroom's own agents now, d.newsroom and its writers, appear to run on account D, not here) | | | |

Recommendation: **archive** the first six (all done; the newsroom has moved on to v0.14.214 since). **Keep for now** @newsroom.accountant, the only one of the 26 active this month: its unpushed work should be recovered, or declared disposable, by whoever keeps the newsroom (Dinis's answer to question 4 below), before it is archived.

### The other sites (14 sessions)

| Session | Repository | Status, last said | Cost | Recommendation |
|---|---|---|---|---|
| ruv.sgit.ai (14 to 15 Oct) | Website__Ruv | completed: "live and verified"; "vault CI jobs need three repo secrets added" | $21.47 | Archive; the three secrets are an item for Dinis (listed below). |
| abp.sgit.ai website (RiskMandate) (11 to 12 Sep) | Website__ABP | review ready: ontology graph rebuild, 11 edges proposed | $46.33 | **Keep for now**: ask Dinis whether abp.sgit.ai is sgit's or RiskMandate's, and whether the 11 edges matter. |
| Store.sgit.ai website setup (10 Sep) | Website__Store | completed: repository and CI created | $15.75 | Archive. |
| Chrome extensions website setup (9 Sep) | Website__Chrome-Extensions | completed: live, v0.1.0 | $7.39 | Archive. |
| teams.sgit.ai (8 Sep) | Website__Teams | completed: live | $10.23 | Archive. |
| threat-modeling.sgit.ai (8 to 9 Sep) | Website__Threat-Modeling | blocked: waiting for feedback on the next round | $9.62 | Archive; the next round, if wanted, to the small-sites keeper. |
| open-source.sgit.ai (24 to 25 Aug) | Website__Open-Source | blocked: licence question | $27.61 | Archive: the repository's dev shows it answered on 6 Sep ("CC BY across everything written"). |
| twins.sgit.ai website setup (25 Aug) | Website__Twins | review ready: 12 pages | $16.38 | Archive. |
| nfrs.sgit.ai website setup (25 Aug) | Website__NFRs | review ready: 26 pages, 3 judgment calls flagged | $15.60 | Archive; the 3 calls to the small-sites keeper. |
| skills.sgit.ai (25 to 26 Aug) | Website__Skills | review ready: v0.1.0 | $13.66 | Archive. |
| llms.sgit.ai (24 to 26 Aug) | Website__LLMs | review ready: "Phase 4: vault holds token refs, not raw keys; not yet shipped" | $38.49 | Hand over phase 4 to the small-sites keeper; then archive. |
| coding.sgit.ai (24 to 25 Aug) | Website__Coding | blocked: deploy failed, "check Settings, Pages, source GitHub Actions" | $12.97 | Archive; whether coding.sgit.ai is live is for the small-sites keeper to check. |
| sg-compute.sgit.ai (24 Aug) | Website__SG-Compute | review ready: five open items flagged | $23.94 | Archive; the five items to the small-sites keeper. |
| standards.sgit.ai (24 to 25 Aug) | Website__Standards | review ready: v0.1.4 pushed | $53.95 | Archive. |
| Infographic catalogue site (23 to 24 Aug) | Website__Infographics | blocked: waiting for a PNG to be pushed | $9.57 | Archive; the PNG to the small-sites keeper. |
| Vault concepts and usage review (22 Aug) | Website__Graphs | review ready: a reading of two vaults | $1.20 | Archive. |

(The April to May "SG/..." sessions, SG/Send, SG/Vault, SG/Compute and others, are SG/Send's history, not sgit's: for cl-6.conductor@SGSend.dinis.)

## The team now (27 Nov 2026, 01:36 UTC)

Two sessions created by cl-6.maestro at Dinis's word (cl-6.maestro's message, 01:37 UTC on 27 Nov), both checked by their session records:

| Agent | Session | Repository attached | Reports to | State at 01:36 UTC |
|---|---|---|---|---|
| cl-6.website@sgit.dinis | session_016CrbJJBxxMtZtCXzFBB9Nf | SGit-AI/SGit-AI__Website | me | started 01:36 UTC; **blocked**: read only, push refused (403); no key, no area, nothing changed. Its clone: dev at v0.7.87 (4e00434) |
| cl-6.conductor@SGSend.dinis | session_016CrbJL9HXMutDbCSwhPb6o | the-cyber-boardroom/SGraph-AI__App__Send (dev) | Dinis, through cl-6.maestro; a peer, not part of this team | started 01:33 UTC, working; leads a project on the API the vaults use |

So item 3 below is filled (but blocked until SGit-AI is writable), and SG/Send (item 6, question 5) has its own conductor. What sgit needs from the SG/Send API goes to cl-6.conductor@SGSend.dinis as a request, never as a change in its repository.

## Which agents it needs (proposal)

A team under this area, `site/factory/dinis-cruz/account-f/sgit/<role>/`, each in its own session created by cl-6.maestro (rule R4):

1. **cl-6.conductor@sgit** (me): the map, the retrofit plan, routing; no code.
2. **a dev for SGit-AI__CLI**: the code, tests and releases; first task, the security-review branch above. First of the team, because the PyPI-on-dev rule must be settled before any agent pushes there.
3. **a keeper for sgit.ai** (SGit-AI__Website): **started as cl-6.website@sgit.dinis** on 27 Nov. The agents' main entry point, not moved since 13 Oct; first tasks, the two handovers above (the add-vaults branch and the refactor's seven decisions).
4. **one keeper for the other 20 sites** while they are quiet, not one each: first tasks, the handovers above, then which sites stay live.
5. **the newsroom** (Website__Newsroom and its API): already has agents (d.newsroom and its writers). I propose leaving it with them and only linking it from here, unless Dinis wants it moved to account 6.
6. **SG/Send** (SGraph-AI__App__Send): **settled**: it has its own conductor, cl-6.conductor@SGSend.dinis; sgit's needs are sent there.

The existing `team/` folders in SGit-AI__CLI and SGraph-AI__App__Send (explorer, villager, librarian and others) are an older role set; the retrofit should say what happens to them rather than run two systems side by side.

## Does sgit need its own IaC repository?

My view, firmer now that I can see 24 repositories: **not yet, but probably later**. Today the org-level things (repositories, keys, Pages settings) can go through SovereignWebsite__IaC as for other projects, and the project's history can live in the agents' homes here. But sgit is its own GitHub organisation with 24 public repositories, many with the same CI, Pages and auto-tag pipeline, plus release secrets (PyPI, Docker Hub) that SovereignWebsite__IaC does not manage. Once the CLI's release pipeline and a first site are under the new way, an SGit-AI IaC repository to seed and refresh them all would earn its keep. Dinis's call.

## What Dinis must attach or decide

1. **Attach SGit-AI__CLI** (and, when their keepers start, the sites; SGit-AI__Website is now attached to cl-6.website@sgit.dinis) to account 6 in new sessions created by cl-6.maestro, not to mine. On 26 Nov `list_repos` showed nothing of the SGit-AI organisation. Attaching SGit-AI__Website on 27 Nov gave **read access only**: cl-6.website's `git push --dry-run` to dev at 01:36 UTC got 403 (the Claude GitHub App has no access to that repository). So **nothing in SGit-AI is writable from account 6** until Dinis installs the Claude GitHub App on the SGit-AI organisation or reconnects GitHub; a session may then need restarting for fresh credentials. A CLI dev session would be blocked the same way.
2. **Dev publishes to PyPI**: keep it (a dev push is a pre-release), or change the CLI's pipeline so only a release step publishes.
3. **The security review's AI gate** needs an Anthropic key; give it to the CLI dev's session as a credential, or drop the gate.
4. **The newsroom**: stays with its current agents (apparently account D), or comes under this conductor. Either way, someone must recover or discard @newsroom.accountant's unpushed work.
5. **SG/Send**: answered on 27 Nov: its own conductor, cl-6.conductor@SGSend.dinis.
6. **An IaC repository for SGit-AI**: yes or no (my view above).
7. **Private repositories**: whether SGit-AI__SG-Meter, Reader, Newsroom__Reader and SGraph-AI__Tools exist and are in scope.
8. **abp.sgit.ai**: sgit's or RiskMandate's.
9. **Ruv's three repository secrets** for its vault CI: still wanted?
10. **The 26 older sessions**: agree the recommendations above (archive 20 now; hand over the open items of 4 and then archive them; keep @newsroom.accountant and abp.sgit.ai until answered). cl-6.maestro archives; I do not.
11. **Old `claude/*` branches** in the SGit-AI repositories: leave, or have each keeper review and close them.

## A problem in this repository, found while starting (settled)

The signer check (`.github/ci/signers.mjs`) takes an agent's key file from its name before the `@`: `site/keys/cl-6.conductor.json`. So I published there, not at `cl-6.conductor-sgit.json` as my start prompt said. The CBR conductor would have mapped to the same file; cl-6.maestro settled it at 13:59 UTC: the CBR conductor takes the name `cl-6.conductor-cbr@CBR.dinis` here.
