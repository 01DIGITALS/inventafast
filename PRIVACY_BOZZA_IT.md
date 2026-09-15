# Informativa privacy — InventaFast per Android

**Bozza da approvare prima della pubblicazione.** Versione 15 settembre 2026.
Confermare operatività del contatto e verifica
finale degli SDK prima di inserire questo testo nell'app e sul sito pubblico.

Il titolare del trattamento è Louis Sanges. InventaFast è sviluppata da
LouisBigDev. Contatto privacy e assistenza:
louisbigdev@hotmai.com.

## Inventario e funzionamento locale

L'app memorizza sul dispositivo il nome dell'azienda e dei magazzini, gli articoli,
i codici a barre, i formati, i materiali, le unità di misura, le classificazioni,
le quantità e le preferenze. L'apprendimento di materiali e packaging consiste
nel riutilizzo delle voci inserite nell'archivio locale.
Non è richiesto un account InventaFast. Non sono presenti pubblicità o servizi
di sincronizzazione gestiti dallo sviluppatore. Per l'acquisto e il ripristino
dello sblocco viene utilizzato l'account Google Play dell'utente.

## Demo e acquisto tramite Google Play

La demo dura sette giorni dal primo avvio. Non prevede addebiti automatici.
Alla scadenza l'archivio non viene cancellato: senza acquisto resta disponibile
l'esportazione dei dati salvati. Lo sblocco è un acquisto unico, senza abbonamento;
il prezzo applicabile viene mostrato da Google Play prima della conferma.

Per gestire la demo e consentire l'utilizzo offline dopo l'acquisto, l'app
conserva sul dispositivo la data di inizio demo, l'ultima data verificata,
lo stato dello sblocco e un indicatore di anomalie dell'orologio. Questi dati
sono conservati in un archivio protetto separato dall'inventario. Azzerare
i conteggi o cancellare il catalogo non elimina lo stato della licenza.

Google Play gestisce il pagamento e il ripristino degli acquisti. L'app riceve
i dati tecnici della transazione, tra cui identificativo del prodotto, stato
dell'acquisto, identificativi della transazione e token di acquisto, e ne
verifica la firma per abilitare lo sblocco. Il codice applicativo conserva
come licenza lo stato dello sblocco, non i dati della carta di pagamento.
Non invia le ricevute a un server dello sviluppatore. La gestione dell'acquisto
e del ripristino richiede una connessione e i servizi Google Play.

I dati di pagamento e le registrazioni conservate da Google sono soggetti
alla [privacy policy Google](https://policies.google.com/privacy).
La cancellazione dei dati di InventaFast non cancella la cronologia degli
acquisti Google Play e non costituisce una richiesta di rimborso.

## Fotocamera e scanner

La fotocamera viene utilizzata su richiesta per leggere i codici a barre e,
facoltativamente, accendere la torcia. I fotogrammi sono elaborati sul dispositivo
con il modello di riconoscimento incluso nell'app. Il codice viene utilizzato
per ricercare o registrare un articolo; l'app non salva fotografie o video.
È possibile inserire i codici manualmente senza concedere l'accesso alla camera.
Il beep e la vibrazione sono disattivabili separatamente.

La release Android esaminata non dispone del permesso Internet. Google ML Kit,
utilizzato dallo scanner, contiene componenti che possono generare diagnostica,
metriche d'uso e identificativi di installazione. La comunicazione di rete diretta
del processo dell'app è disabilitata nella release. Prima di pubblicare va
completata la valutazione degli eventuali servizi di sistema e delle dichiarazioni
richieste per gli SDK: questo paragrafo non autorizza automaticamente la risposta
«nessun dato raccolto» nel modulo Sicurezza dei dati.

## Esportazioni e condivisione

Excel e PDF vengono generati localmente. Quando si sceglie di condividerli,
Android consente di selezionare l'app destinataria. Il contenuto del report sarà
accessibile al destinatario scelto e soggetto alle sue modalità di trattamento.
Lo sviluppatore non riceve automaticamente i report.

## Conservazione, protezione e cancellazione

L'archivio è conservato nell'area privata dell'app, protetta dai controlli di
accesso di Android. Non esiste una password aggiuntiva né una cifratura del
database gestita dall'app. Le regole Android escludono i dati dell'app dal backup
cloud e dal trasferimento automatico Android tra dispositivi.

«Nuovo inventario» azzera i conteggi conservando il catalogo.
«Cancella archivio completo» elimina prodotti, conteggi e valori appresi;
non elimina nome azienda, magazzini, preferenze o report già generati.
I report locali rimangono fino alla cancellazione dei dati dell'app o alla
disinstallazione. Queste operazioni eliminano anche l'archivio locale.
Le copie già condivise vanno eliminate presso i rispettivi destinatari.
Anche dopo la scadenza della demo è possibile eliminare tutti i dati locali
dalle impostazioni Android dell'app o disinstallando InventaFast. Prima di
procedere, esportare gli inventari che si desidera conservare. Lo sviluppatore
non dispone di una copia remota dell'archivio e non può recuperarlo.
Non è presente una funzione di importazione/ripristino degli Excel o PDF:
sono copie consultabili dei conteggi, non backup ripristinabili dell'app.

Le richieste inviate volontariamente via email sono trattate dal destinatario
per rispondere all'assistenza; la politica di conservazione di tale corrispondenza
deve essere definita dal responsabile prima della pubblicazione di questa bozza.

## Modifiche

L'informativa va aggiornata quando cambiano le funzioni o i servizi utilizzati.

---

Nota di pubblicazione: sostituire le note di revisione con le decisioni verificate,
pubblicare su URL pubblico HTTPS accessibile senza login e non in formato PDF,
e rendere il testo o il collegamento accessibile da Preferenze → Informazioni.

