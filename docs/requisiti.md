# Requisiti

## Scopo

Strumento interno del lab. Ogni laptop rotto riceve un ID; cercando l'ID si apre la scheda con:

- storico della macchina (arrivo, diagnosi, interventi, destinazione finale)
- modello e specifiche
- tutorial di smontaggio: testo scritto + video incorporati
- parti da smontare e valore stimato di ciascuna

## Vincoli

- Nessun dato personale sensibile.
- Hosting self-hosted leggero (PC sempre acceso, Raspberry Pi o mini PC); hosting pubblico non escluso.
- Stack semplice: pochi servizi, database su file (es. SQLite).

## Decisioni (2026-10-20)

- **Utenti:** l'app la usa solo il lab.
- **Rapporto con l'e-shop:** l'app non sostituisce l'e-shop. Lo storico delle riparazioni resta nell'e-shop:
  qui si registra solo il numero di intervento come riferimento. Serve a catalogare laptop, caricatori e parti.
- **Nessun dato personale:** né del cliente né di chi esegue l'intervento.
- **Parti con ID proprio:** solo le parti di valore (es. SSD, schermi, schede); le altre si tracciano
  solo come provenienti da un laptop.
- **Etichette:** ogni oggetto sparso (laptop, caricatore, parte di valore) ha l'ID scritto a mano
  su scotch di carta. Nessuna etichetta stampata per ora.
- **QR code:** servirà per far accedere i clienti all'app (vedi domande aperte).

## Domande aperte

- I clienti accedono via QR: cosa vedono? (catalogo parti/laptop in vendita? solo una pagina informativa?)
  Va conciliato con "l'app la usa solo il lab": probabile area pubblica in sola lettura + area lab.
