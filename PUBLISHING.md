# Pubblicazione degli aggiornamenti

Questa repository è pubblica. Pubblicare soltanto file intenzionalmente distribuibili: niente sorgenti privati, token, cookie, dati utente o chiavi private. Un adattatore eseguibile distribuito come patch è comunque scaricabile e ispezionabile da chiunque; mantenere privata la repository di sviluppo non rende segreto il codice incluso nella patch.

## Prima di attivare il canale

1. Implementare e verificare il client Android/Tizen: formato del manifest, verifica della firma, compatibilità, limiti di dimensione e gestione degli errori.
2. Configurare una chiave di firma per gli aggiornamenti; incorporare la chiave pubblica attendibile nell’app. La chiave privata deve rimanere nel sistema di pubblicazione. Un checksum da solo non dimostra la provenienza.
3. Definire versioni monotone, scadenza dei metadati e protezione contro il riutilizzo di manifest vecchi. Prevedere la rotazione delle chiavi senza fidarsi di chiavi inviate da un manifest non ancora verificato.
4. Abilitare l’indice soltanto quando almeno un pacchetto firmato è stato provato sul runtime supportato. L’indice iniziale enabled=false è preparatorio e non autorizza alcun aggiornamento.

## Pubblicazione futura

- Compilare e testare nel progetto privato, esportando soltanto i file di distribuzione.
- Caricare una release con file immutabili identificati dalla versione: pacchetto, dimensione, SHA-256 e firma/metadati firmati.
- Pubblicare per ultimo l’indice aggiornato, dopo aver verificato che tutti gli asset siano scaricabili senza login. Non inserire URL temporanei o link a release private.
- Firmare i byte esatti dell’indice; il client deve verificare i byte prima di interpretare e applicare la configurazione. Specificare il formato crittografico nel protocollo definitivo, non inventarlo diversamente fra client e publisher.
- Dichiarare piattaforma, versione minima/massima del runtime e API dell’adattatore. Android Node Mobile e servizio Tizen non sono runtime intercambiabili.
- Scaricare in staging, verificare firma/hash/dimensione/compatibilità, attivare atomicamente a riproduzione terminata e mantenere la versione precedente. Il ripristino locale non deve autorizzare qualsiasi downgrade scaricato dalla rete.

## Permessi del sistema di build

Il GITHUB_TOKEN della repository privata non concede automaticamente accesso in scrittura a questa repository separata. Configurare una credenziale di pubblicazione dedicata con permessi limitati a questo canale, custodita nei secret della CI privata. Non inserirla nelle app, nei file pubblici o negli artifact.

La distribuzione degli APK e dei WGT completi resta distinta dalle patch: Android può richiedere la conferma di installazione del sistema; un WGT richiede la firma Samsung e il metodo di installazione previsto dalla TV. Questo canale non elimina tali requisiti.
