# AURA online

**Stesse regole. Vite diverse.** Gioco formativo di ICEI sulla partecipazione giovanile, giocato dai telefoni.

👉 **Per giocare:** https://marcogiusta.github.io/aura-online/

## Come funziona

1. Sul computer collegato al proiettore aprite il link qui sopra e cliccate **«Apri una nuova stanza»**: compaiono un QR code e un codice di 4 lettere.
2. Le persone inquadrano il QR con il telefono, scrivono un nickname ed entrano. Niente app, niente email, niente dati personali.
3. **«Distribuisci i personaggi»**: il gioco sceglie i personaggi con il divario più ampio e sorteggia chi li gioca (oltre 6 persone si gioca in coppia).
4. Tutti giocano insieme, ognuno dal proprio telefono; il proiettore mostra tabellone, pedine e chi ha finito.
5. Dopo il giro 6 si scrivono i bisogni e si votano le politiche dai telefoni; alla fine traiettorie, costi delle barriere e debrief.

## Prima di ogni formazione

- Aprite la stanza sul proiettore: la scritta verde «Stanza aperta» indica che il collegamento funziona.
- Provate con 2 telefoni, uno sul Wi-Fi della sala e uno con i dati mobili.
- Tenete a portata di mano la versione offline v0.4 come piano B.

## Tecnica

Un solo file statico (`index.html`). Proiettore e telefoni si collegano direttamente (WebRTC) tramite il servizio pubblico gratuito di PeerJS. La partita è salvata nel browser del proiettore.
