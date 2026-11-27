# Request: Site__Ideas at ideas.sovereignweb.site (27 Nov 2026, 11:39 UTC)

**Asked by Dinis Cruz**, in cl-6.maestro's session, 27 Nov 2026, relayed to me by cl-6.maestro at 11:37 UTC: "for these briefs and ideas can you put them on the actual site (with dedicated github repo, DNS and CI pipeline) and I will work on them there ... we can then track what is the maturity model of each of these ideas"; "I would like is to see this on a site (that also has a good design)".

## What this asks the Factory for
A request in the Factory's own format (SovereignWebsite__IaC `requests/README.md`), ready to copy as it is:

- [`requests/2026-11-27__ideas/site.json`](requests/2026-11-27__ideas/site.json) goes to IaC `requests/2026-11-27__ideas/site.json`.
- [`build-requests-no-group.patch`](build-requests-no-group.patch), one line in IaC `build/requests.mjs`, adds `ideas` to `NO_GROUP`.

Org apply and DNS apply then make:
- the repository **SovereignWebsite/Site__Ideas**, with Pages from dev and the usual site pipeline: version, build, checks (link previews, links, quality, HTML validity, accessibility), deploy and tag;
- the address **https://ideas.sovereignweb.site**, with a CNAME in Route 53 and HTTPS once GitHub issues the certificate.

## On the name and address
The Factory's rule is that every site has a group (Dinis, 20 Nov 2026: "Everything should have a group for now"). No group fits a set of Dinis's own ideas. The rule already allows exceptions for a product's own home, listed in `NO_GROUP`: `presentations.sovereignweb.site` (Dinis, 23 Nov) and `review.sovereignweb.site` (block 2026-11-24__block-03). This request uses the same exception, so the name cl-6.maestro proposed stands. A site with no group is named `Site__<Name>`, which gives **Site__Ideas**.

If Dinis prefers no exception, the alternative is a new group: `dinis-cruz.ideas.sovereignweb.site` as `Site__Ideas__Dinis-Cruz`, one site per person as `presentations` does. That needs `ideas` added to `GROUPS` and `GROUP_NAMES` instead. It is not drafted here.

## Keeper and design
- **Keeper:** cl-6.ideas@SovereignWebsite.dinis. cl-6.maestro starts that session once the repository exists, on Dinis's yes.
- **Design:** cl-6.design@dinis. By the Factory's guidance a new request is registered with design.b at M0 for a design brief. cl-6.design works as proposals for b.design's sign-off (map.md section 3), so the brief and sign-off stay with design.b.
- **Content to seed it**, staged by cl-6.maestro in Site__Agent__Maestro__Claude__6 dev, `site/factory/dinis-cruz/account-f/`: `ideas/index.json` (b5017eb: six ideas, a 0 to 6 maturity scale, intersections), `plans/2026-11-27-commerce/`, `plans/2026-11-27-events/`, `plans/2026-11-27-meetscribe-store.md` and `decisions/2026-11-27-work-cells.md`. The keeper copies it in after its first build.

## Checked
In a clone of SovereignWebsite__IaC (dev, 27 Nov 11:39 UTC), with both files applied:
- `validate()` from build/requests.mjs returns no errors;
- `host()` gives `ideas.sovereignweb.site` and `repoName()` gives `Site__Ideas`;
- `load('requests')` returns no errors;
- `node test/run.mjs` passes.

## What Dinis must do
1. Say yes to this request and its address. `requests/**` needs his merge (policy/abp.json).
2. Merge it when it lands. factory.b commits requests sent by other agents, naming on whose behalf. I cannot push to SovereignWebsite__IaC, and I do not route to account B agents, so this goes to factory.b through cl-6.maestro and cl-6.router.
