# How this repository was made (Friuli-Venezia Giulia)

This file is written by the build on 2026-11-02, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Consiglio regionale del Friuli Venezia Giulia, LEXVIEW (banca dati delle leggi regionali) | <https://lexview-int.regione.fvg.it/FontiNormative/xml/index.aspx> | 2026-11-02 | L. 633/1941 art. 5 (official acts are not protected; this record relies on that exemption). Site note legali: download for personal, non-commercial use; reproduction for other ends needs prior authorisation. LEXVIEW itself: electronic reproduction allowed citing the source, the non-authentic character and free of charge. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `lr-1964-002` | L.R. 9 settembre 1964, n. 2: Determinazione delle indennità di carica spettanti al Presidente del Consiglio Regionale, al Presidente della Giunta Regionale ed agli Assessori e determinazione dell' indennità di presenza dei Consiglieri. | 1 | 2026-11-02 to 2026-11-02 |
| `lr-1965-005` | L.R. 21 aprile 1965, n. 5: Servizio di Tesoreria della Regione Friuli - Venezia Giulia. | 1 | 2026-11-02 to 2026-11-02 |
| `lr-1965-010` | L.R. 12 luglio 1965, n. 10: Acquisto da parte della Regione Friuli - Venezia Giulia di cartelle fondiarie, di nuova emissione, della Sezione autonoma del Credito fondiario della Cassa di Risparmio di Gorizia. | 1 | 2026-11-02 to 2026-11-02 |
| `lr-1965-014` | L.R. 13 agosto 1965, n. 14: Acquisto di obbligazioni dell' Istituto di Credito per il finanziamento a medio termine alle piccole e medie imprese situate nel territorio della Provincia di Udine. | 1 | 2026-11-02 to 2026-11-02 |
| `lr-1965-018` | L.R. 31 agosto 1965, n. 18: Intervento della Regione nella spesa per le opere pubbliche di interesse agrario e forestale. | 1 | 2026-11-02 to 2026-11-02 |
| `lr-1965-020` | L.R. 14 ottobre 1965, n. 20: Autorizzazione all' acquisto di beni immobili per uffici, enti ed istituti, dipendenti dalla Regione. | 1 | 2026-11-02 to 2026-11-02 |
| `lr-1965-023` | L.R. 29 ottobre 1965, n. 23: Sovvenzioni, contributi, sussidi e spese dirette, per finalità istituzionali. | 1 | 2026-11-02 to 2026-11-02 |
| `lr-1965-031` | L.R. 17 dicembre 1965, n. 31: Istituzione del Comitato tecnico - consultivo regionale per la finanza. | 1 | 2026-11-02 to 2026-11-02 |

The build made 8 commits:

| Commits | Kind |
| ---: | --- |
| 8 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `futuro`: laws not yet in force on 2026-11-02.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 8 laws in the record.
- 8 tags.

## Dates

Each commit is dated at noon (Europe/Rome) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Statuto speciale della Regione Friuli-Venezia Giulia (legge costituzionale 31 gennaio 1963, n. 1), art. 29: regional laws are published in the Bollettino Ufficiale and enter into force on the fifteenth day after publication, unless they set another term. Not used for dating: each text is dated the day it was read. https://lexview-int.regione.fvg.it/FontiNormative/xml/index.aspx

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `80cf5ff8b547998b13e0f7719023a7aefdcd66d82ce7e303112281db369d4c56` (33751 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3d00541d258745461ab52b1b0cb4e1716a27a95d`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

8 versions of 8 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Every regional law LEXVIEW publishes is included, found by number year by year (a missing number answers an empty page); laws it marks as repealed in full ("Legge abrogata"), and laws all of whose articles are repealed, are left out. Regulations are not included.
- Each law is recorded by its text in force on the retrieval day only, as its oldest version available, dated that day and credited to the database as publisher.
- The editor's notes (note markers, "Note:" lists, notes on the whole law) and the editor's corrections ("Correzioni effettuate d'ufficio") are not copied. Repealed articles stay as printed, "( ABROGATO )".
- Units: anything before the first article (preambolo), one file per article; headings of titles, chapters and sections go with the next article.
- A law whose page does not read back letter for letter under a second, independent reader is left out.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- A model (Claude) wrote the fetch and parse code; it wrote no law text. Every word of law comes from LEXVIEW, the Consiglio regionale del Friuli Venezia Giulia's law database.
