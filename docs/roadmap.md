# Roadmap

## Fase 1 — Raccolta dati (in corso)

Obiettivo: avere su file tutto ciò che l'app dovrà mostrare, prima di scrivere codice.

- [ ] Censire ogni laptop presente nel lab → `inventario/<id>.md`
- [ ] Per ogni modello incontrato, creare la scheda → `modelli/<slug>.md`
- [ ] Per ogni modello: specifiche e varianti
- [ ] Per ogni modello: procedura di smontaggio (testo) + video di riferimento
- [ ] Per ogni modello: elenco parti recuperabili con codice ricambio
- [ ] Per ogni parte: valore stimato con fonte e data della stima
- [ ] Rivedere `docs/requisiti.md` alla luce dei dati raccolti (campi mancanti, casi strani)

Criterio di uscita: inventario completo e ogni modello presente in inventario ha una scheda
con almeno specifiche e parti. Smontaggio e video possono restare parziali.

## Fase 2 — Progettazione

- Schema dati definitivo (derivato dal frontmatter delle schede)
- Scelta stack (vincolo: self-hosted leggero, vedi `docs/requisiti.md`)
- Mockup pagina di ricerca ID e scheda laptop

## Fase 3 — Sviluppo

- App web: ricerca per ID, scheda laptop, scheda modello, aggiornamento stato/storico
- Script di import da `inventario/` e `modelli/`

## Fase 4 — Messa in servizio

- Installazione sulla macchina del lab, backup dei dati
