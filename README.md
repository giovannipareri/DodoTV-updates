# DodoTV updates

Canale pubblico degli adattatori HTTP per DodoTV Android e Tizen. La repository principale e le release complete delle app restano private. Nessun login GitHub richiesto ai dispositivi per leggere questo canale.

Chiave ruotata il 9 novembre 2026 su richiesta del proprietario. Il pacchetto corrente richiede **Android 1.0.30 o successiva e Tizen 1.1.6 o successiva** con la nuova chiave pubblica incorporata. Le versioni precedenti rifiutano la nuova firma: aggiornare le app. La firma di installazione Android e gli identificativi delle app restano invariati.

Bundle firmato API 1 corrente: **1794222477**. Contiene gli stessi quattro adattatori delle nuove app. Impronta SHA256 della chiave pubblica (SPKI DER): `476da7d1786668fac68df713fe8fffcf38871b5bb28531b8a84666915ef44b05`.


- Indice: updates/stable.json, firma separata updates/stable.json.sig.
- Pacchetti: bundles/ oppure asset delle release adapters-<sequenza>.
- Verifiche: firma RSA-SHA256 con chiave pubblica incorporata nell'app, hash SHA256, dimensioni, compatibilità e sequenza antireplay.
- Attivazione: successivo avvio del servizio, dopo download verificato; rollback se l'inizializzazione del pacchetto fallisce.

La firma valida attesta la provenienza del pacchetto, non la disponibilità futura dei siti. Nuovi download rifiutati dopo la scadenza dell'indice; adattatori già installati utilizzabili offline. Nessuna chiave privata, credenziale o cookie viene pubblicato. Sorgenti degli adattatori e LICENSE sono inclusi intenzionalmente.

Vedi [PUBLISHING.md](PUBLISHING.md) per la procedura di pubblicazione.
