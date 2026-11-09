# DodoTV updates

Canale pubblico degli adattatori HTTP per DodoTV Android e Tizen. La repository principale e le release complete delle app restano private. Nessun login GitHub richiesto ai dispositivi per leggere questo canale.

Chiave ruotata il 9 novembre 2026 su richiesta del proprietario. Il pacchetto corrente richiede **Android 1.0.30 o successiva e Tizen 1.1.6 o successiva** con la nuova chiave pubblica incorporata. Le versioni precedenti rifiutano la nuova firma: aggiornare le app. La firma di installazione Android e gli identificativi delle app restano invariati.

Il pacchetto API 1 corrente è indicato da `updates/stable.json`. La baseline della rotazione è la sequenza 1794222477. Contiene gli stessi quattro adattatori delle nuove app. Impronta SHA256 della chiave pubblica (SPKI DER): `476da7d1786668fac68df713fe8fffcf38871b5bb28531b8a84666915ef44b05`.


- Indice: updates/stable.json, firma separata updates/stable.json.sig.
- Pacchetti: bundles/ oppure asset delle release adapters-<sequenza>.
- Verifiche: firma RSA-SHA256 con chiave pubblica incorporata nell'app, hash SHA256, dimensioni, compatibilità e sequenza antireplay.
- Attivazione: successivo avvio del servizio, dopo download verificato; rollback se l'inizializzazione del pacchetto fallisce.

La firma valida attesta la provenienza del pacchetto, non la disponibilità futura dei siti. Nuovi download rifiutati dopo la scadenza dell'indice; adattatori già installati utilizzabili offline. Nessuna chiave privata, credenziale o cookie viene pubblicato. Sorgenti degli adattatori e LICENSE sono inclusi intenzionalmente.

Vedi [PUBLISHING.md](PUBLISHING.md) per la procedura di pubblicazione.


Automazione verificata il 9 novembre 2026: i secret configurati dal proprietario hanno firmato e pubblicato la sequenza 1794228042 come asset della release pubblica. Download anonimo, firma/hash e attivazione al successivo avvio verificati con il client Android e Tizen. Gli aggiornamenti futuri sono identificati dall’indice, senza modificare questo README a ogni pubblicazione.
