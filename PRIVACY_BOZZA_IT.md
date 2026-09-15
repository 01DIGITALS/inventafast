# Informativa privacy — InventaFast per Android

**Bozza revisionata il 15 settembre 2026 — non ancora definitiva per lo store.**
Il contatto e la durata di conservazione delle email sono stati confermati dal titolare.
Questa bozza riguarda il candidato Android **0.3.0+3**, nel quale ML Kit è stato sostituito con un decoder locale. Resta da completare la valutazione dei componenti Google Play Billing, riportata nelle [note di revisione](REVISIONE_PRIVACY_2026-09-15.md). La gestione degli incassi prevede la sola consultazione in Google Play Console.

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
- Lo scanner usa un decoder locale. I servizi degli acquisti includono componenti Google da valutare separatamente: si veda la sezione 4.

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

**Componenti Google degli acquisti — valutazione ancora aperta.** Google Play Billing include componenti di diagnostica e trasporto degli eventi, distinti dallo scanner locale. La loro presenza è stata rilevata nelle dipendenze del candidato esaminato; non dimostra, da sola, quali dati siano effettivamente trasmessi in una specifica sessione. Non è stata effettuata una cattura di rete. L'assenza del permesso INTERNET dell'app non controlla le comunicazioni svolte da Google Play Services.

Prima dell'uso di questa bozza come informativa definitiva occorre completare la valutazione dei flussi di acquisto e della loro eventuale diagnostica: dati, finalità, ruoli, conservazione, base giuridica ed eventuali controlli o consensi necessari. Non si dichiara che l'intera app sia priva di componenti diagnostici Google.

**Gestione degli incassi.** Il titolare consulta ordini e report esclusivamente all'interno di Google Play Console per verificare gli acquisti e gli incassi dell'app. Questa gestione non prevede lo scaricamento o la conservazione di copie su computer o servizi cloud esterni, né la condivisione dei report con un commercialista o altre persone. La consultazione riguarda le informazioni sull'ordine e gli importi resi disponibili dalla Console, limitatamente a quanto necessario. Per la gestione del rapporto di acquisto la base giuridica è l'esecuzione del contratto, art. 6(1)(b) GDPR; eventuali adempimenti imposti dalla legge si fondano sull'art. 6(1)(c). Non viene costituito un archivio separato degli incassi presso il titolare: la disponibilità e la conservazione dei dati nel servizio Google seguono le condizioni e l'informativa del servizio, senza un termine di cancellazione autonomamente impostato dall'app. Eventuali future modalità diverse saranno valutate e descritte prima di essere adottate.

## 5. Fotocamera e scanner locale

L'accesso alla fotocamera è facoltativo ed è richiesto per la scansione. È possibile inserire manualmente i codici senza concedere il permesso, oppure revocarlo nelle impostazioni Android. Torcia, suono e vibrazione servono al funzionamento dello scanner; suono e vibrazione sono disattivabili separatamente.

Nella versione Android 0.3.0+3 il riconoscimento usa **ZXing-C++ tramite flutter_zxing**, un decoder locale che sostituisce Google ML Kit. La fotocamera e il processo di decodifica vengono avviati entrando nello scanner e rilasciati uscendo. I fotogrammi sono elaborati sul dispositivo; questa integrazione non usa servizi remoti, lettura di immagini da URL o selezione dalla galleria, e non salva fotografie o video. La registrazione dei log del decoder nativo è disattivata.

La rimozione di ML Kit e del suo componente di inizializzazione è stata verificata nel bundle esaminato. La diagnostica specifica ML Kit descritta nelle precedenti bozze non riguarda questo nuovo scanner. Questa conclusione non si estende automaticamente ai servizi Google Play utilizzati per gli acquisti, descritti nella sezione 4.

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
