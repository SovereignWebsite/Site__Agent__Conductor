# Cell brief: research everything published by and about A. Oliveira Cruz

Proposed 2026-11-27T15:24Z by cl-6.conductor@SovereignWebsite.dinis, for cl-6.maestro@dinis to open as a work cell (Site__Agent__Maestro__Claude__6 `decisions/2026-11-27-work-cells.md`; it keeps `cells/board.json` and starts the sessions). Proposed id: `2026-11-27-poet-research`.

## Objective, in Dinis's words
"can we use our new AgileCells on this site? starting with a full research on all that has been published and is available on google, note that we have now access to Google Search from the API, so we should leverage it" (Dinis, in cl-6.conductor's session, 27 Nov 2026).

The site is a-oliveira-cruz.author.sovereignweb.site (Site__Author__A-Oliveira-Cruz; [request](README.md)). The poet has agreed to a public site (Dinis, same session).

## What the research covers
1. **His published works.** Every book, collection, anthology appearance and periodical publication that can be found, with title, year, publisher, place, edition and ISBN where known.
2. **What has been written about him and his work.** Reviews, articles, interviews, prizes, readings, events, library and catalogue entries.
3. **Where his work can be found today.** Publishers, bookshops, libraries, archives and digital copies.

## How
- **Google Search through the API**, as Dinis asked. Search in Portuguese first and in English. Vary the name: "A. Oliveira Cruz", the full name if Dinis gives it, and the titles as they are found.
- Also search the catalogues that list Portuguese publications directly, such as PORBASE (the Portuguese national bibliographic database), publishers' and bookshops' catalogues, and newspaper archives.
- Read each source, not just the search snippet. Record the URL, the date read, and what it says.

## Rules
- **Nothing invented.** Every fact carries at least one source; two independent sources for dates and titles where possible. Conflicts between sources are listed, not resolved by guessing.
- **Published and public material only.** Nothing about his private or family life beyond what he has published himself or Dinis gives. No relatives are named.
- **No poems copied in full.** Copyright stays with the poet and his publishers. The site quotes only short lines with their source, or texts the poet or Dinis provides for it.
- No paid sources, logins or scraping behind a paywall. No contact with third parties without Dinis's word.
- Plain British English for the notes; titles and quotations stay in Portuguese.

## Roles
| Role | Who | Does |
|---|---|---|
| Researcher | a short-lived cell session with the Google Search API (cl-6.maestro starts it) | runs the searches, reads the sources, drafts the files below |
| Checker | a second session, or cl-6.librarian@dinis if it is running | re-checks each fact against its sources, marks each one confirmed, single-source or conflicting |
| Keeper | cl-6.a-oliveira-cruz@SovereignWebsite.dinis, once the repository exists | applies the result to the site repository, signed, naming the cell |
| Review | cl-6.conductor@SovereignWebsite.dinis | checks the result against this brief before the keeper applies it |

## Deliverable
One diff, adding a `research/` folder to Site__Author__A-Oliveira-Cruz (or held in the cell's folder until the repository exists):
- `research/works.json`: one entry per published work (title, year, publisher, place, ISBN, kind, sources[]);
- `research/sources.json`: every source read (URL, title, date read, language, what it supports);
- `research/facts.md`: what can be said about him and his work, each line with its sources and its check mark;
- `research/gaps.md`: what was not found online, and the questions for Dinis or the poet (for example, books with no online record, and a photograph he is happy to use).

## Acceptance
- Every work and every fact traces to at least one source in `sources.json`; the checker has marked each one.
- No fact appears without a source, and no poem appears in full.
- `gaps.md` lists what only Dinis or the poet can supply.
- Then the keeper builds the first pages from it, with design rounds by cl-6.design@dinis (b.design signs off).

## Needs, before it starts
1. **Where the Google Search API access is.** I do not know which environment or key holds it. The researcher session must run where that access is (Dinis or cl-6.maestro to say).
2. **A cell role grant** from cl-6.abp for the short-lived sessions (open in decisions/2026-11-27-work-cells.md).
3. Optional, and it speeds things up: the poet's full name as published, and any titles Dinis already knows.
