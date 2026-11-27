# Now: cl-6.conductor@sgit.dinis

Updated 27 Nov 2026, 01:42 UTC.

## Done
- Key made with openssl; public half published alone at `site/keys/cl-6.conductor.json`; git signs with it in this clone.
- [map.md](map.md): the project's repositories, their state, the team it needs, the IaC question, and what Dinis must attach or decide. Nothing in the project changed.
- map.md revised at cl-6.maestro's ask: account 6's 26 older sgit sessions (August to October), from their records only, with a keep, hand over or archive recommendation each; and the 17 more SGit-AI site repositories they work on (24 public in all).

- 27 Nov 01:36 UTC: cl-6.maestro, at Dinis's word, started cl-6.website@sgit.dinis on SGit-AI__Website (reports to me) and cl-6.conductor@SGSend.dinis on SGraph-AI__App__Send (a peer). Both added to map.md and agent.json.

## Open
- Three API findings from cl-6.conductor@SGSend.dinis recorded in map.md for the CLI dev (not yet checked in the code). I talk to that conductor directly about the API.
- **Blocker:** SGit-AI is read only from account 6. cl-6.website's push to SGit-AI__Website got 403 at 01:36 UTC (the Claude GitHub App has no access). Dinis must install the App on SGit-AI or reconnect GitHub. I was wrong at 01:37 UTC to tell cl-6.maestro the access worked; corrected in map.md.
- Brief cl-6.website@sgit.dinis on its two handovers (map.md, sgit.ai section) once it has its key and area.
- Waiting on Dinis (through cl-6.maestro) for the ten open questions at the end of map.md (SG/Send is answered). Nothing else moves until SGit-AI__CLI is attached to a new session and the PyPI-on-dev question is answered.
- **Differs from my start prompt:** it named my key file `cl-6.conductor-sgit.json`; the signer check only reads `site/keys/<name before @>.json`, so I used `cl-6.conductor.json`. The CBR conductor would have mapped to the same file; settled by cl-6.maestro at 13:59 UTC: mine stays, the CBR conductor takes the name cl-6.conductor-cbr@CBR.dinis here.
- cl-6.maestro (13:59 UTC): wait for Dinis's answers before attaching anything or proposing sessions beyond the team list in map.md.
- No wake set; to propose to cl-6.maestro once there is work to wake for.
- `tools/check.sh` fails before my changes: the site's own `site/index.html` (outside my area) has none of the 14 Open Graph and Twitter tags, so the deploy fails until its keeper fixes it. My files are Markdown and JSON only. cl-6.maestro will raise it with the page's keeper; I leave the page alone.
