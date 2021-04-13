---
title: Creazione di un evento
description: Informazioni sugli eventi AltspaceVR, su come crearli e aggiungere oggetti di personalizzazione e 3D all'editor globale.
ms.date: 03/11/2021
ms.topic: article
keywords: eventi, terminologia, console, Multimedia, editor globale, Live Stream
ms.openlocfilehash: 9b9f7ac8ef5d036b739873fc19c879250a1e264e
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212912"
---
# <a name="creating-an-event"></a>Creazione di un evento

Si tratta di una guida dettagliata per la creazione di eventi in AltspaceVR. Si consiglia vivamente di partecipare a diversi eventi in AltspaceVR per ottenere un'idea del funzionamento. Per un elenco di tutti gli eventi, vedere il [Calendario degli eventi di AltspaceVR](https://account.altvr.com/events) .

In questo articolo si apprenderà:

* Terminologia dell'evento AltspaceVR
* Creazione dell'evento e dello spazio degli eventi o del mondo
* Uso della console multimediale per una presentazione della diapositiva
* Personalizzazione dell'evento con le immagini
* Aggiunta di oggetti 3D mediante Editor/Kit internazionali
* Come registrare o Live Stream evento

## <a name="altspacevr-event-terminology"></a>Terminologia dell'evento AltspaceVR

Di seguito sono riportati i termini che è necessario conoscere per la creazione dell'evento e dello spazio eventi:

</br>

| Termine | Definizione |
|---|---|
| Compilazione globale | AltspaceVR offre la possibilità di creare e personalizzare i mondi virtuali. AltspaceVR ospita documentazione di supporto, canali di discordia ed eventi nel mondo che consentono di [ottenere ulteriori informazioni su come ottenere assistenza e iniziare a creare mondi](../world-building/world-building-faq.md). |
| World | Un mondo è uno spazio virtuale in AltspaceVR. Potrebbe trattarsi di un ufficio o di una vasta gamma di Mountain. Si tratta di un ambiente altamente personalizzabile. Si trova all'interno di un universo ed è possibile che esistano più mondi all'interno di quell'universo. Se si desidera disporre di più spazi eventi per eventi speciali, centri di formazione e spazi di riunioni diversi per rendere disponibili le spezie, aggiungere i mondi nello stesso universo per mantenerli insieme come gruppo. |
| Universo | Un universo nel mondo AltspaceVR che compila la lingua volgare rappresenta la categorizzazione dei tuoi mondi. Ogni universo può ospitare più mondi. I mondi ereditano le impostazioni dell'universo, semplificando l'aggiunta di utenti a allow-list per più mondi e altre funzionalità di controllo. Per altre informazioni, vedere [gestione dei mondi](../world-building/managing-worlds.md) . |
| Modello | Un modello (o un modello di spazio) è un ambiente o un ambiente prestabilito che può essere usato invece di crearne uno usando le funzionalità di creazione del mondo. AltspaceVR offre un'ampia gamma di modelli per esperienze ed eventi differenti. |
| Spazio eventi | Uno spazio eventi è un sinonimo di World in AltspaceVR. In generale, si riferisce a un mondo usato per ospitare gli eventi. |
| Sito Web | I riferimenti al "sito Web" sono nel [sito Web di AltspaceVR](https://altvr.com/). Spesso è più semplice creare e modificare gli eventi tramite la [pagina Web eventi](https://account.altvr.com/events/my) in un computer o un tablet anziché tramite il dispositivo VR. È necessario accedere al sito Web anche per la [compilazione mondiale](../world-building/managing-worlds.md) . |
| Ruoli contestuali | I [ruoli contestuali](../getting-started/roles.md) sono assegnati dall'autore dell'evento o dal generatore globale. Questi ruoli offrono agli utenti in un mondo o in uno spazio di eventi funzionalità aggiuntive. Attualmente, sono costituiti da host, Presenter, moderatore, pilota (Flight), di bonifica (World Building) e megafono. Questi possono essere assegnati singolarmente o globalmente, consentendo a tutti di avere gli stessi ruoli nello spazio o nel mondo degli eventi. |
| Interfaccia utente (UI)/menu | Quando ci si trova in AltspaceVR nel mondo, all'interno dell'ambiente immersivo sono disponibili menu a sinistra e a destra dello schermo. Il menu Circle o Main con il logo AltspaceVR apre l'interfaccia utente principale (UI) o il menu per accedere a schermate diverse per esplorare AltspaceVR e personalizzare l'esperienza. Gli elementi facoltativi dell'interfaccia utente sono disponibili nella dimensione corretta dello schermo e includono in genere gli strumenti host e dell'editor globale. Questi vengono aperti e interagiscono facendo clic su di essi con il cursore. |
| SDK/MRE | Si tratta di termini di compilazione globale associati al Software Development Kit e alle estensioni per la [realtà mista](../world-building/using-mixed-reality-extensions.md) usate per aggiungere funzionalità e funzionalità all'esperienza di creazione globale. Si tratta in genere di utenti più avanzati. |

## <a name="understanding-events"></a>Informazioni sugli eventi

AltspaceVR consente di creare in modo semplice un mondo in cui è possibile usare uno spazio di modelli preesistente da usare o personalizzare in base alle esigenze specifiche o creare un mondo da zero. Questo articolo illustra l'uso di un modello predefinito per creare l'evento. Le sezioni seguenti sulla personalizzazione dell' [evento con le immagini](#branding-your-event-with-images) e l' [aggiunta di oggetti 3D con editor e kit internazionali](#adding-3d-objects-using-world-editor-and-kits) includono suggerimenti per un'ulteriore personalizzazione. Per informazioni sulla creazione di un mondo personalizzato da zero, partecipare al World Building tour Meetups in AltspaceVR e [consultare la documentazione del supporto per la compilazione del mondo](../world-building/world-editor-getting-started.md).

AltspaceVR offre due modi per creare uno spazio per l'evento.

* **Uso monouso:** Creare un evento e selezionare un mondo modello.
* **Uso ripetuto:** Creare uno spazio globale e importarlo nell'evento.

Il processo di creazione di un evento è lo stesso per entrambi, con una sola eccezione: la [creazione di un mondo e l'importazione](../world-building/managing-worlds.md) come spazio degli eventi di ripetizione-utilizzo. È anche necessario tenere presente quanto segue:

</br>

| Termine | Definizione |
|---|---|
| Mondo copiato | L'uso di uno spazio globale per un evento ripetuto consente la personalizzazione permanente. I segni, le immagini, i punti di generazione e le altre personalizzazioni vengono mantenuti da evento a evento anziché personalizzare lo spazio eventi ogni volta. |
| Personalizzare il mondo degli eventi | Quando viene creato un evento, il modello o il mondo importato viene copiato e bloccato nell'evento. È possibile apportare modifiche al mondo dell'evento e non influisca sul mondo originale e viceversa. Si consiglia di aggiungere decorazioni festive, immagini o altri elementi decorativi monouso per l'uso di un editor globale per rendere più gradevole lo spazio degli eventi e appropriato per l'evento. |

Le modifiche apportate al mondo originale non saranno presenti nel mondo dell'evento, a meno che non venga aggiornato lo spazio degli eventi:
1. Usare il pulsante **re-import World** nella pagina Web dell'evento.
2. Consente di attendere 2-3 minuti per il completamento della sincronizzazione. 
3. Se lo spazio degli eventi non è stato modificato, passare a **impostazioni > modera > Reimposta spazio** per ripristinare lo spazio degli eventi. Si reimposterà molto spazio come un generatore mondiale.

In caso di problemi tecnici, ad esempio se gli elementi non vengono caricati correttamente, passare al menu AltspaceVR e selezionare **impostazioni > modera > Reimposta spazio** per ripristinare lo spazio degli eventi e visualizzare le nuove modifiche. Gli utenti di PC Windows in 2D possono usare la scelta rapida da tastiera: **CTRL + ALT + R** in AltspaceVR per reimpostare rapidamente lo spazio.

## <a name="creating-your-event-and-event-space-or-world"></a>Creazione dell'evento e dello spazio degli eventi o del mondo

Di seguito sono riportate istruzioni dettagliate per la creazione di un evento per un evento singolo o ripetuto. Selezionando il modello o importando un mondo per l'evento. 

> [!NOTE]
> La pagina Web degli eventi di AltspaceVR offre istruzioni su ogni aspetto del modulo tramite i pulsanti per il punto interrogativo verde. Scorrere il cursore su di essi per istruzioni specifiche.

Nella pagina Web [eventi > My Events](https://account.altvr.com/events/my) nel sito Web di AltspaceVR selezionare **pianificare un evento** o passare direttamente alla [pagina Web Crea evento in AltspaceVR](https://account.altvr.com/events/new).

1. **Titolo evento:** Digitare il nome dell'evento. Mantenerla specifica e concisa per la visualizzazione nelle varie visualizzazioni del calendario nel sito Web di AltspaceVR e nell'interfaccia nel mondo. Provare a lasciare il titolo inferiore a 23 caratteri, inclusi gli spazi tra le parole.
2. **Descrizione:** Digitare la descrizione dell'evento.
    * Deve contenere almeno 10 caratteri nella descrizione oppure l'evento non verrà creato.
    * Aggiungere uno spazio vuoto tra i paragrafi.
    * Per aggiungere un collegamento a Facebook, discordia, sito Web o altre risorse dell'evento, usare il formato seguente (questo Markdown funziona solo sulla pagina di promozione dell'evento nel sito Web, il rendering non verrà eseguito correttamente nei menu di AltspaceVR): `[Event Name](http://example.com/)`

3. Data di **inizio/data di fine:** Impostare l'ora di inizio e verificare che l'ora di fine sia successiva all'ora di inizio.
4. **Categoria:** Scegliere la categoria che meglio descrive il tipo di evento. 
5. Impostare l'evento su **privato** o **pubblico**.
    * Visibilità: gli eventi pubblici sono visibili nella [scheda tutti](https://account.altvr.com/events/all) del calendario eventi del sito Web di AltspaceVR e sono aperti al pubblico.
    * Gli eventi privati non sono visibili nei calendari degli eventi AltspaceVR e richiedono che l'URL dell'evento entri nello spazio degli eventi.
    * Se si vuole ' Aggiungi come evento principale ', l'evento deve essere impostato su Public.
6. **Selezionare un modello:** Lungo il lato destro della pagina Web è disponibile un elenco di immagini di anteprima dei modelli disponibili in AltspaceVR. Sono disponibili sale da gioco, uffici, spazi riunioni, spazi di presentazione e divertenti spazi Meetup. Selezionare un aspetto interessante. In caso contrario, è sufficiente creare un nuovo evento con un nuovo modello. Se si vuole creare un mondo personalizzato per gli eventi, selezionare il **cielo freddo** come modello predefinito e seguire le istruzioni riportate di seguito per l'importazione del mondo.
7. Selezionare le **Opzioni avanzate**

### <a name="advanced-options"></a>Advanced Options

1. **Alza** di livello: Ogni evento richiede due immagini di personalizzazione (queste immagini vengono visualizzate nel sito Web AltspaceVR e non vengono visualizzate nell'evento all'interno di AltspaceVR):
    * **Riquadro:** È necessario che l'immagine del riquadro sia di 1920x1080 pixel. Questa immagine verrà ridimensionata in diverse dimensioni di anteprima e visualizzata nel calendario eventi AltspaceVR con altri eventi. Assicurarsi che l'immagine sia chiara e che non abbia molto testo. Non usare le immagini o i logo protetti da copyright di cui non si è proprietari.
    * **Banner:** È necessario che le immagini del banner siano 1920x576. Questa operazione verrà ridimensionata automaticamente in modo necessario e visibile nelle informazioni sull'evento o nella pagina Web. Una sovrapposizione semi-trasparente copre il 25% inferiore dell'immagine. Evitare di inserire testo in tale area.
    * Un'altra opzione (più veloce) consiste nel copiare l'immagine del **riquadro nell'immagine del banner in background**. verrà usata anche l'immagine del riquadro come immagine del banner. Prova:). Se l'aspetto non è corretto, è possibile creare una nuova immagine banner.
2. **In VR:** Questa sezione include le funzionalità che si applicano all'esperienza virtuale durante l'evento all'interno dell'app AltspaceVR:
    * **Ruoli contestuali predefiniti:** Il punto interrogativo verde elenca i ruoli specifici disponibili per tutti i membri del gruppo *di destinatari nell'evento*. Il più comune è *megaphone_only*. Aggiungere questo valore per dare l'opzione "amplifica la voce" sotto il pulsante Strumenti host a tutti i membri del pubblico in modo che possano essere ascoltati nell'evento se è uno spazio grande. Se l'evento richiede il volo, aggiungere il programma *pilota*. Per aggiungerli entrambi, il formato è: *megaphone_only, pilota*. Ogni utente deve abilitare la modalità di volo nell'app AltspaceVR passando a Impostazioni/input/volo.
    * **Istruzioni:** Le [istruzioni](../world-building/adding-welcome-messages.md) sono destinate al testo che genera un'immagine iniziale all'arrivo nello spazio. Gli utenti devono selezionare ' OK ' per rimuoverlo dalla propria visualizzazione. Questo viene spesso usato per fornire istruzioni per i destinatari, ad esempio "è possibile rimanere muti fino a quando non è stato invitato a parlare" o "benvenuto all'evento XYZ in cui verrà illustrata la ABC". Questa operazione non è obbligatoria, quindi è consigliabile usarla in modo sensato. È anche possibile usare Markdown per aggiungere il colore e il ridimensionamento dei tipi di carattere, più dettagli: [http://digitalnativestudios.com/textmeshpro/docs/rich-text](http://digitalnativestudios.com/textmeshpro/docs/rich-text)
3. **Avanzate:** Di seguito è riportata una rapida spiegazione delle funzionalità avanzate per gli eventi (alcune di queste funzionalità non verranno visualizzate finché non viene creato l'evento e si modifica l'evento):
    * **Amministratori:** Gli amministratori sono AltspaceVR gli utenti considerati attendibili per facilitare la gestione dell'evento. Potrebbero essere i cohost o gli host di backup. Aggiungendo il nome utente all'elenco Admins, è possibile:
        * Modificare il titolo, la descrizione e altre funzionalità dell'evento.
        * Aggiungere e rimuovere ruoli contestuali per moderatori, presentatori e altri ruoli.
        * Eliminare l'evento.
    * **Gruppo:** Scegliere tra i [gruppi](group-features.md) privati usando il menu a discesa. Visualizzerà solo se l'account è stato creato o aggiunto a un gruppo.
    * **Motto:** Questa frase concisa verrà visualizzata nella pagina Web dell'evento sotto il titolo.
    * **Importa da mondo:** Per usare uno spazio degli eventi di tutto il mondo creato per l'uso ripetuto, questa è la sezione del modulo da usare per importare il layout e la personalizzazione del mondo nell'evento. Tenere presente le considerazioni seguenti:

    **Importa il tuo mondo:** Per importare un mondo, è stato creato e personalizzato:
    * Selezionare la freccia a discesa per visualizzare un elenco di mondi creati.
    * Selezionare il mondo.
    * Dopo aver completato il resto del modulo dell'evento, attendere almeno 2 minuti prima di visitare lo spazio eventi in AltspaceVR per assicurarsi che le informazioni del database vengano aggiornate e che venga generato il mondo.
    
    **Usa il mondo di un altro utente:**
    * Contattare il proprietario del mondo per richiedere che usi la funzionalità **condivisione con amici** in un singolo mondo per condividerlo con l'utente.

3. **ID video di YouTube:** Visibile nella pagina Web dell'evento, consente di aggiungere trailer o video di eventi di YouTube alla pagina Web eventi, non al mondo. È necessario solo la parte relativa all'ID video dell'URL: dQw4w9WgXcQ
4. **Handle di Twitter:** In questo modo, il flusso di Twitter viene aggiunto alla pagina Web dell'evento. Se l'account Twitter è personale e non correlato all'evento o all'associazione, è possibile che si verifichi una condivisione eccessiva. È necessario solo l'handle: @elonmusk
5. **Ruoli contestuali:** Questo è il punto in cui si controllano i privilegi avanzati o i [ruoli contestuali](../world-building/granting-roles.md) degli host di eventi, dei Presenter, dei moderatori e di altri ruoli all'interno dell'evento. Per aggiungerli, immettere il nome utente AltspaceVR e assegnare loro un ruolo nel menu a discesa. Per rimuoverli, selezionare la casella di controllo per rimuovere e salvare la pagina Web dell'evento. Nota: se si desidera concedere una funzionalità di moderazione del relatore, è necessario aggiungerli come Presenter e moderatore. Sono attualmente disponibili i seguenti ruoli contestuali:
    * **Presenter:** Aggiunge le [funzionalità della riga anteriore](../faqs/front-row-events.md) all'interfaccia dell'utente in AltspaceVR per aggiungerle.
    * **Moderatore:** Aggiunge funzionalità di moderazione all'interfaccia dell'utente, inclusa la possibilità di eseguire il testo di ogni partecipante, di disattivarle a livello globale per l'evento o di rimuoverle dall'evento. Aggiungere di nuovo il relatore e assegnare loro i ruoli di moderazione se si desidera disporre di privilegi di moderazione.
    * **Solo megafono:** Aggiunge il pulsante di amplificazione della voce alla relativa interfaccia tramite il pulsante Strumenti host.
    * Di **bonifica:** Aggiunge il pulsante editor globale alla relativa interfaccia.
    * **Progetto pilota:** Aggiunge le funzionalità di volo per quel singolo utente. Nota: è necessario abilitarla in Impostazioni/input/volo
    * **Esecutore musicale:** Aggiunge funzionalità e funzionalità associate a eventi concertistici e musicali.
6. **Blocca utenti elencati:** Se si vuole impedire a un utente di accedere oppure un utente è stato rimosso in precedenza dall'evento da un moderatore o da un relatore e l'evento è stato duplicato, verrà elencato il nome dell'utente del blocco elencato. Gli host o gli amministratori di eventi possono aggiungere o rimuovere un utente elencato di blocco in qualsiasi momento.

Quando il modulo è completo e triple selezionato, selezionare **Crea evento**.

> [!IMPORTANT]
> Se l'evento non viene creato correttamente, verificare di avere almeno 10 caratteri nella descrizione e/o di aver selezionato un modello. se selezionato, il nome del modello verrà trasformato da bianco a blu.

## <a name="event-page-actions"></a>Azioni della pagina di evento

Nella pagina Web dell'evento sono disponibili le azioni e le opzioni seguenti:

1. Selezionare **modifica** per apportare modifiche alle impostazioni dell'evento.
2. Selezionare **fine evento** per terminare l'evento (se l'evento è più presto, ad esempio).
3. Selezionare **imposta su bozza** per impostare l'evento su bozza anziché su attivo.
4. Se è stato eseguito un aggiornamento per il mondo importato, è necessario selezionare **REimportare il mondo** affinché le modifiche vengano visualizzate nell'evento, non dimenticare di reimpostare lo spazio nell'evento:)
5. Selezionare **evento duplicato** per duplicare l'evento per gli eventi futuri. Questo duplicato verrà quindi visualizzato negli eventi personali/della bozza, sarà necessario aggiornare il nuovo giorno/ora e attivarlo da questa posizione.
6. Selezionare **Aggiungi come evento principale** per impostare l'evento sull'elenco dei calendari.
7. Selezionare **Elimina evento** se si vuole eliminare completamente l'evento (non è possibile recuperare questo evento).

Quando si è pronti, passare al menu **eventi > My Events** nell'interfaccia AltspaceVR nel mondo e immettere lo spazio degli eventi per reimpostare lo spazio, controllare le modifiche o continuare la personalizzazione. 

> [!IMPORTANT]
> Si tratta di una copia e le personalizzazioni dello spazio eventi sono solo per questo evento. Se si sta spendendo molto tempo per personalizzare lo spazio dell'evento, potrebbe essere preferibile creare un mondo per l' **evento di uso ripetuto**.

Per ulteriori informazioni sulla personalizzazione dello spazio degli eventi o sulla creazione di un ambiente di spazio degli eventi originale da importare:

* [Ricerca per categorie concedere ruoli ad altre persone nei miei mondi?](../world-building/granting-roles.md)
* [Ricerca per categorie consentire agli utenti di volare (o avere altre capacità) nel mondo?](../world-building/adding-user-abilities.md)
* [Dove posso ottenere assistenza per la compilazione globale?](../world-building/getting-help.md)
* [Ricerca per categorie gestire i miei mondi?](../world-building/managing-worlds.md)
* [Domande frequenti sulla creazione di un mondo](../world-building/world-building-faq.md)
* [Ricerca per categorie aggiungere punti di spawn personalizzati ai miei mondi?](../world-building/adding-custom-spawn-points.md)
* [Ricerca per categorie caricare i kit personali?](../world-building/uploading-custom-kits.md)
* [Ricerca per categorie iniziare a usare il Toolkit per la compilazione del mondo (Uploader Unity)?](../world-building/world-building-toolkit-getting-started.md)

## <a name="using-the-multimedia-console-for-a-slide-presentation"></a>Uso della console multimediale per una presentazione della diapositiva

La console multimediale è un ottimo modo per organizzare il contenuto per una presentazione, tra cui immagini, audio o video. Seguire le [istruzioni della console multimediale](multimedia-console.md) per ottenere la configurazione per l'evento.

## <a name="branding-your-event-with-images"></a>Personalizzazione dell'evento con le immagini

L'aggiunta di immagini allo spazio degli eventi o al logo e alla personalizzazione dell'azienda o anche fotografie di se stessi, del team o di altri contenuti visivi è facile in AltspaceVR.

I requisiti dell'immagine sono:
* I file JPG o PNG sono accettati
* Dimensioni massime immagine: 1920x1080
* Risoluzione: 72 DPI
* Dimensioni file: inferiori a 250 KB per file

Il processo implica il caricamento dell'immagine nelle foto di [AltspaceVR](https://account.altvr.com/photos), quindi l'uso delle foto nell'editor mondiale per l'importazione e l'inserimento nello spazio globale degli eventi.

1. Passare a [Photos (foto](https://account.altvr.com/photos) ) nel sito Web AltspaceVR.
2. Selezionare **Carica**.
3. Selezionare **Sfoglia** per aprire una finestra di dialogo nel computer e individuare e selezionare l'immagine ottimizzata.
4. Selezionare **Open** (Apri).
5. Selezionare **Crea foto**.
6. Ripetere questa operazione per tutte le immagini.

In AltspaceVR e nel mondo dell'evento, posizionarsi vicino a dove si vuole inserire l'immagine. Se si sta creando questo per un **evento di utilizzo ripetuto**, assicurarsi di trovarsi nel mondo e non nello spazio degli eventi.

1. Nell'angolo in basso a destra dell'interfaccia utente selezionare **editor globale/pannello Editor**
2. Fare clic sulla scheda **mine** in basso.
3. Selezionare **Photos**.
4. Le foto vengono archiviate in base all'ordine cronologico di caricamento, quindi l'immagine più recente caricata deve essere la prima immagine nell'elenco. Selezionarlo per aggiungerlo al mondo.
5. Usando il cursore del dispositivo, acquisire l'immagine e posizionarla nel punto desiderato.
    * È possibile ridimensionarla usando i controller, in genere scorrendo il cursore orizzontalmente sul touch pad in VR o usando il mouse in modalità 2D.
    * Per ottimizzare la posizione e la rotazione dell'immagine, selezionare il simbolo dell' **ingranaggio** nell'immagine nell'editor e impostare la rotazione e la posizione in modo appropriato.
    * È anche possibile ridimensionare l'immagine con la funzionalità di scalabilità.

> [!NOTE]
> Quando la modalità di modifica è impostata su on (testo arancione), si avrà automaticamente la possibilità di volare, consentendo di spostare più facilmente le immagini nel mondo degli eventi.

6. Ripetere questa operazione per ogni selezione host per ogni immagine.
7. Quando le immagini sono impostate sul posto, selezionare **blocca tutto** se non sono state bloccate singolarmente e disattivare la modalità di modifica e chiudere l'editor.
8. Usare un massimo di cinque foto per ogni evento.

## <a name="adding-3d-objects-using-world-editor-and-kits"></a>Aggiunta di oggetti 3D mediante Editor e kit internazionali

AltspaceVR consente di importare oggetti 3D in mondi con l'editor mondiale. Sono attualmente disponibili molti kit di editor del mondo per l'uso e molto altro ancora. Sono disponibili astronavi, razzi, animali animati, sculture, alberi, piante e molti oggetti diversi. In alternativa, è possibile aggiungere kit personalizzati alla raccolta pubblica o per un uso personale oppure prendere in considerazione l'uso di una delle [app ALTSPACEVR MRE](../world-building/using-mixed-reality-extensions.md), che portano oggetti interagiscono nel mondo, ad esempio caschi, spade, Ali, abbigliamento, cappelli o altri oggetti interagiscono. Si prevede che l'elenco di oggetti da espandere a breve.

Le istruzioni sono incentrate sull'uso di elementi già presenti nei kit. Per ulteriori informazioni sull'aggiunta e l'importazione di oggetti 3D in AltspaceVR, vedere ["come importare i modelli di glTF nei propri mondi".](../world-building/importing-models.md) e ["ricerca per categorie caricare i kit personali?"](../world-building/uploading-custom-kits.md).

Per aggiungere un oggetto 3D esistente tra i kit di compilazione globale nel mondo degli eventi, con la modalità di apertura e modifica del pannello Editor globale abilitata:

1. Esplorare i kit per l'oggetto che si vuole importare e selezionarlo.
2. Selezionare l'oggetto kit con il cursore e posizionarlo. Usare l'icona a forma di ingranaggio nell'oggetto dell'editor globale per usare le opzioni posizione, rotazione e scala per la voce di numero manuale.
3. Quando l'oggetto viene posizionato nella posizione corretta, bloccarlo facendo clic sull'icona del lucchetto.
4. Se lo si desidera, aggiungere un altro oggetto. Si consiglia di aggiungere oggetti 3D, mantenendo le selezioni non più di elementi di cinque diversi kit singoli, per un migliore supporto per gli utenti di Oculus quest. Non usare più di 200 oggetti in un mondo.
5. Al termine, bloccare tutti gli elementi, disattivare la modalità di modifica e chiudere l'editor globale. Aggirare. Invita alcuni tester a visitare il computer e scoprirlo e prepararsi per un evento eccezionale.

Per ulteriori informazioni sui kit di editor del mondo e sull'aggiunta di oggetti 3D a AltspaceVR:

* [Che cos'è il programma di accesso anticipato?](../world-building/early-access.md)
* [Come importare i modelli glTF nei miei mondi?](../world-building/importing-models.md)
* [Ricerca per categorie usare un MRE nel mondo?](../world-building/using-mixed-reality-extensions.md)

## <a name="how-to-record-or-live-stream-my-event"></a>Come registrare o Live Stream evento

Vedere il documento di supporto seguente per istruzioni su come registrare o trasmettere in streaming live l'evento:

* [Come registrare o Live Stream evento](recording-and-live-streaming.md)