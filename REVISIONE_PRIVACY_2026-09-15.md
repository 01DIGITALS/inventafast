# Revisione della bozza privacy — 15 settembre 2026

## Esito e perimetro

Aggiornata PRIVACY_BOZZA_IT.md su richiesta del titolare. È una bozza revisionata, non una certificazione di conformità né una pagina definitiva per Google Play.

Confermati dall'utente: Louis Sanges come titolare, LouisBigDev come sviluppatore, louisbigdev@hotmail.com come contatto e 6 mesi dalla chiusura per le email di assistenza. Aggiunta la cancellazione anticipata su richiesta quando applicabile, senza ingiustificato ritardo; non una promessa incondizionata di cancellazione istantanea. Il limite ordinario evita di conservare email indefinitamente in assenza di richieste.

La revisione del codice è stata svolta direttamente in sola lettura sul progetto Android locale. La richiesta di un secondo controllo alla task “Definisci InventaFast” non è stata consegnata: l'app segnala che la task ha già un processo di scrittura attivo. Successivamente l'utente ha riportato la raccomandazione della task e Work ha letto direttamente il rapporto locale aggiornato `mobile/store/VERIFICA_PRIVACY_0.2.0.md`. L'allineamento seguente si basa su quel rapporto e sulle fonti Google; non si dichiara riuscita la consegna diretta.

## Riscontri tecnici

Percorsi relativi alla cartella mobile del progetto di sviluppo, non a questo repository pubblico:

| Dichiarazione | Riscontro letto | Limite |
| --- | --- | --- |
| Inventario locale | lib/platform/mobile_services.dart e lib/engine/database.dart: SQLite privato, schema prodotti/magazzini/conteggi/preferenze | Non è una prova universale dell'assenza di traffico degli SDK |
| Scanner incluso | android/gradle.properties: useUnbundled=false; mobile_scanner 7.4.2, dipendenza bundled com.google.mlkit:barcode-scanning:17.3.0 | Documentazione Google corrente da confrontare con la versione distribuita |
| Immagini e zoom | MobileScanSession; default del plugin returnImage=false e autoZoom=false | Non effettuata una nuova cattura di rete o prova ottica |
| Rete release | android/app/src/release/AndroidManifest.xml rimuove INTERNET; manifest unificato disponibile di versione 0.2.0, codice 2, conferma l'assenza | Presenza di componenti ML Kit/DataTransport e servizi Google; non conclusivo su IPC o attività di altri processi |
| Acquisti | lib/platform/store_gateway.dart, lib/licensing/purchases.dart e MainActivity.kt: ricezione acquisto, verifica firma locale, conferma al servizio Play | Non collaudato qui un acquisto reale sulla release firmata; dati amministrativi della Console da mappare |
| Licenza | lib/licensing/license_controller.dart e lib/platform/license_storage.dart: demo 7 giorni, date locali, stato purchased/clockBlocked in secure storage | “Ultima data verificata” corretto in “ultima data osservata”; nessuna certificazione oraria remota |
| Export | lib/platform/export_files.dart: generazione locale, cartelle exports nell'area app, share sheet | Copie esterne sotto il controllo dei destinatari |
| Cancellazione | lib/engine/inventory_engine.dart: reset conteggi, cancellazione prodotti e valori appresi; schema con cancellazione a cascata | Nome azienda, magazzini, preferenze e report non cancellati dal comando archivio |
| Backup | allowBackup=false e esclusioni cloud/device-transfer in data_extraction_rules.xml | Nessuna prova su tutti i produttori o cancellazione di vecchie copie |

L'audit preesistente AUDIT_GOOGLE_PLAY_2026-09-15.md è stato usato soltanto come contesto: contiene riferimenti a una versione precedente senza acquisti e non è stato assunto come fotografia completa della versione attuale. Nessuna nuova build, prova su dispositivo, modifica del codice o caricamento nello store effettuati in questa revisione.

## Allineamento con la verifica tecnica aggiornata

Si mantiene ML Kit bundled per la prima versione. La scelta privilegia l'integrazione già collaudata; non dimostra superiorità rispetto a ZXing-C++, che richiederebbe integrazione e prove comparative. Non è una conclusione sulla liceità della diagnostica.

Il rapporto aggiornato riguarda InventaFast Android 0.2.0+2, AAB di 67.939.807 byte, SHA-256 `2ae4fba15ca7ea7739c91ed127aa02aacb5e22aabe7f265c0bad8307cf62c039`. Sostituisce il precedente hash `4dd4fef1b3f70f56c72403a5944fff841db1a06a438ba361c46ecc6ce4859861`.

Il rapporto conferma nei DEX del nuovo bundle il percorso ML Kit verso Google Play Services (`mlkit:vision`, servizio telemetry e `IClientTelemetryService`), con 38 riferimenti pertinenti nella mappa R8. È chiusa l'incertezza sulla presenza del percorso diagnostico. Non si richiede un test senza traffico per dimostrarne l'assenza: un simile test non sarebbe conclusivo.

Risultati riportati dalla task tecnica: 56 test Flutter superati, analisi Dart senza issue, Android Lint 0 errori e 3 avvisi, verifiche native di allineamento a 16 KB superate, avvio e fotocamera sull'emulatore x86_64 a 16 KB riusciti. Work ha letto il rapporto, non ha rieseguito questi collaudi. Restano distinti il candidato firmato per Play, i pagamenti/ripristini reali e il collaudo ARM64 a 16 KB.

La sezione scanner della policy ora dichiara le metriche Google e distingue riconoscimento locale e diagnostica. Non contiene una promessa di assenza di raccolta. Email e conservazione sono già confermate dal titolare: le indicazioni contrarie rimaste in fondo al rapporto locale sono superate dalle conferme riportate all'inizio di questo documento.

## Prima della versione definitiva

1. Completare l'inquadramento giuridico della diagnostica confermata: ruoli, base giuridica, conservazione pertinente ed eventuale informazione/consenso in app. Le pagine ML Kit consultate descrivono metriche e finalità ma non forniscono, da sole, una base giuridica specifica per questa integrazione o un periodo unico di conservazione. Non inventare un consenso già raccolto o attribuire automaticamente il legittimo interesse. Confermare che il candidato firmato mantenga la configurazione verificata. Non usare il permesso fotocamera come consenso alla diagnostica.
2. Mappare ordini, rimborsi, report finanziari e diagnostica eventualmente accessibili al titolare in Play Console, comprese copie esportate, destinatari amministrativi e obblighi di conservazione applicabili. La sola ispezione del codice non verifica questi trattamenti.
3. Attuare operativamente la cancellazione delle email dopo 6 mesi e su richiesta quando dovuta, incluse le copie gestite dal titolare. Verificare condizioni del servizio email, ruoli e garanzie applicabili al suo effettivo utilizzo; non presumere un accordo da responsabile del trattamento solo perché la casella è Hotmail.
4. Valutare e documentare il bilanciamento prima di usare il legittimo interesse per la difesa di diritti; non estenderlo indiscriminatamente a telemetria o marketing.
5. Prima di rimuovere il carattere di bozza, verificare completezza dell'informativa per tutti i trattamenti effettivi, eventuali ulteriori recapiti/ruoli necessari e coerenza con il modulo Sicurezza dei dati.
6. Pubblicare poi una pagina HTTPS accessibile senza login e non PDF, collegata anche dall'app. Rivalutare il trattamento dei visitatori per l'hosting finale. Questa revisione non attiva GitHub Pages e non certifica la conformità agli store.

## Fonti consultate

- [Garante: principi e contenuti dell'informativa](https://www.garanteprivacy.it/home/principi-fondamentali-del-trattamento): finalità, basi giuridiche, destinatari, trasferimenti e conservazione.
- [Garante: diritti degli interessati](https://www.garanteprivacy.it/regolamentoue/diritti-degli-interessati): esercizio dei diritti e termini di risposta.
- [Garante: diritti e cancellazione](https://www.garanteprivacy.it/home/i-miei-diritti/diritti): condizioni del diritto alla cancellazione.
- [iubenda: struttura dell'informativa](https://www.iubenda.com/it/help/105832-modello-informativa-privacy/): testo personalizzato ai trattamenti reali, linguaggio chiaro, contatti, basi, terzi, diritti e aggiornamenti. Usato come guida editoriale, non come fonte normativa o certificazione; non copiate clausole del modello.
- [Google ML Kit: Terms & Privacy](https://developers.google.com/ml-kit/terms): elaborazione degli input sul dispositivo distinta dalle metriche inviate a Google.
- [Google ML Kit: data disclosure](https://developers.google.com/ml-kit/android-data-disclosure): diagnostica, informazioni dispositivo/app e identificativi anche per funzioni bundled.
- [Google: privacy](https://policies.google.com/privacy?hl=it) e [trasferimenti](https://policies.google.com/privacy/frameworks?hl=it).
- [Microsoft: privacy](https://www.microsoft.com/it-it/privacy/privacystatement): Outlook/Hotmail e garanzie di trasferimento.
- [GitHub: privacy](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement): consultazione del repository.
- [Android: backup](https://developer.android.com/identity/data/autobackup): configurazione dei backup e del trasferimento.
- [Google Play: User Data](https://support.google.com/googleplay/android-developer/answer/10144311): responsabilità sugli SDK e requisiti della pagina privacy.

EUR-Lex è stato consultato ma la lettura automatica del testo integrale è stata bloccata dal controllo del sito; per questa revisione sono state utilizzate le spiegazioni ufficiali del Garante sopra indicate. Non si presenta come effettuata una lettura integrale del Regolamento da EUR-Lex.
