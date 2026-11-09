# Pubblicazione del canale

La repository privata DodoTV contiene scripts/build-adapter-update.cjs e scripts/publish-adapter-update.cjs. La chiave privata dedicata rimane esterna al sorgente e deve corrispondere alla chiave pubblica fissata nei client.

1. Validare i quattro adattatori e la compatibilità API 1 su entrambe le piattaforme.
2. Generare il bundle JSON e l'indice con sequenza crescente, hash/dimensione, scadenza e firma separata RSA-SHA256 sui byte esatti dell'indice.
3. Pubblicare prima il bundle e LICENSE; aggiornare indice e firma nello stesso commit. Non sovrascrivere bundle già distribuiti.
4. Verificare lettura anonima, firma e attivazione al successivo avvio.

Il publisher CI privato richiede i secret DODOTV_UPDATE_PRIVATE_KEY e DODOTV_UPDATES_TOKEN; il secondo autorizza Contents write esclusivamente su questa repository. Secret configurati dal proprietario e verificati il 9 novembre 2026: pubblicazione automatica della sequenza 1794228042 riuscita, inclusi download anonimo e attivazione su entrambi i client. Il workflow manuale DodoTV adapter updates nella repository privata permette di pubblicare e verificare il canale senza ricompilare le app.

Non committare chiavi private, token, cookie, keystore o certificati Samsung. Il token serve esclusivamente al publisher e non va incluso nelle app. Non modificare schema API, nomi dei quattro moduli o chiave pubblica senza aggiornare i client. Conservare GPLv3 e provenienza dei sorgenti.
