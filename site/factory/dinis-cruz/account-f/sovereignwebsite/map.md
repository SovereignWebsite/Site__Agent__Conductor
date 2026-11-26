# The Sovereign Website work on account 6: map and proposed split

By cl-6.conductor-sw@SovereignWebsite.dinis, 26 Nov 2026, 16:45 UTC. A first read; nothing was changed anywhere outside this area. Every claim points at where it was read. Where something was not found, it says so.

**How it was read.** The agent sites (maestro, factory, conductor, decisions .agents.sovereignweb.site) do not resolve from this session's "Default (limited)" network, so I read their public source repositories on GitHub instead (dev branches, cloned read-only at about 16:41 UTC): SovereignWebsite__IaC, Site__Agent__Maestro, Site__Agent__Maestro__Claude__6, Site__Agent__Factory, Site__Agent__Decisions. Paths below are in those repositories.

## 1. What the Sovereign Website work is
- **Account B is the Sovereign Website account** (Dinis, 23 Nov, through maestro.b; IaC `board/2026-11-23__go-to-market-week.md`). The week of 23 to 30 Nov is "go-to-market week": "scalability and offering our services ... go to market with sovereign websites ... get the hub to the next level ... creating websites, every hour ... the whole design loop, this whole usability loop, the whole observability loop ... what we're selling is this agentic workflow" (same file, Dinis's words abridged there).
- **What is built:** sites made and kept by agents, each in its own repository under the SovereignWebsite organisation, deployed by the Factory's pipeline (IaC, Site__Agent__Factory), with signed commits, agent areas on agent-type sites, the hub (hub.sovereignwebsite.site) and its operator page, and Dinis's decisions as signed records (Site__Agent__Decisions).
- **The plan's lanes** (go-to-market-week.md): hub.b (operator page, then the hub's next level); librarian.b (every agent of each role across accounts, "the librarian comes first"); sites.b (a queue of sites, one live each time it works); design.b and design.b.rounds (one design improvement live each round, starting with the selling sites); strategy.b (segments, pipeline); outreach.b (drafts only, a person sends after Dinis's yes); observability.b (traffic, blocked on Dinis); conductor.b (dispatch and status.json).
- **Limits stated there:** wakes on account B off until Dinis re-enables them; prices only as `board/2026-11-19__saw-plan.md` records them; no private prospect named in any repository.

## 2. Agents on account B (Sovereign Website)
From b.maestro's list, Site__Agent__Maestro `site/factory/dinis-cruz/account-b/sessions.json` (updated field 24 Nov 00:17 UTC, entries added since), "does" as written there:

| Agent | Does |
|---|---|
| b.conductor (conductor.b) | conductor of the Sovereign Website team; handing over to a fresh session (below) |
| b.decisions | signs Dinis's decisions for all accounts |
| b.strategy | go-to-market, market research, use cases |
| b.factory | the IaC factory: pipeline, policy, org, DNS |
| b.sites | new sites and their content; shared navigation |
| b.hub | hub.sovereignwebsite.site |
| b.design (session 2), b.design.rounds | design guidelines and sign-off; design rounds |
| b.security | security reviews before anything goes live |
| b.observability (session 2) | traffic for every site |
| b.feedback | the feedback box on every site |
| b.librarian | the library and the newsroom relay |
| b.accountant | budgets |
| b.outreach | outreach drafts with Dinis |
| b.startups | startup brochure sites |
| suno.b (new session) | music for the posts; songs podcast |
| b.migration | AgentiCCells sites to SovereignWebsite |
| b.vault.keeper | the only agent that holds onboarding vault keys (26 Nov, Opus) |
| cl-2.crm.dev | the CRM, moved from crm.dev.a on A (26 Nov, Opus) |
| b.calendar | the Google Calendar tool (26 Nov, Sonnet) |
| b.social | the social media agent: every channel, approved posts to Buffer (26 Nov, Sonnet) |
| b.stories | second stories: the gap behind each problem (26 Nov, Opus) |

Also named in b.maestro's `now.md` (25 Nov 19:19 UTC) as waiting on Dinis: studio.b, instagram.b, b.onboarding, and b.abp's draft policies for account B's 22 agents. Site keepers for individual sites are listed by b.sites; not copied here.

**conductor.b's state** (IaC `board/conductor.b/agent.json`, updated 26 Nov 01:42 UTC): "handing over" to https://claude.ai/code/session_01Kw9UwBrWEfUnBbb4gCS9cg (Dinis, 01:41 UTC 26 Nov); active until 1 Dec; no wake ("one of the four Dinis has not created"); its area lives in IaC `board/conductor.b/` because it has no push here ("until it moves there (onboarding order, item 5)"). It keeps `status.json` and `board/operator.json` (feeds https://hub.sovereignweb.site/operator/), routes Dinis's words, retires key entries but never adds one, and does not build (`role.md`). Its operator view (updated 26 Nov 01:41 UTC) lists 17 asks waiting on Dinis. I found no newer record from its new session in the repositories read.

**Capacity:** b.maestro, 25 Nov 19:19 UTC: "Account B at 43% of its weekly limit; resets Monday." Account 6, cl-6.maestro `now.md`: "account 6 is now on Max, 11% of the 5-hour limit and 2% of the weekly used" (an earlier entry, 26 Nov); Dinis on 26 Nov ~16:35 UTC asks for missing agents to be made "on the accounts that have more head-room (token wise)" (`decisions/2026-11-26-create-missing-agents.md`). **Newer (26 Nov, about 16:45 UTC):** account B is at 73% of its capacity, from Dinis as relayed by cl-6.maestro at 16:47 UTC (not in a signed record), with his direction that more of the token-heavy Sovereign Website work should move to account 6 this week. Not found: a newer figure for account 6.

## 3. Sovereign Website agents already on account 6
From cl-6.maestro, Site__Agent__Maestro__Claude__6 `site/factory/dinis-cruz/account-f/sessions.json` and `now.md`:

| Agent | What, as recorded | Shared repository |
|---|---|---|
| cl-6.social@dinis | twin of b.social; drafts for PrompTugal, sgit, CBR and the Sovereign Website videos; never posts, never holds a token (started 16:33 UTC 26 Nov, Sonnet) | Site__Agent__Social |
| cl-6.helm@dinis | the helm twin: top-level dev and design advice; first job append lanes v2 tests and guide (25 Nov 23:08 UTC, Opus) | Site__Agent__Helm |
| The decisions panel: cl-6.decisions, cl-6.security, cl-6.strategy, cl-6.accountant (@dinis), cl-6.maestro the fifth voice, cl-6.counsel when needed (25 Nov 23:15 UTC) | account 6's decisions; cl-6.decisions endorsed by decisions.2 until 30 Nov | Site__Agent__Decisions, Security, Strategy, Accountant, Counsel |
| cl-6.router@dinis | router of account F: cross-account synchronisation | Site__Agent__Router__Claude__6 |
| cl-6.conductor@sgit.dinis, cl-6.conductor-cbr@CBR.dinis | conductors of sgit and CBR (13:54 UTC 26 Nov) | this repository |
| cl-6.conductor-sw (me) | this map | this repository |
| cl-6.studio@dinis | the Sovereign Website videos (started 16:50 UTC 26 Nov, Sonnet; https://claude.ai/code/session_016CrbJJe27HT4pDaUAkSFEi) | Site__Agent__Studio |
| cl-6.librarian@dinis | the librarian's first run (16:50 UTC, Sonnet; https://claude.ai/code/session_016CrbJL9iaXQ1KjPkESLpRK) | Site__Agent__Library |
| cl-6.design@dinis | design rounds on the selling sites, as proposals for b.design (16:50 UTC, Sonnet; https://claude.ai/code/session_016CrbJN8TyFQTFEyKbVKSXf) | Site__Agent__Design |
| cl-6.observability-sw | token-heavy, credential-free work for observability.b: drain tests, review, secret-free pilot drafts, stats page, reports ([plan](https://github.com/SovereignWebsite/Site__Agent__Observability/blob/dev/site/factory/dinis-cruz/account-f/sovereignwebsite/plan.md); split waits on observability.b and Dinis) | Site__Agent__Observability |

Not yet on account 6, recorded as waiting on Dinis in cl-6.maestro's `now.md`: **the Sovereign Website videos** ("a studio twin of studio.c on F, with a publishing agent that prepares posts for a person to post. Needs Site__Agent__Studio and Site__Agent__Instagram attached to account F"; "Whether to start the Sovereign Website studio session now, on Site__Agent__Studio"). Everything else on account 6 (about 45 sessions) is PrompTugal.

## 4. What account 6 could take on (proposals, for Dinis to choose)
With account B at 73% (section 2), all three sessions below are worth starting this week, not one at a time; the order is a suggestion. The rule I propose: account 6 takes **token-heavy work that reads widely and writes into its own areas or as proposals**, and leaves every site's keeper, every pipeline and every routing job where it is on account B. Each is a twin in its role's shared repository, as Dinis's 25 Nov rule says ("Twins, not homes").

1. **The studio and videos (first).** Already Dinis's open question to cl-6.maestro. cl-6.studio@dinis in Site__Agent__Studio (area `site/accounts/f/` or `site/factory/dinis-cruz/account-f/`), Sonnet; makes the Sovereign Website videos; cl-6.social drafts their posts; a person posts.
2. **The librarian's first run.** The plan says the librarian comes first; IaC `operator.json` shows it waiting on "a budget for the librarian's first run". A cross-account read of every agent of each role is mostly reading: account 6's head-room fits it. cl-6.librarian@dinis in Site__Agent__Library, Sonnet, writing only its account-f area; b.librarian adopts or publishes what it wants.
3. **Design rounds.** One improvement per round on the selling sites (hub, sovereign-website.startups) needs many renders and checks. cl-6.design@dinis in Site__Agent__Design proposing changes as branches or patches for b.design's sign-off, never merging to a site it does not keep.
4. **Site health sweeps.** Run tools/check.sh-style checks (link previews, accessibility, HTML validity) across the public Sovereign Website site repositories and publish one findings page per sweep in my area, for each keeper to act on. I can do this myself, read-only, no new session.
**Environment (cl-6.maestro, 16:44 UTC):** the limited "Default" environment allows no outside hosts. 1 (studio) and 3 (design) need only their repository. 2 (librarian) reads public GitHub repositories, which `git clone` reached from Default in this session; if it must read the live agent sites, it needs those *.agents.sovereignweb.site hosts allowed, which is Dinis's and cl-6.maestro's call.

5. **Not proposed:** a second conductor routing account B's agents, any key or IaC work, outreach, or anything on Dinis's one-way list.

## 5. How I split with conductor.b, without duplicating
- **conductor.b keeps** account B: routing Dinis's words to account B agents, status.json and the operator page, key retirements in IaC, the onboarding order. I never write to SovereignWebsite__IaC or to an account B agent's area, and never route to account B agents.
- **I keep** account 6's Sovereign Website lane: this map, the roster of account 6 SW twins, their proposals to cl-6.maestro (who alone creates sessions and wakes, cl-6.abp's R4), and their state in my `now.md`.
- **One keeper per site.** An account 6 twin never pushes to a site an account B agent keeps unless a decisions record hands it over; until then it proposes (branch, patch or findings page) and links it.
- **One list for Dinis.** I do not start a second asks list: account 6's SW asks go into my `agent.json` `waiting_on` and to cl-6.maestro, and I ask cl-6.router to tell conductor.b (and b.maestro) by link so the operator page can show them.
- **Reading, not messaging.** I read conductor.b's area and operator.json at every wake before proposing anything, so work it already holds is not started twice.

## 6. What Dinis must decide
1. ~~Which of section 4's proposals to start~~: all three (Dinis, 16:48 UTC, [record](decisions/2026-11-26-start-studio-librarian-design.md)); Sonnet as proposed.
2. The split in section 5: is account 6 the place for token-heavy Sovereign Website work, with account B keeping routing and keepers?
3. May account 6 twins push to account B's site repositories when a keeper agrees, or only propose (my default: only propose)?
4. Network: this session cannot resolve *.agents.sovereignweb.site, so it reads the source repositories instead. Allowing those hosts in the Default environment is an environment change for cl-6.maestro and you; reading GitHub works meanwhile.
5. conductor.b's area: it was to move into this repository (its onboarding order, item 5). Its keeper's call and yours; I will not touch it.
6. ~~A wake for me~~: set by cl-6.maestro, trig_01Exkuw8Yfc7D9XMoME9PFo9, 09:47 and 18:47 UTC.

## 7. Known issue
`bash tools/check.sh` fails on dev before any change of mine, on the repository's own `site/index.html` (no Open Graph and Twitter tags, share-check). Recorded, not fixed: outside my area.
