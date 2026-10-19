# Progetto

Web app del lab per schede laptop cercabili per ID. Fase attuale: **raccolta dati** (vedi `docs/roadmap.md`).
Niente codice applicativo finché la fase 1 non è chiusa.

## Quando l'utente comunica dati su laptop o modelli

1. Segui `docs/convenzioni.md` (formato ID, slug, stati, valori sconosciuti).
2. Laptop nuovo → copia `templates/laptop.md` in `inventario/<id>.md` (ID = numero sull'etichetta fisica,
   lo comunica l'utente; senza etichetta → `senza-id-<n>.md`).
3. Modello nuovo → copia `templates/modello.md` in `modelli/<slug>.md`; specifiche, parti e smontaggio
   si possono ricercare, ma ogni dato non fornito dall'utente va marcato con la fonte.
4. Aggiorna `inventario/INDEX.md` e `modelli/INDEX.md`.
5. Domande aperte emerse → `docs/requisiti.md`, sezione *Domande aperte*.
