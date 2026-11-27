# Request: the poet A. Oliveira Cruz's site (27 Nov 2026)

**Dinis Cruz, in this session (cl-6.conductor@SovereignWebsite.dinis), 27 Nov 2026:** "can you create a site for the poet a-oliveira-cruz which A. Oliveira Cruz who has published a very large body of work of poetry in Portugal".

## The site
- **Address:** https://a-oliveira-cruz.author.sovereignweb.site
- **Repository:** SovereignWebsite/Site__Author__A-Oliveira-Cruz
- **Request:** [requests/2026-11-27__a-oliveira-cruz/site.json](requests/2026-11-27__a-oliveira-cruz/site.json). It is public; keeper cl-6.a-oliveira-cruz@SovereignWebsite.dinis (a session cl-6.maestro would start), design cl-6.design@dinis.

## Why `author` and not `poet`
- `author` is the Factory's group for "writers and their work" (Dinis, 22 Nov 2026, for donna-freed: "put her as an author"). A poet fits it without any rule change.
- In `<label>.<provider>.<group>`, the middle part of an author address names the author of a work, for one of their works: Dinis's book is `one-human-nine-agents.dinis.author.sovereignweb.site`. So `a-oliveira-cruz.poet.author` would read as a work called "a-oliveira-cruz" by an author called "poet".
- `a-oliveira-cruz.poet.sovereignweb.site` would need a new `poet` group, a rule change for one site.
- What it leaves room for: each collection can later have its own site under the poet, as `<collection>.a-oliveira-cruz.author.sovereignweb.site`.

## Before it is made public
The Factory's rule: "Every site Dinis asks for has the person's or organisation's approval for a public address", and a request names no private person until they agree. A body of published poetry makes the name public as an author. The site still needs A. Oliveira Cruz's agreement (or that of whoever speaks for the work) to a public address, recorded by Dinis. Until then the request waits, or goes in as a private vault site (`"access": "vault"`), which shows only a gated holding page.

## Content
Only from sources Dinis gives, or the poet's own published material. Nothing is invented about the poet's life or work. The keeper asks Dinis for sources at its first round.

## Checked
In a clone of SovereignWebsite__IaC (dev b252826), together with the ideas requests: `validate()` returns no errors, the address and repository name are as above, and `node test/run.mjs` passes.
