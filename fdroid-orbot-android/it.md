---
name: F-Droid per Android
description: L'alternativa open-source a Google Play Store
---
![cover](assets/cover.webp)

## Cos'è il *sideloading*
Come utenti Bitcoin siamo sempre alla ricerca di soluzioni che siano rispettose della privacy e che soddisfino personali standard di sicurezza. Google Play Store, generalmente, non rispecchia la risposta efficace a queste esigente, pertanto la comunità ha trovato (o svilippato) alternative al "monopolio" del Play Store.
Il *sideloading* è proprio questo: la possibilità di scaricare app per Android da fonti diverse dallo store ufficiale di Google.

Uno di questi è F-Droid.
Esaminato in maniera meticolosa nel corso di svariati audit di sicurezza, F-Droid è una piattaforma che applica rigirose policy di esclusione verso app troppo ansiose di tracciare gli utenti.
Non significa che lo scetticismo, sempre salutare quando si ricercano privacy e sicurezza, debba essere messo da parte. Le app tipo i wallet, ad esempio, dovrebbero essere scaricate da sorgenti ufficiali. Ma F-Droid può essere uno dei primi passi di un personale percorso dedicato alla ricerca del miglior grado di privacy possibile.

# Download F-Droid
Si comincia da una veloce ricerca sul web, imparerete col tempo il sito ufficiale a memoria

![img](assets/it/02.webp)

Dare una lettura alla documentazione è sempre una buona idea, per poi recarsi nella sezione del *Download*. Quest'ultimo è disponibile subito, tramite QR code per installarlo sul cellulare, ma in questo tutorial vedremo anche l'interessante fase della verifica. Ci apprestiamo, pertanto, a scaricare F-Droid su PC.

![img](assets/it/03.webp)

Vediamo infatti che è possibile verificare di scaricare una versione legittima, firmata da una chiave PGP unica, ed è proprio quello che faremo

![img](assets/it/04.webp)


# Download e verifica su OS Linux

Importazione e verifica firme su Linux si eseguono agevolmente da riga di comando.
Pertanto si deve aprire il terminale -> accertarsi di essere in */home* -> creare la directory */fdroid* e spostarsi con il comando *cd* per prepararsi al download.

![img](assets/it/05l.webp)

Copiare quindi i comandi che si trovano nella pagina di verifica sul sito di F-Droid. Il primo per scaricare il file .asc

![img](assets/it/06l.webp)

il secondo per l'apk.

![img](assets/it/07l.webp)

Infine, il comando per scaricare ed importare la chiave pubblica PGP necessaria alla verifica.

![img](assets/it/08l.webp)

che deve mostrare questo output se avvenuto correttamente.

![img](assets/it/09l.webp)

Con il comando *ls -la* controlliamo di aver scaricato tutto nella directory corretta

![img](assets/it/10l.webp)

Quindi si può lanciare il comando di verifica *gpg --verify* selezionando il file .asc

![img](assets/it/11l.webp)

che deve dare questo risultato

![img](assets/it/12l.webp)

---

# Download e verifica su OS Windows
Scarichiamo quindi il file *.apk*, cioè l'applicativo per android ed anche il file *.asc*.
  
![img](assets/it/05w.webp)

per poi ricercare la chiave pubblica PGP e verificare la versione con Kleopatra.
Gli sviluppatori di F-Droid hanno caricato la chiave pubblica su keyserver.ubuntu.com e - nelle istruzioni - c'è la stringa univoca da ricercare.

1. In un'altra finestra del browser, quindi, si incolla il link copiato che si trova tra le istruzioni di verifica di F-Droid

![img](assets/it/06w.webp)

2. Si incolla la chiave, che inizia per 37D2 e si clicca su *Search*

![img](assets/it/07w.webp)

3. la ricerca porta ad una pagina con molti link delle chiavi pubbliche, si può scegliere il primo

![img](assets/it/08w.webp)

4. per poi decidere di salvare il file proposto.

![img](assets/it/09w.webp)

## Importazione della chiave pubblica
A questo punto andare nella directory dove si sino scaricati tutti questi elementi e scegliere, con il tasto destro del mouse, di aprire con *Blocco note* il file denominato 37d2xxxx.asc.

![img](assets/it/10.webp)

Copiare tutto il messaggio

![img](assets/it/11.webp)

Lanciare Kleopatra e selezionare il menu *Notepad*

![img](assets/it/12.webp)

quindi incollare. Alla prima importazione Kleopatra chiede la certificazione, che possiamo dare.

![img](assets/it/13.webp) ![img](assets/it/14.webp)

## Verifica della versione di F-Droid

A questo punto possiamo tornare nel menu principale di Kleopatra, dove compare la chiave pubblica di F-Droid, certificata.
Scegliere adesso il menu *Dectryp/Verify* 

![img](assets/it/15.webp)

che apre il file manager, attraverso il quale dobbiamo scegliere di verifiare il file F-Droid.apk **.asc**

![img](assets/it/16.webp)

Kleopatra, o GPG4Win inizia automaticamente la procedura di verifica. Se l'esito è positivo, ovvero appare come in questa foto

![img](assets/it/17.webp)

Abbiamo la ragionevole certezza che nella directory *Download* c'è una versione legittima di F-Droid, firmata cioè con la chiave PGP unica dello sviluppatore. Possiamo pertanto trasferire F-Droid sul cellulare ed installarlo.

---

# Installazione sul cellulare

Dopo aver trasferito il file verificato sul cellulare, F-Droid si può installare. Andiamo a lanciare l'installazione cliccando sull'apk dove si trova, ad esempio nel *Download* di Android.

![img](assets/it/18.webp)

Se si tratta della prima volta che si installa sul proprio dispositivo unapk da fonte diversa dal Play Store ufficiale, il sistema chiede di modificare le impostazioni (di default, ogni dispositivo Android rifiuta questo tipo di installazione, che va autorizzata manualmente.

![img](assets/it/19.webp)

Automaticamente si arriva nei settings dove si deve autorizzare l'installazione.

![img](assets/it/20.webp)

Ora si può installare F-Droid ed aprirlo-

![img](assets/it/21.webp) ![img](assets/it/22.webp)

A seconda dello stato di aggiornamento dell'apk installato, F-Droid potrebbe scaricare autonimamente gli aggiornamenti dai Repository.
Se ciò non avviene, conviene comunque procedere in modo manuale. Si scelgano i *Settings* di F-Droid in basso a destra

![img](assets/it/23.webp)

per vedere lo stato di avanzamento.

![img](assets/it/24.webp)

Nei *Settings* scegliere *Repository* e 

![img](assets/it/25.webp)

aggiungere alla nostra app i repository del Guardian Project ed F-Droid Archive

![img](assets/it/26.webp)

### L'aggiornamento manuale va fatto di tanto in tanto, seguendo le procedure appena spiegate. Eventuali aggiornamenti venrranno segnalati e saranno visibili cliccando sull'icona delle notifiche.

![img](assets/it/27.webp)

# Bonus: Orbot, Tor per Android

Terminati tutti gli aggiornamenti, siamo pronti per esplorare questo nuovo store.
Nel menu principale *Latest* è visibile in basso a destra una casella di ricerca. Si può cercare un'app predefinita e scaricarla.

![img](assets/it/28.webp)

Scegliamo ad esempio di cercare **Orbot**.

Tra i risultati di ricerca, selezionare **Orbot: proxy with Tor**

![img](assets/it/29.webp)

Scegliere *Install* e Orbot sarà pronto per essere lanciato, configurato ed utilizzato

![img](assets/it/30.webp)

# Conclusioni
Il Guardian Project, respnsabile del progetto, è una comunità di volontari che compilano le app open source per listarle sulla piattaforma.
Può capitare che alcuni aggiornamneti disponibili su Play Store, siano invece in "ritardo" su F-Droid, perché la comunità sta ancora compilando il nuovo sorgente.
**È bene non aggiornare da sorgenti miste le proprie app. Se si sono installate da F-Droid, non aggiornare col Play Store e viceversa**. Se non si è disposti ad aspettare l'aggiornamento del Guardian Project, significa che F-Droid non è lo strumento giusto per noi.

In linea di massima, a parere di chi scrive, i wallet in particolare, non dovrebbero mai essere scaricati da F-Droid (tanto meno dal Play Store), bensì dal sito/repository Github ufficiale dello sviluppatore.
