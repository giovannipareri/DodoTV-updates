# DodoTV updates

Canale pubblico degli adattatori HTTP per DodoTV Android e Tizen. La repository principale e le release complete delle app restano private. Nessun login GitHub richiesto ai dispositivi per leggere questo canale.

Primo bundle firmato API 1: 1794219686. Compatibile con la nuova generazione del client aggiornamenti (Android 1.0.28 o successiva e Tizen 1.1.4 o successiva, dopo completamento delle rispettive build); le vecchie app non consultano questo canale. Il primo pacchetto contiene gli stessi quattro adattatori della build, per inizializzare il canale senza cambiare i flussi.

- Indice: updates/stable.json, firma separata updates/stable.json.sig.
- Pacchetti: bundles/ oppure asset delle release adapters-<sequenza>.
- Verifiche: firma RSA-SHA256 con chiave pubblica incorporata nell'app, hash SHA256, dimensioni, compatibilità e sequenza antireplay.
- Attivazione: successivo avvio del servizio, dopo download verificato; rollback se l'inizializzazione del pacchetto fallisce.

La firma valida attesta la provenienza del pacchetto, non la disponibilità futura dei siti. Nuovi download rifiutati dopo la scadenza dell'indice; adattatori già installati utilizzabili offline. Nessuna chiave privata, credenziale o cookie viene pubblicato. Sorgenti degli adattatori e LICENSE sono inclusi intenzionalmente.

Vedi [PUBLISHING.md](PUBLISHING.md) per la procedura di pubblicazione.
