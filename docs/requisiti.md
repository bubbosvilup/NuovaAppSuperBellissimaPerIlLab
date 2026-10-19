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

## Domande aperte

Da chiudere durante la raccolta dati.

- Chi usa l'app? Solo chi lavora nel lab o anche esterni in sola lettura?
- Serve tracciare chi ha fatto cosa nello storico?
- Le parti smontate vanno inventariate singolarmente (con un proprio ID) o basta sapere da quale laptop vengono?
- Serve stampare etichette/QR con l'ID da attaccare ai laptop?
