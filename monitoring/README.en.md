<!-- lawwatch: written from data/checks by the check trail; edit the records, not this page -->

# Monitoring: what is read and what came of it

[Italiano](README.md)

How global-law monitors every country: [global-law monitoring/](https://github.com/lexifina/global-law/tree/main/monitoring). This page is the same for Friuli-Venezia Giulia only: every time an official source is read, when, and what came of it (acts added, changed and removed). The machine-readable form is [data/checks/](../data/checks/) (JSON Lines, schema `lexifina-check/1`), in `git log` as `Kind: check` commits, and month by month in [checks/](checks/).

**Last check:** 2026-11-24 00:29 UTC, LEXVIEW (Consiglio regionale del Friuli Venezia Giulia): 54 addresses read; 2 added, 0 changed, 0 removed; changes found; 0 not published, 0 of them with no reason.

## Sources

| Source | Folders | How often | Last successful check | Last result | State |
| --- | --- | --- | --- | --- | --- |
| [LEXVIEW (Consiglio regionale del Friuli Venezia Giulia)](https://lexview-int.regione.fvg.it/FontiNormative/xml/index.aspx) | `lr-<year>-<number>/` | daily | 2026-11-24 00:29 UTC | changes found | watched: LEXVIEW has no bulk route or list of laws: laws are read one page at a time; each held law's text is compared at least every 30 days |

## The last 30 days

| Started (UTC) | Source | Read | Added | Changed | Removed | Not published (no reason) | Result | Commits |
| --- | --- | ---: | ---: | ---: | ---: | ---: | --- | ---: |
| [2026-11-24 00:26](checks/2026-11.md#it-lexview-20261124t002600z) | lexview | 54 | 2 | 0 | 0 | 0 (0) | changes found | [3](https://github.com/lexifina/italy-friuli-venezia-giulia-law/compare/0f25929d4d8e...4cb94107b9ab) |

## Check it yourself

```
python tools/checktrail.py                      # the latest check of every source
python tools/checktrail.py --day 2026-11-23     # every check of a day
python tools/checktrail.py --act <id>           # when an act was seen and published
git log --grep='^Kind: check' --format='%ci %s'  # the checks in the history
```

Only the official publication has legal force; the texts here are copies for reading and searching.
