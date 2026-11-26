# The signer check accepts a key filed under the full agent id (26 Nov 2026)

**Dinis Cruz, in cl-6.conductor-sw's session, 26 Nov 2026:** "yes, do option 2, fix the signer check" (option 2 of [the handover](../sessions/2026-11-26-first/handover.md): the signer check keyed on the full agent id, so a role suffix repeating the @project can go; [his rule](../decisions/2026-11-26-name-suffix-redundant.md)).

## The change (`.github/ci/signers.mjs`)
- A site may publish an agent's key at `site/keys/<name before the @>.json` (as before) **or** `site/keys/<full agent id>.json`, e.g. `site/keys/cl-6.conductor@SovereignWebsite.dinis.json`. Two agents sharing a short name in one repository no longer clash.
- Self-publication (a commit that only adds the trailer's own key file) now also requires that the agent has **no live key in the repository already**, so a full-id file cannot slip a second key in under a name that has one. Before, the short file's existence blocked that by itself.
- The live-key guard compares agent ids without regard to case (cl-6.security's low finding, fixed by cl-6.conductor on 26 Nov 17:01 UTC): `G@X.y` cannot self-publish a key beside a live `g@X.y` one.
- Unchanged: Factory keys match by full name; a Factory agent's name cannot be claimed with another key; a key added with any other change does not vouch for itself; owner override and person commits as before.

## Tested
In a clone of SovereignWebsite__IaC (dev, 26 Nov): the fix in `seed/site-template` and copied to every seed carrying the check, `node build/managed.mjs record` run, and five new cases in `test/run.mjs` (a second agent with the same short name publishes under its full id; its later commit passes; the short-name agent still passes; a full-id file cannot add a second key under an existing name; a full-id key with another change does not vouch for itself), and a sixth for the case finding (a full-id file under the same name in another case is refused; it fails without the fix). `node test/run.mjs`: every block OK, last run against dev 94b1625.

## Where it is
- **Here:** applied to this repository's `.github/ci/signers.mjs` on Dinis's word. Org apply keeps a keeper's change and reports it (build/managed.mjs), so it will not be overwritten.
- **For the Factory:** [2026-11-26-signers-full-agent-id.patch](2026-11-26-signers-full-agent-id.patch), against SovereignWebsite__IaC dev (seeds, managed history, tests). Regenerated after the case fix. I cannot push there; routed through cl-6.maestro to the Factory, with security review before org apply carries it to every site.
