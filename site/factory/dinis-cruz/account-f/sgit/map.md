# sgit: map of the project's repositories

By cl-6.conductor@sgit.dinis, 26 Nov 2026, 13:57 UTC. First piece of work, before changing anything: nothing below has been changed by me. Every fact comes from a repository, PyPI or a public page read today; what I could not see is marked so.

## How I looked

- `list_repos` on account 6 (queries: sgit, sgraph, send, vault, cyber-boardroom), and the full list.
- The project's own public pages: https://sgit.ai/llms.txt, https://sgit.ai/llms-full.txt (every page of the site in one file), https://sgit.ai/.well-known/sgit-agents.json, https://newsroom.sgit.ai/llms.txt, and the PyPI record for `sgit-ai` (https://pypi.org/project/sgit-ai/).
- `git ls-remote` and a shallow, read-only clone of each public repository those pages name (last 30 commits of the default branch).

## The short version

- **The code is `SGit-AI/SGit-AI__CLI`** (PyPI names it as the repository). It is public but not attached to account 6, so I can read it and cannot push to it.
- **The project lives in its own GitHub organisation, `SGit-AI`**, none of whose repositories are visible to account 6. Seven are public; four names the site gives are not public (or do not exist).
- **One repository it depends on is visible here:** `the-cyber-boardroom/SGraph-AI__App__Send` (the SG/Send server sgit speaks to). That is the CBR conductor's ground as much as mine.
- **Nothing in the sgit repositories follows the current way yet**: no per-agent keys, no `Agent:` trailers, no agent areas (one exception: the newsroom, below), several still work on `claude/*` branches and on main.
- **One rule clash to settle first:** in SGit-AI__CLI a push to dev publishes a pre-release to PyPI. "Dev only" there still ships a package.

## Repositories

### Visible to account 6 (can push)

| Repository | What it is | State on 26 Nov 2026 |
|---|---|---|
| SovereignWebsite/Site__Startups__Sgit | The independent brochure at sgit.startups.sovereignweb.site, made from sgit's public pages. Kept by startups.b on account B. Not the project. | dev last moved 25 Nov (Factory org-apply refreshes). Already on the current way (CLAUDE.md, signed keys, dev only). Its facts.json stops at 28 Oct 2026 (0.27.0). |
| the-cyber-boardroom/SGraph-AI__App__Send | SG/Send: the zero-knowledge storage and transfer API (Python) and its web UIs (SG/Vault, share, admin, workspace). sgit's default server is `dev.send.sgraph.ai`. | Active: dev last commit 25 Nov 2026 21:24 UTC; 28 branches, many `claude/*`. Commits carry `Claude-Session:` but no `Agent:` trailer and no per-agent key. Has its own `team/` folder of role files. |
| SovereignWebsite/SovereignWebsite__Vault, Site__Agent__Vault-Keeper | Names match "vault"; they are SovereignWebsite's own, not sgit's. | Not part of sgit as far as I can tell; listed so nobody else wonders. |

### Public, not attached to account 6 (read only from here)

| Repository | What it is | Branches | State |
|---|---|---|---|
| SGit-AI/SGit-AI__CLI | **The sgit code**: package `sgit-ai`, Python 3.11+, Apache-2.0, author "The Cyber Boardroom" on PyPI. | dev, main, 17 others (mostly `claude/*`) | dev last commit 15 Nov 2026; dev carries version v0.27.1, PyPI's latest release is 0.27.0 (28 Oct). CI: a dev push publishes a PyPI pre-release; a main push publishes the release and to Docker Hub. Has CLAUDE.md (Type_Safe rules), `team/` (assessment, decisions, explorer, humans, villager), `review/`, `_to_review/`. Commits by "Claude" with one session URL, no `Agent:` trailer. |
| SGit-AI/SGit-AI__Website | sgit.ai, the official documentation site, itself served from a vault. | dev and 6 `claude/*` | dev last commit 13 Oct 2026 (site v0.7.87, "the newsroom has moved"). GitHub Pages deploy from dev. No `Agent:` trailers. |
| SGit-AI/SGit-AI__Website__Newsroom | newsroom.sgit.ai, the SGit Newsroom. | default dev | **The most active**: last commit 24 Nov 2026 (site v0.14.214). Its own agents already keep areas: the last commit is "d.newsroom (writer-11) keeps its area current: agent.json, now.md, role.md". So it is already being retrofitted, apparently from account D. |
| SGit-AI/SGit-AI__Website__PKI | pki.sgit.ai. | dev, main, 7 `claude/*` | dev last commit 23 Nov 2026 (site v0.2.36). |
| SGit-AI/SGit-AI__Website__Graphs | graphs.sgit.ai (Fractal Semantic Graphs). | dev, main, 6 `claude/*` | dev last commit 20 Sep 2026 (v0.6.22). Has CLAUDE.md and `decisions/`. |
| SGit-AI/SGit-AI__Website__Secrets | secrets.sgit.ai. | dev, main | dev last commit 6 Oct 2026 (v0.1.13). |
| SGit-AI/SGit-AI__Website__NHI | nhi.sgit.ai. | dev, main (same commit) | Last commit 19 Aug 2026 (v0.1.19). Quiet. |
| SGit-AI/SGit-AI__Website__SG_Sentinel | sg-sentinel.sgit.ai; the site itself says SG/Sentinel is a May 2026 design, not built. | dev, main | Last commit 20 Aug 2026 (v0.1.1). Quiet. |

### Named by the project's pages, not public (or not existing)

`SGit-AI/SGit-AI__Newsroom__API` (a villager brief names it as the newsroom's repository), `SGit-AI/SGit-AI__SG-Meter` (the reading meter), `SGit-AI/SGit-AI__Reader`, `SGit-AI/SGit-AI__Newsroom__Reader`, and `SGraph-AI__Tools` (owner not stated; not public as `sgraph-ai` or `SGraph-AI`). I cannot tell private from absent without access.

### Sites with no repository I could find

sgit.ai names about 40 subdomains of its own (for example coding, open-source, abp, nfrs, risks, wardley-maps, twins, llms, skills, issues-fs, subscriptions, standards, store, providers, teams, games). Many may be vaults served as apps rather than repositories; I have not checked each. Mapping them is a later piece of work if Dinis wants it.

## Which agents it needs (proposal)

The project is a product with one code repository and a cluster of sites. A team under this area, `site/factory/dinis-cruz/account-f/sgit/<role>/`, each in its own session created by cl-6.maestro (rule R4):

1. **cl-6.conductor@sgit** (me): the map, the retrofit plan, routing; no code.
2. **a dev for SGit-AI__CLI**: the code, tests and releases. First of the team, because the PyPI-on-dev rule must be settled before any agent pushes there.
3. **a site keeper for SGit-AI__Website** (sgit.ai, the docs): it is the agents' main entry point and has not moved since 13 Oct.
4. **the small sites** (PKI, Graphs, Secrets, NHI, SG_Sentinel): one keeper for all five while they are quiet, not one each.
5. **the newsroom**: already has agents (d.newsroom and its writers). I propose leaving it with them and only linking it from here, unless Dinis wants it moved to account 6.
6. **SG/Send** (SGraph-AI__App__Send): shared with The Cyber Boardroom; I propose it belongs to the CBR conductor, with sgit's needs sent there.

The existing `team/` folders in SGit-AI__CLI and SGraph-AI__App__Send (explorer, villager, librarian and others) are an older role set; the retrofit should say what happens to them rather than run two systems side by side.

## Does sgit need its own IaC repository?

My view: **not now**. The org-level things (repositories, keys, Pages settings) can go through SovereignWebsite__IaC as for other projects, and the project's history can live in the agents' homes here. The case for one later: sgit is its own GitHub organisation with release secrets (PyPI, Docker Hub) and many sites, which SovereignWebsite__IaC does not manage today. It is Dinis's call; I would wait until the CLI's release pipeline is under the new way.

## What Dinis must attach or decide

1. **Attach SGit-AI__CLI** (and, when its keeper starts, SGit-AI__Website) to account 6 in new sessions created by cl-6.maestro, not to mine. Today account 6 has no access to the SGit-AI organisation at all.
2. **Private repositories**: whether SGit-AI__Newsroom__API, SG-Meter, Reader and Newsroom__Reader exist and should be in scope.
3. **Dev publishes to PyPI**: keep it (a dev push is a pre-release), or change the CLI's pipeline so only a release step publishes.
4. **The newsroom**: stays with its current agents (apparently account D), or comes under this conductor.
5. **SG/Send**: mine, the CBR conductor's, or shared.
6. **An IaC repository for sgit**: yes or no (my view above: no, for now).
7. **Old `claude/*` branches and work on main** in the SGit-AI repositories: leave, or have each keeper review and close them.

## A problem in this repository, found while starting

The signer check (`.github/ci/signers.mjs`) takes an agent's key file from its name before the `@`: `site/keys/cl-6.conductor.json`. So I published there, not at `cl-6.conductor-sgit.json` as my start prompt said (that file would be ignored and every later commit refused). But the CBR conductor is `cl-6.conductor@CBR.dinis`, which maps to the same file. Its key commit would change my file rather than add a new one, so the check would refuse it, and it could not publish its key without taking my place. One of the two names must change (for example `cl-6.conductor-cbr@...`), or the check must take the whole name. Raised with cl-6.maestro.
