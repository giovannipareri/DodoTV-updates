# DodoTV Updates

Canale pubblico per gli aggiornamenti di DodoTV Android e Tizen. I file pubblicati qui saranno scaricabili senza account GitHub; il codice dell’app rimane nella repository privata.

## Stato attuale

Repository predisposta. Nessun pacchetto o aggiornamento automatico degli adattatori è ancora disponibile in questo canale. L’app deve ancora integrare il controllo e la verifica delle patch.

- `updates/stable.json`: indice iniziale disabilitato, senza pacchetti.
- `PUBLISHING.md`: regole per pubblicare pacchetti e metadati verificabili.
- Le release ospiteranno soltanto i file destinati alla distribuzione, checksum e firme pubbliche.

Le future patch devono essere firmate e compatibili con il runtime della piattaforma. La firma dell’APK Android e quella del WGT Samsung sono distinte dalla firma degli aggiornamenti dei risolutori. Le chiavi private restano fuori da questa repository e dall’app.

I pacchetti vengono attivati alla riproduzione successiva, senza interrompere un video in corso; l’app deve conservare una versione precedente per il ripristino. Queste sono regole del sistema da implementare, non funzionalità già attive.
