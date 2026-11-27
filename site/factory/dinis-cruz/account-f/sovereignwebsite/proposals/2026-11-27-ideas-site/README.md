# Requests: the ideas sites (27 Nov 2026)

**Dinis Cruz, in this session (cl-6.conductor@SovereignWebsite.dinis), 27 Nov 2026:** "yes, go with Site__Ideas at ideas.sovereignweb.site and dinis-cruz.ideas.sovereignweb.site I like that". First asked in cl-6.maestro's session, relayed at 11:37 UTC: "for these briefs and ideas can you put them on the actual site (with dedicated github repo, DNS and CI pipeline) and I will work on them there ... we can then track what is the maturity model of each of these ideas"; "I would like is to see this on a site (that also has a good design)".

Read as the presentations pattern: a product home with no group, plus one site per person under a new `ideas` group.

## The two sites
| Address | Repository | Request |
|---|---|---|
| https://ideas.sovereignweb.site | SovereignWebsite/Site__Ideas | [requests/2026-11-27__ideas/site.json](requests/2026-11-27__ideas/site.json) |
| https://dinis-cruz.ideas.sovereignweb.site | SovereignWebsite/Site__Ideas__Dinis-Cruz | [requests/2026-11-27__dinis-cruz/site.json](requests/2026-11-27__dinis-cruz/site.json) |

Both are public, with Pages from dev and the usual site pipeline: version, build, checks (link previews, links, quality, HTML validity, accessibility), deploy and tag. DNS apply adds the CNAMEs, and HTTPS follows once GitHub issues the certificates.

## The rule change
[build-requests-ideas-group.patch](build-requests-ideas-group.patch), against SovereignWebsite__IaC dev b252826:
- `ideas` is added to `GROUPS` and `GROUP_NAMES` (as "Ideas", so the repository is `Site__Ideas__<Name>`);
- `ideas` is added to `NO_GROUP`, so the product's own home can sit at ideas.sovereignweb.site, as presentations does;
- a row for the `ideas` group goes in the groups table of `requests/README.md`.

## Keeper and design
- **Keeper of both:** cl-6.ideas@SovereignWebsite.dinis. cl-6.maestro starts that session once the repositories exist.
- **Design:** cl-6.design@dinis. By the Factory's guidance a new request is registered with design.b at M0 for a design brief. cl-6.design works as proposals for b.design's sign-off (map.md section 3), so the brief and sign-off stay with design.b.
- **Content to seed it**, staged by cl-6.maestro in Site__Agent__Maestro__Claude__6 dev, `site/factory/dinis-cruz/account-f/`: `ideas/index.json` (b5017eb: six ideas, a 0 to 6 maturity scale, intersections), `plans/2026-11-27-commerce/`, `plans/2026-11-27-events/`, `plans/2026-11-27-meetscribe-store.md` and `decisions/2026-11-27-work-cells.md`. The keeper copies it in after its first build.

## For the design brief
- **The strategy behind it.** Dinis, word for word, relayed by cl-6.maestro at 11:38 UTC: "the core strategy is that all of this (i.e. sites) are way for users/customers to experience ABPs". It is recorded in `ideas/index.json` under "strategy". So each idea's page shows the behaviour policy (ABP) of the agents and tools behind that idea, not only a description of the idea.
- Dinis liked the events MVP's layer diagram (`plans/2026-11-27-events/`). He wants the site to have a good design.

## Checked
In a clone of SovereignWebsite__IaC (dev b252826, 27 Nov), with the patch and the three requests from today applied (these two, and [the poet's](../2026-11-27-poet-site/README.md)):
- `validate()` returns no errors for any of the three, and `load('requests')` returns no errors;
- the addresses and repository names come out as in the table above;
- `node test/run.mjs` passes.

## What is left
Dinis has said yes, in this session. Next, factory.b copies the files into SovereignWebsite__IaC (it commits requests sent by other agents, naming on whose behalf), and Dinis merges, because `requests/**` and `build/**` need his merge (policy/abp.json). I cannot push to SovereignWebsite__IaC, so this goes to factory.b through cl-6.maestro and cl-6.router.
