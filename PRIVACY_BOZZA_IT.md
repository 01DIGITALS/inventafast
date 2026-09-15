# Informativa privacy — InventaFast per Android

**Bozza revisionata il 15 settembre 2026 — non ancora definitiva per lo store.**
Il contatto e la durata di conservazione delle email sono stati confermati dal titolare.
La verifica tecnica aggiornata conferma la presenza della diagnostica Google. ML Kit viene mantenuto per questa versione. Restano da completare l'inquadramento giuridico della diagnostica e dei trattamenti amministrativi degli acquisti, riportati nelle [note di revisione](REVISIONE_PRIVACY_2026-09-15.md).

## 1. Titolare e contatti

Il titolare dei trattamenti svolti per fornire assistenza e gestire il rapporto con gli utenti è **Louis Sanges**, sviluppatore di InventaFast con il nome **LouisBigDev**.

Per assistenza e richieste relative ai dati personali: **[louisbigdev@hotmail.com](mailto:louisbigdev@hotmail.com)**.

Questa informativa riguarda InventaFast per Android. Non descrive una futura versione iOS né sostituisce le informative dei servizi esterni scelti dall'utente.

## 2. In sintesi

- L'inventario è conservato sul dispositivo. Non è richiesto un account InventaFast e non è presente una sincronizzazione con server dello sviluppatore.
- La fotocamera serve a leggere i codici a barre; i fotogrammi sono elaborati sul dispositivo e l'app non salva fotografie o video.
- Gli acquisti sono gestiti da Google Play. Lo sviluppatore non riceve dall'app i dati della carta di pagamento.
- Excel e PDF sono generati localmente. La condivisione avviene soltanto quando l'utente la richiede e sceglie un destinatario.
- Le email inviate all'assistenza sono ricevute e trattate dal titolare.
- L'elaborazione locale dello scanner non equivale all'assenza di diagnostica dei componenti Google: si veda la sezione 5.

## 3. Dati dell'inventario e funzionamento locale

L'app memorizza nome dell'azienda e dei magazzini, articoli, codici a barre, formati, materiali, unità di misura, classificazioni, quantità, date delle operazioni, preferenze e identificativi interni necessari a collegare le registrazioni. Il riutilizzo di materiali e packaging deriva dalle voci dell'archivio locale; non comporta l'invio del catalogo a un servizio di intelligenza artificiale.

Il nome di un'azienda o il contenuto di un campo libero può contenere dati personali, ad esempio quando identifica una persona fisica. Inserire soltanto informazioni necessarie all'inventario.

Il codice applicativo non invia automaticamente l'inventario allo sviluppatore. Se un'impresa utilizza l'app per trattare dati personali di altre persone per proprie finalità, deve valutarne autonomamente la liceità e gli obblighi informativi. La fornitura del software non attribuisce allo sviluppatore l'accesso a tali dati.

Nella versione esaminata non risultano pubblicità, account applicativi o strumenti di analisi del comportamento integrati dallo sviluppatore. I componenti Google e la loro diagnostica sono descritti separatamente.

## 4. Demo, licenza e acquisti

La demo dura sette giorni dal primo avvio e non comporta addebiti automatici. Alla scadenza l'archivio non viene cancellato e rimane disponibile l'esportazione. Lo sblocco è un acquisto unico, senza abbonamento; il prezzo viene mostrato da Google Play prima della conferma.

Per gestire la demo e lo sblocco offline, l'app conserva separatamente dall'inventario la data di inizio demo, l'ultima data osservata dall'app, lo stato dello sblocco e un indicatore di anomalie dell'orologio. Non si tratta di una data certificata da un server. Un'anomalia può impedire l'accesso alla demo, lasciando disponibile l'esportazione.

Google Play gestisce pagamento e ripristino. L'app riceve dati tecnici dell'acquisto, fra cui prodotto, stato, identificativi della transazione, token e firma; verifica la risposta per abilitare lo sblocco. Ricevuta, firma, token e identificativi della transazione sono elaborati per la verifica; il codice applicativo esaminato non li salva nel database inventario, nello storage della licenza o nei propri log. Il proprio archivio di licenza conserva lo stato e le date sopra descritti, non una copia completa della ricevuta né i dati della carta. Questo non descrive le eventuali cache, i log o la conservazione interna dei servizi Google. Non è previsto l'invio delle ricevute a un server dello sviluppatore.

All'avvio l'app avvia la consultazione del prodotto tramite Google Play, prima che l'utente prema “Acquista”. La consultazione delle offerte, l'acquisto e il ripristino utilizzano Google Play e possono richiedere una connessione anche se l'inventario funziona offline. Consultare il prodotto non comporta un acquisto o un addebito. L'app non richiede le credenziali dell'account Google.

Le informazioni gestite da Google seguono le [Norme sulla privacy di Google](https://policies.google.com/privacy?hl=it). Cancellare i dati di InventaFast non elimina la cronologia di Google Play e non equivale a chiedere un rimborso. Dopo la cancellazione può essere necessario ripristinare l'acquisto con il medesimo account Google Play.

## 5. Fotocamera e componenti dello scanner

L'accesso alla fotocamera è facoltativo ed è richiesto per la scansione. È possibile inserire manualmente i codici senza concedere il permesso, oppure revocarlo nelle impostazioni Android. Torcia, suono e vibrazione servono al funzionamento dello scanner; suono e vibrazione sono disattivabili separatamente.

Il riconoscimento usa Google ML Kit con modello incluso nell'app. Secondo la [documentazione privacy di ML Kit](https://developers.google.com/ml-kit/terms), immagini e risultati del riconoscimento sono elaborati sul dispositivo e non sono inviati ai server Google attraverso tali API.

ML Kit viene inizializzato all'avvio dell'app tramite un componente Android; la diagnostica del riconoscimento è collegata all'elaborazione dello scanner. Questi eventi non dimostrano, da soli, che dati siano stati inviati in una specifica sessione: non è stata effettuata una cattura del traffico di rete. Non si assume che l'inizializzazione attenda l'apertura della fotocamera o la concessione del relativo permesso.

**Diagnostica Google.** Oltre al riconoscimento locale, ML Kit include componenti che raccolgono metriche tecniche e possono comunicarle a Google tramite Google Play Services. La verifica del bundle Android conferma la presenza di questo percorso. La scansione offline non equivale quindi all'assenza di diagnostica.

Per le funzioni con modello incluso, Google documenta informazioni su dispositivo e app, identificativi per installazione, tempi di elaborazione, configurazione e versione delle API, dimensioni degli input/output, eventi tecnici e codici di errore. Queste metriche sono distinte dalle immagini e dal contenuto dell'inventario. Google le utilizza per analisi d'uso, diagnosi dei problemi, manutenzione e miglioramento delle API e individuazione degli abusi. Fonte: [dichiarazioni sui dati di ML Kit](https://developers.google.com/ml-kit/android-data-disclosure) e [condizioni privacy ML Kit](https://developers.google.com/ml-kit/terms).

L'effettiva trasmissione può dipendere dalla configurazione dei servizi Google, dal campionamento e dalla disponibilità della rete. L'assenza del permesso INTERNET nell'app non impedisce necessariamente comunicazioni svolte da Google Play Services. Non si dichiara che ogni categoria venga trasmessa in ogni scansione. L'auto-zoom non è abilitato. L'app attuale non offre un interruttore né raccoglie un consenso specifico per la diagnostica. Il rifiuto del permesso fotocamera, l'uscita dallo scanner e la disattivazione dell'auto-zoom non garantiscono l'arresto della diagnostica o la cancellazione di eventi già accodati.

**Punto da completare prima dell'uso come informativa definitiva:** individuare i ruoli e la base giuridica applicabili alla diagnostica, i criteri di conservazione pertinenti e gli eventuali obblighi di informazione e consenso nell'app. La scelta tecnica di mantenere ML Kit e la descrizione della diagnostica non sostituiscono questa valutazione. Il permesso fotocamera non costituisce un consenso generale alla telemetria.

## 6. Esportazione e condivisione

Excel e PDF sono generati e salvati nell'area dell'app usando i dati dell'inventario. L'utente può avviare la condivisione e scegliere un'altra app o un destinatario tramite Android.

Il destinatario potrà accedere ai dati contenuti nel report secondo il servizio scelto. Lo sviluppatore non riceve automaticamente le esportazioni. Controllare il contenuto prima di condividerlo, soprattutto se include informazioni personali o riservate.

## 7. Assistenza, finalità e basi giuridiche

Quando scrivi all'assistenza, Louis Sanges riceve indirizzo email, eventuale nome, contenuto del messaggio e allegati che decidi di inviare. Non inviare password, dati completi della carta, documenti d'identità o interi archivi se non necessari.

Per i trattamenti di sua competenza, il titolare utilizza:

| Finalità | Dati necessari | Base giuridica |
| --- | --- | --- |
| Fornire la demo, gestire lo sblocco e rispondere a richieste relative all'app o all'acquisto | Stato della licenza, dati tecnici necessari dell'acquisto; contatto e contenuto pertinente delle richieste | Esecuzione del contratto o misure precontrattuali richieste dall'interessato, art. 6(1)(b) GDPR |
| Rispondere alle richieste di esercizio dei diritti e adempiere a obblighi applicabili | Dati indispensabili alla richiesta o all'obbligo | Obbligo legale, art. 6(1)(c) GDPR |
| Accertare, esercitare o difendere un diritto in una controversia concreta | Soltanto la documentazione pertinente | Legittimo interesse alla tutela dei diritti, art. 6(1)(f) GDPR, previa valutazione della necessità e del bilanciamento |

L'invio di email è facoltativo, ma senza un contatto e le informazioni indispensabili potrebbe non essere possibile rispondere. I dati necessari alla verifica dell'acquisto servono per abilitare o ripristinare lo sblocco. Le basi indicate non autorizzano automaticamente eventuale diagnostica degli SDK.

## 8. Destinatari e trasferimenti

Le richieste di assistenza sono gestite soltanto nella casella **Microsoft Outlook/Hotmail**, accessibile al solo titolare, senza altri archivi di assistenza dichiarati. Microsoft tratta le comunicazioni secondo le condizioni del servizio e la propria [informativa privacy](https://www.microsoft.com/it-it/privacy/privacystatement).

**Google** gestisce i servizi Google Play e i trattamenti descritti nelle proprie informative. Le app e i destinatari scelti per condividere un report trattano invece la copia ricevuta secondo le loro condizioni. Autorità o professionisti possono ricevere soltanto dati necessari a un obbligo applicabile o alla gestione di una controversia.

L'inventario locale non viene trasferito automaticamente all'estero dallo sviluppatore. L'uso di email, Google Play e servizi esterni può comportare trattamenti anche fuori dallo Spazio economico europeo. Microsoft e Google descrivono nelle rispettive informative le garanzie applicabili, incluse clausole contrattuali standard e, dove applicabile, decisioni di adeguatezza. Si vedano anche le [garanzie per i trasferimenti di Google](https://policies.google.com/privacy/frameworks?hl=it). Non si dichiara che tutti i dati restino nell'Unione europea.

La consultazione di questo documento su **GitHub** comporta un accesso a un servizio distinto dall'app, soggetto all'[informativa GitHub](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). Non comporta il caricamento del tuo inventario.

## 9. Conservazione, protezione e cancellazione

**Inventario e preferenze.** Restano sul dispositivo finché vengono cancellati dall'utente. L'area privata dell'app è protetta dai controlli Android; non sono presenti una password aggiuntiva o una cifratura del database gestita dall'app. Lo stato di licenza è conservato separatamente mediante l'archiviazione protetta del sistema.

La configurazione esclude i dati dell'app dal backup cloud e dal trasferimento automatico Android. Non elimina eventuali copie prodotte da versioni precedenti o da strumenti esterni.

**Comandi di cancellazione.**

- “Nuovo inventario” azzera i conteggi dei magazzini selezionati e conserva il catalogo.
- “Cancella archivio completo” elimina prodotti, conteggi collegati e valori appresi; conserva nome azienda, magazzini, preferenze, report già generati e stato della licenza.
- Cancellare tutti i dati dell'app dalle impostazioni Android o disinstallarla elimina l'archivio locale, i report nell'area dell'app e lo stato di licenza. La scadenza della demo non impedisce queste operazioni.
- Le copie salvate o condivise fuori dall'app vanno eliminate separatamente. I report interni non hanno una scadenza automatica.

Lo sviluppatore non dispone di una copia remota da recuperare. Excel e PDF sono report consultabili: non esiste una funzione che li importi per ripristinare l'archivio.

**Email di assistenza.** Messaggi e allegati vengono conservati per gestire la richiesta e per **6 mesi dalla sua chiusura**, poi cancellati dalle copie gestite dal titolare. Puoi chiederne la cancellazione anche prima: quando ricorrono le condizioni dell'art. 17 GDPR, il titolare provvede senza ingiustificato ritardo. Il termine massimo ordinario di conservazione non viene quindi prolungato in attesa di una richiesta. Se un documento è necessario per un obbligo legale o una controversia concreta, ne viene conservata separatamente solo la parte pertinente per il periodo richiesto dall'obbligo o dalla tutela del diritto. Le copie tecniche del fornitore email seguono le sue regole di cancellazione e conservazione.

I dati conservati autonomamente da Google, Microsoft o dal destinatario di una condivisione non vengono eliminati cancellando l'app.

## 10. Diritti e richieste

Nei casi previsti dal GDPR puoi chiedere accesso, rettifica, cancellazione, limitazione e portabilità dei dati, nonché opporti ai trattamenti basati sul legittimo interesse. Se un trattamento è basato sul consenso, puoi revocarlo senza pregiudicare la liceità del trattamento precedente.

Scrivi a **louisbigdev@hotmail.com**. La risposta viene fornita di regola gratuitamente entro un mese; eventuali proroghe, fino a ulteriori due mesi nei casi previsti, vengono motivate entro il primo mese. Possono essere richieste solo informazioni necessarie a verificare l'identità.

Puoi presentare reclamo al **[Garante per la protezione dei dati personali](https://www.garanteprivacy.it/)** o all'autorità competente. I diritti non sono assoluti e si applicano alle condizioni stabilite dal GDPR.

Il titolare non può accedere da remoto al tuo archivio: per i dati esclusivamente locali puoi usare i comandi dell'app e di Android descritti sopra. Questo non limita i diritti sui dati effettivamente ricevuti dal titolare, ad esempio via email.

## 11. Aggiornamenti

La data di revisione è indicata all'inizio. L'informativa sarà aggiornata quando cambiano funzioni, fornitori o trattamenti. Per nuove finalità verranno fornite le informazioni necessarie prima del relativo trattamento e, se richiesto, verrà raccolto un consenso distinto. La semplice lettura dell'informativa non costituisce consenso.
