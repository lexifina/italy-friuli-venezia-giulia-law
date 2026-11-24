<!-- lawwatch: written from data/checks by the check trail; edit the records, not this page -->

# Monitoraggio: che cosa si legge e con quale esito

[English](README.en.md)

Come global-law monitora ogni paese: [global-law monitoring/](https://github.com/lexifina/global-law/tree/main/monitoring). Questa pagina fa lo stesso per Friuli Venezia Giulia soltanto: ogni lettura di una fonte ufficiale, quando è avvenuta e con quale esito (atti aggiunti, modificati e rimossi). La forma leggibile dalle macchine è [data/checks/](../data/checks/) (JSON Lines, schema `lexifina-check/1`), in `git log` come commit `Kind: check`, e mese per mese in [checks/](checks/).

**Ultimo controllo:** 2026-11-24 00:29 UTC, LEXVIEW (Consiglio regionale del Friuli Venezia Giulia): 54 indirizzi letti; 2 aggiunti, 0 modificati, 0 rimossi; modifiche trovate; 0 non pubblicati, di cui 0 senza motivo.

## Fonti

| Fonte | Cartelle | Frequenza | Ultimo controllo riuscito | Ultimo esito | Stato |
| --- | --- | --- | --- | --- | --- |
| [LEXVIEW (Consiglio regionale del Friuli Venezia Giulia)](https://lexview-int.regione.fvg.it/FontiNormative/xml/index.aspx) | `lr-<year>-<number>/` | ogni giorno | 2026-11-24 00:29 UTC | modifiche trovate | sorvegliata: LEXVIEW non offre download massivi né un elenco delle leggi: le leggi si leggono una pagina alla volta; il testo di ogni legge presente qui è confrontato almeno ogni 30 giorni |

## Gli ultimi 30 giorni

| Inizio (UTC) | Fonte | Letti | Aggiunti | Modificati | Rimossi | Non pubblicati (senza motivo) | Esito | Commit |
| --- | --- | ---: | ---: | ---: | ---: | ---: | --- | ---: |
| [2026-11-24 00:26](checks/2026-11.md#it-lexview-20261124t002600z) | lexview | 54 | 2 | 0 | 0 | 0 (0) | modifiche trovate | [3](https://github.com/lexifina/italy-friuli-venezia-giulia-law/compare/0f25929d4d8e...4cb94107b9ab) |

## Verificalo da te

```
python tools/checktrail.py                      # l'ultimo controllo di ogni fonte
python tools/checktrail.py --day 2026-11-23     # tutti i controlli di un giorno
python tools/checktrail.py --act <id>           # quando un atto è stato visto e pubblicato
git log --grep='^Kind: check' --format='%ci %s'  # i controlli nella cronologia
```

Ha valore legale solo la pubblicazione ufficiale; i testi qui sono copie per la lettura e la ricerca.
