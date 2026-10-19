# NuovaAppSuperBellissimaPerIlLab

Web app interna del lab: ogni laptop rotto riceve un **ID**; inserendo l'ID si apre la sua scheda
con storico, modello, tutorial di smontaggio (testo + video), parti recuperabili e valore stimato.

## Fasi

| Fase | Cosa | Stato |
|------|------|-------|
| 1. Raccolta dati | Censire i laptop presenti, i modelli e la documentazione di smontaggio/parti | **in corso** |
| 2. Progettazione | Schema dati definitivo, scelta stack, mockup | da fare |
| 3. Sviluppo | App web + import dei dati raccolti | da fare |
| 4. Messa in servizio | Hosting nel lab, backup | da fare |

Dettagli in [docs/roadmap.md](docs/roadmap.md).

## Struttura

```
inventario/          una scheda per ogni laptop fisico (ID = numero sull'etichetta, es. 001)
  INDEX.md           tabella riepilogativa di tutto l'inventario
modelli/             una scheda per ogni modello: specifiche, smontaggio, parti, video
  INDEX.md           elenco dei modelli
docs/                documentazione di progetto (requisiti, convenzioni, roadmap)
templates/           modelli vuoti delle schede
```

Le schede sono Markdown con frontmatter YAML: leggibili a mano adesso, importabili nel database
dell'app in fase 3. Le regole di compilazione sono in [docs/convenzioni.md](docs/convenzioni.md).
