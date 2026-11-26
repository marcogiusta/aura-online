# AURA online

**Stesse regole. Vite diverse.** Gioco formativo di ICEI sulla partecipazione giovanile, giocato dai telefoni.

👉 **Per giocare:** https://marcogiusta.github.io/aura-online/

## Come funziona

1. Sul computer collegato al proiettore aprite il link qui sopra e cliccate **«Apri una nuova stanza»**: compaiono un QR code e un codice di 4 lettere.
2. Le persone inquadrano il QR con il telefono, scrivono un nickname ed entrano. Niente app, niente email, niente dati personali.
3. **«Distribuisci i personaggi»**: il gioco sceglie i personaggi con il divario più ampio e sorteggia chi li gioca (oltre 6 persone si gioca in coppia).
4. **«Regole e via!»**: 9 diapositive con le regole sul proiettore (frecce ← → o telecomando); sui telefoni compare il riassunto. Si possono rivedere con «📽 Regole».
5. Tutti giocano insieme, ognuno dal proprio telefono. Il proiettore **racconta** ogni mossa: situazione, scelta (e alternative non possibili), effetti, carte AURA, risorse del personaggio. A fine giro, il riepilogo «Stesso giro, vite diverse» con una domanda per la discussione.
6. Eventi Mondo dopo i giri 4, 7 e 9. Dopo il giro 8 si scrivono i bisogni e si votano le politiche dai telefoni; alla fine traiettorie, costi delle barriere e debrief.

## Prima di ogni formazione

- Aprite la stanza sul proiettore: la scritta verde «Stanza aperta» indica che il collegamento funziona.
- Provate con 2 telefoni, uno sul Wi-Fi della sala e uno con i dati mobili.
- Se il collegamento diretto è bloccato dalla rete, il telefono passa da solo alla **via di riserva** (broker MQTT pubblici, messaggi cifrati): pallino giallo invece che verde, si gioca uguale.
- Se un telefono non si collega comunque, sullo schermo trova il motivo e che cosa fare (cambiare rete, riprovare).
- Per reti difficili si può aggiungere un relay TURN gratuito di Metered: aprite il gioco con `?turn=NOMEAPP:APIKEY` (il QR lo passa ai telefoni).
- Tenete a portata di mano la versione offline v0.4 come piano B.

## Tecnica

Un solo file statico (`index.html`). Proiettore e telefoni si collegano direttamente (WebRTC) tramite il servizio pubblico gratuito di PeerJS; se la rete lo blocca, via di riserva su broker MQTT pubblici (EMQX, HiveMQ, Eclipse) con messaggi cifrati AES-GCM. La partita è salvata nel browser del proiettore.
