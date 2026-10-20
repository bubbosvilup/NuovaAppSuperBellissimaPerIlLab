# Convenzioni di raccolta dati

## Laptop vs modello

- **Laptop** = la macchina fisica sul banco. Ha un ID univoco, uno stato e uno storico.
- **Modello** = il tipo di macchina (es. ThinkPad T480). Contiene ciò che vale per tutti gli esemplari:
  specifiche, smontaggio, video, parti e valori.

Più laptop possono puntare allo stesso modello: tutorial e parti si scrivono una volta sola.

## ID laptop

L'ID è il numero a tre cifre scritto sull'etichetta fisica del laptop (`001`, `002`, …), mai riutilizzato
(anche se il laptop viene smaltito). File: `inventario/001.md`.

Laptop ancora senza etichetta: file `inventario/senza-id-<n>.md` con `id: ~`; quando riceve l'etichetta
si rinomina il file e si compila `id`.

## ID caricatori e parti

Caricatori e parti di valore hanno un ID scritto su scotch di carta attaccato all'oggetto (es. `1A`).
L'ID è solo un'etichetta: non codifica la posizione.

## Numero intervento

Il numero della scheda di riparazione dell'e-shop va in `interventi`. Lo storico completo resta
nell'e-shop: qui non si copiano dati del cliente. Un laptop può averne più
di uno, o nessuno.

## Slug modello Apple

Per i Mac lo slug usa il codice "Model Axxxx" stampato sotto la scocca: `apple-macbook-pro-a1502`.
Lo stesso codice copre più anni con schede logiche diverse: l'anno esatto si ricava dal numero EMC,
stampato accanto, da registrare nella scheda del laptop.

## Slug modello

`marca-modello` in minuscolo con trattini, es. `lenovo-thinkpad-t480`, `hp-elitebook-840-g5`.
Se la variante cambia le parti (es. con/senza GPU dedicata) si usa uno slug separato.
File: `modelli/<slug>.md`.

## Stati del laptop

| Stato | Significato |
|-------|-------------|
| `arrivato` | in lab, non ancora esaminato |
| `in-diagnosi` | in esame |
| `da-riparare` | riparabile, in attesa di intervento o ricambi |
| `riparato` | funzionante |
| `da-smontare` | destinato al recupero parti |
| `smontato` | parti recuperate |
| `smaltito` | uscito dal lab |

Ogni cambio di stato si registra anche nella sezione *Storico* della scheda, con la data.

## Valori sconosciuti

Si lascia il campo vuoto (`~` in YAML), non si inventa. Se un dato è incerto si scrive nelle note
con un `?` (es. "RAM 8GB?").

## Valore delle parti

Ogni stima riporta fonte e data (es. `eBay usato, 2026-10`): i prezzi dell'usato cambiano.

## Indici

`inventario/INDEX.md` e `modelli/INDEX.md` si aggiornano a ogni nuova scheda o cambio di stato.
