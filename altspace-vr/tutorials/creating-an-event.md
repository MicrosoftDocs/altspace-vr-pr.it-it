---
title: Creazione di un evento
description: Informazioni sugli eventi AltspaceVR, su come crearli e sull'aggiunta di oggetti 3D e di personalizzazione con World Editor.
ms.date: 03/11/2021
ms.topic: article
keywords: eventi, terminologia, console, contenuti multimediali, editor del mondo, flusso live
ms.openlocfilehash: 1e758b35b3bd5d5a580eb04e683d6b1dc4500b43
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923038"
---
# <a name="creating-an-event"></a>Creazione di un evento

Questa è una guida dettagliata per la creazione di eventi in AltspaceVR. È altamente consigliabile partecipare a diversi eventi in AltspaceVR per avere un'esperienza di funzionamento. Controllare [altspaceVR Events Calendar per](https://account.altvr.com/events) un elenco di tutti gli eventi.

In questo articolo si apprenderà:

* Terminologia degli eventi altspaceVR
* Creazione dell'evento e dello spazio eventi o del mondo
* Uso della console multimediale per una presentazione di diapositive
* Personalizzazione dell'evento con immagini
* Aggiunta di oggetti 3D con World Editor/Kit
* Come registrare o Live Stream my event

## <a name="altspacevr-event-terminology"></a>Terminologia degli eventi altspaceVR

Di seguito sono riportati i termini con cui è necessario avere familiarità con la creazione dello spazio eventi e degli eventi:

</br>

| Termine | Definizione |
|---|---|
| World Building | AltspaceVR offre la possibilità di creare e personalizzare ambienti virtuali. Gli host AltspaceVR supportano la documentazione, i canali Discord e gli eventi nel mondo per altre informazioni su come ottenere assistenza e iniziare [a creare mondi.](../world-building/world-building-faq.md) |
| World | Un mondo è uno spazio virtuale in AltspaceVR. Può trattarsi di un ufficio o di una vasta gamma di monti. Si tratta di un ambiente altamente personalizzabile. Si trova all'interno di un universo e possono essere presenti più mondi all'interno di tale universo. Se si vogliono avere più spazi eventi per eventi speciali, centri di training e diversi spazi riunioni per rendere più interessanti le cose, aggiungere i mondi nello stesso universo per mantenerli insieme come gruppo. |
| Universo | Un universo in AltspaceVR world building vernacular rappresenta la categorizzazione dei tuoi mondi. Ogni universo può contenere più mondi. I mondi ereditano le impostazioni dell'universo, semplificando l'aggiunta di persone all'elenco di elementi consentiti per più mondi e altre funzionalità di controllo. Per [altre informazioni, vedere Gestione](../world-building/managing-worlds.md) dei mondi. |
| Modello | Un modello (o modello di spazio) è un mondo o un ambiente predefinito che può essere usato invece di crearne uno usando le funzionalità di World Building. AltspaceVR offre un'ampia gamma di modelli per esperienze ed eventi diversi. |
| Spazio eventi | Uno spazio eventi è un sinonimo del mondo in AltspaceVR. In generale, si riferisce a un mondo usato per ospitare gli eventi. |
| Sito Web | I riferimenti al "sito Web" sono disponibili nel sito [Web di AltspaceVR.](https://altvr.com/) Spesso è più semplice creare e modificare eventi tramite la pagina [Web Eventi](https://account.altvr.com/events/my) in un computer o un tablet anziché tramite il dispositivo VR. Sarà necessario accedere al sito Web anche per [la creazione di](../world-building/managing-worlds.md) un mondo. |
| Ruoli contestuali | [I ruoli contestuali](../getting-started/roles.md) vengono assegnati dall'autore dell'evento o dal generatore di eventi. Questi ruoli offrono agli utenti di un mondo o di uno spazio eventi funzionalità e funzionalità aggiuntive. Attualmente sono costituiti da Host, Moderator, Pilot (flight), Terraformer (world building) e Megaphone Only. Possono essere assegnati singolarmente o globalmente, consentendo a tutti di avere gli stessi ruoli nello spazio eventi o nel mondo. |
| Interfaccia utente (interfaccia utente)/Menu | In AltspaceVR nel mondo, all'interno dell'ambiente immersivo, sono disponibili menu a sinistra e a destra dello schermo. Il cerchio o il menu principale con il logo AltspaceVR apre l'interfaccia utente o il menu principale per accedere a diverse schermate per esplorare AltspaceVR e personalizzare l'esperienza. Gli elementi facoltativi dell'interfaccia utente si trovano nelle dimensioni giuste dello schermo e in genere includono World Editor e Host Tools. Questi vengono aperti e con cui si interagisce facendo clic su di essi con il cursore. |
| SDK/MRE | Si tratta di termini di creazione del mondo associati al Software Development Kit e [alle](../world-building/using-mixed-reality-extensions.md) estensioni di realtà mista usati per aggiungere funzionalità e funzionalità all'esperienza di creazione del mondo. Si tratta in genere di utenti più avanzati. |

## <a name="understanding-events"></a>Informazioni sugli eventi

AltspaceVR semplifica la creazione di un mondo in cui è possibile usare uno spazio modello predefinito da usare o personalizzare in base alle esigenze specifiche o creare un mondo da zero. Questo articolo illustra l'uso di un modello predefinito per creare l'evento. Le sezioni seguenti relative alla [personalizzazione dell'evento](#branding-your-event-with-images) con immagini e all'aggiunta di oggetti [3D](#adding-3d-objects-using-world-editor-and-kits) con World Editor e Kit includono suggerimenti per un'ulteriore personalizzazione. Per informazioni sulla creazione di un mondo personalizzato da zero, partecipare ai meetup del World Building Tour in AltspaceVR e consultare la documentazione di supporto [di World Building.](../world-building/world-editor-getting-started.md)

AltspaceVR offre due modi per creare uno spazio per l'evento.

* **Uso una sola volta:** Creare un evento e selezionare un mondo modello.
* **Uso ripetuto:** Creare uno spazio mondiale e importarlo nell'evento.

Il processo di creazione di un evento è lo [](../world-building/managing-worlds.md) stesso per entrambi, con una sola eccezione: la creazione di un mondo e l'importazione come spazio eventi di ripetizione dell'uso. È anche necessario conoscere:

</br>

| Termine | Definizione |
|---|---|
| Mondo copiato | L'uso di uno spazio mondiale per un evento ripetuto consente la personalizzazione persistente. I segni, le immagini, i punti di generazione e altre personalizzazioni vengono mantenuti da un evento all'altro anziché personalizzare lo spazio eventi ogni volta. |
| Personalizzare il mondo degli eventi | Quando viene creato un evento, il modello o il mondo importato viene copiato e bloccato in tale evento. È possibile apportare modifiche al mondo degli eventi senza influire sul mondo originale e al contrario. Prendere in considerazione l'aggiunta di decori per le festività, immagini o altri elementi decorativi dell'editore mondiale per rendere lo spazio eventi più piacevole e appropriato per l'evento. |

Le modifiche apportate al mondo originale non saranno nel mondo degli eventi a meno che lo spazio eventi non venga aggiornato:
1. Usare il **pulsante RE-IMPORT WORLD** nella pagina Web dell'evento.
2. Consentire da 2 a 3 minuti per il completamento della sincronizzazione. 
3. Se lo spazio eventi non è stato modificato, passare a Impostazioni **> moderare** > Reimposta spazio per reimpostare lo spazio eventi. Lo spazio verrà reimpostato molto come world builder.

In caso di problemi tecnici, ad esempio gli elementi non caricati correttamente, passare al menu AltspaceVR e selezionare Impostazioni **> Moderare > Reimposta** spazio per reimpostare lo spazio eventi e visualizzare le nuove modifiche. Gli utenti di PC Windows in 2D possono usare la combinazione di tasti **CTRL+ALT+R** in AltspaceVR per reimpostare rapidamente lo spazio.

## <a name="creating-your-event-and-event-space-or-world"></a>Creazione dell'evento e dello spazio eventi o del mondo

Di seguito sono riportate istruzioni dettagliate per la creazione di un evento per un evento una sola volta o ripetuto. Selezionando il modello o importando un mondo per l'evento. 

> [!NOTE]
> La pagina Web degli eventi AltspaceVR offre istruzioni su ogni aspetto del modulo tramite l'uso di pulsanti con punto interrogativo verde. Spostare il cursore su di essi per istruzioni specifiche.

Nella [pagina Web > Eventi](https://account.altvr.com/events/my) nel sito Web di AltspaceVR selezionare Pianifica un evento o passare direttamente alla pagina Web Crea evento in [AltspaceVR](https://account.altvr.com/events/new). 

1. **Titolo evento:** Digitare il nome dell'evento. Mantenerlo specifico e conciso per la visualizzazione nelle diverse visualizzazioni del calendario nel sito Web e nell'interfaccia di AltspaceVR. Provare a mantenere il titolo al di sotto di 23 caratteri, inclusi gli spazi tra le parole.
2. **Descrizione:** Digitare la descrizione dell'evento.
    * Deve contenere almeno 10 caratteri nella descrizione oppure l'evento non verrà creato.
    * Aggiungere uno spazio vuoto tra i paragrafi.
    * Per aggiungere un collegamento a Facebook, Discord, sito Web o altre risorse dell'evento, usare il formato seguente (questo Markdown funziona solo nella pagina di promozione dell'evento nel sito Web, il rendering non verrà eseguito correttamente nei menu AltspaceVR): `[Event Name](http://example.com/)`

3. **Data di inizio/data di fine:** Impostare l'ora di inizio e assicurarsi che l'ora di fine sia dopo l'ora di inizio.
4. **Categoria:** Scegliere la categoria che descrive meglio il tipo di evento. 
5. Impostare l'evento **su Privato** o **Pubblico.**
    * Visibilità: gli eventi pubblici sono visibili nella scheda [Tutti](https://account.altvr.com/events/all) del calendario eventi del sito Web AltspaceVR e sono aperti al pubblico.
    * Gli eventi privati non sono visibili nei calendari degli eventi altspaceVR e richiedono l'URL dell'evento per immettere lo spazio eventi.
    * Se si vuole aggiungere come evento principale, l'evento deve essere impostato su pubblico.
6. **Selezionare un modello:** Sul lato destro della pagina Web è disponibile un elenco di immagini di anteprima dei modelli disponibili in AltspaceVR. Sono disponibili sale giochi, uffici, spazi riunioni, spazi di presentazione e spazi di incontro. Selezionarne uno interessante. Se non lo si desidera, è sufficiente creare un nuovo evento con un nuovo modello. Se si vuole creare un mondo di eventi personalizzato, selezionare **cool sky** come modello predefinito e seguire le istruzioni riportate di seguito per importare il mondo.
7. Selezionare **OPZIONI AVANZATE**

### <a name="advanced-options"></a>Advanced Options

1. **Alza di livello:** Ogni evento richiede due immagini personalizzate(queste immagini vengono visualizzate nel sito Web AltspaceVR e non vengono visualizzate nell'evento all'interno di AltspaceVR):
    * **Riquadro:** L'immagine del riquadro deve essere di 1920x1080 pixel. Questa immagine verrà ridimensionata a diverse dimensioni di anteprima e visualizzata nel calendario degli eventi altspaceVR con altri eventi. Assicurarsi che l'immagine sia chiara e non abbia molto testo. Non usare immagini/logo protetti da copyright di cui non si è proprietari.
    * **Banner:** Le immagini del banner devono essere 1920x576. Questo verrà ridimensionato automaticamente in base alle esigenze e visibile nelle informazioni sull'evento o nella pagina Web. Una sovrimpressione semitrasparente copre il 25% inferiore dell'immagine. Evitare di inserire testo in tale area.
    * Un'altra opzione (più rapida) è copiare l'immagine del riquadro nell'immagine del **banner** di sfondo, che userà anche l'immagine del riquadro come immagine del banner. Provare a :). Se l'aspetto non è positivo, è possibile creare una nuova immagine banner.
2. **Nella realtà virtuale:** Questa sezione include le funzionalità che si applicano all'esperienza virtuale durante l'evento all'interno dell'app AltspaceVR:
    * **Ruoli contestuali predefiniti:** Il punto interrogativo verde elenca i ruoli specifici disponibili per tutti *i membri del gruppo di destinatari nell'evento*. Il più comune è *megaphone_only*. Aggiungere questa opzione per assegnare l'opzione "Amplify My Voice" (Amplify My Voice) sotto il pulsante Host Tools (Strumenti host) a tutti i membri del gruppo di destinatari in modo che possano essere ascoltati durante l'evento se si tratta di uno spazio grande. Se l'evento richiede un volo, aggiungere *pilota*. Per aggiungerli entrambi, il formato è: *megaphone_only, pilota.* Ogni utente deve abilitare la modalità fly nell'app AltspaceVR selezionando Settings/Input/Fly (Impostazioni/Input/Fly).
    * **Istruzioni:** Le [istruzioni sono](../world-building/adding-welcome-messages.md) relative al testo che genera un'immagine di benvenuto all'arrivo nello spazio. Gli utenti devono selezionare "OK" per rimuoverlo dalla visualizzazione. Questa opzione viene spesso usata per fornire ai destinatari istruzioni come "Si invita a parlare" o "Benvenuti nell'evento XYZ in cui verrà illustrato ABC". Questo non è obbligatorio, quindi usare consaciamente. È anche possibile usare Markdown per aggiungere il colore e il ridimensionamento dei caratteri, altri dettagli: [http://digitalnativestudios.com/textmeshpro/docs/rich-text](http://digitalnativestudios.com/textmeshpro/docs/rich-text)
3. **Avanzate:** Di seguito è riportata una rapida spiegazione delle funzionalità avanzate per gli eventi (alcune di queste funzionalità verranno visualizzate solo dopo la creazione dell'evento e la modifica dell'evento):
    * **Amministratori:** Gli amministratori sono utenti altspaceVR attendibili per facilitare la gestione dell'evento. Possono essere i cohost o gli host di backup. Aggiungendo il nome utente all'elenco Admins, gli amministratori possono:
        * Modificare il titolo dell'evento, la descrizione e altre funzionalità.
        * Aggiungere e rimuovere ruoli contestuali per moderatori, host e altri ruoli.
        * Eliminare l'evento.
    * **Gruppo:** Scegliere tra i gruppi [privati](group-features.md) usando il menu a discesa. Verrà visualizzato solo se l'account è stato creato o aggiunto a un gruppo.
    * **Riga del tag:** Questa frase concisa verrà visualizzata nella pagina Web dell'evento sotto il titolo.
    * **Importa da mondo:** Per usare uno spazio eventi mondo creato per l'uso ripetuto, questa è la sezione del modulo da usare per importare il layout e la personalizzazione di tale mondo nell'evento. Tenere presenti le considerazioni seguenti:

    **Importare il proprio mondo:** Per importare un mondo, è stato creato e si è proprietari di:
    * Selezionare la freccia a discesa per visualizzare un elenco dei mondo creati.
    * Selezionare il mondo.
    * Dopo aver completato il resto del modulo dell'evento, attendere almeno 2 minuti prima di visitare lo spazio eventi in AltspaceVR per assicurarsi che le informazioni del database siano aggiornate e che il mondo venga generato.
    
    **Use Someone Else's World(Usare il mondo di un altro utente):**
    * Contattare il proprietario del mondo per richiedere che usi **la funzionalità Condividi** con amici in un singolo mondo per condividerla con l'utente.

3. **ID video YouTube:** Visibile nella pagina Web dell'evento, vengono aggiunti trailer o video di eventi YouTube alla pagina Web dell'evento, non al mondo. È necessaria solo la parte dell'URL dell'ID video: dQw4w9WgXcQ
4. **Twitter Handle (Handle Twitter):** Il flusso di Twitter verrà aggiunto alla pagina Web dell'evento. Se l'account Twitter è personale e non è correlato all'evento o all'associazione, è possibile che la condivisione sia in e over. È necessario solo l'handle: @elonmusk
5. **Ruoli contestuali:** Qui è possibile controllare i superpoteri o i ruoli [contestuali](../world-building/granting-roles.md) degli host di eventi, moderatori e altri ruoli all'interno dell'evento. Per aggiungerli, immettere il nome utente altspaceVR e assegnare loro un ruolo nel menu a discesa. Per rimuoverli, selezionare la casella di controllo Rimuovi e salvare la pagina Web dell'evento. NOTA: se si vuole concedere una funzionalità di moderazione host, è necessario aggiungerla come host e moderatore. Sono attualmente disponibili i ruoli contestuali seguenti:
    * **Host:** Aggiunge le [funzionalità front-row](../faqs/front-row-events.md) all'interfaccia dell'utente in AltspaceVR per aggiungere tali funzionalità.
    * **Moderatore:** Aggiunge funzionalità di moderazione all'interfaccia dell'utente, inclusa la possibilità di sms per ogni partecipante, disattivare globalmente l'audio per l'evento o rimuoverli dall'evento. Aggiungere di nuovo l'host e assegnare loro ruoli di moderazione se si vuole che abbia privilegi di moderazione.
    * **Solo Megaphone:** Aggiunge il pulsante Amplify My Voice alla relativa interfaccia tramite il pulsante Host Tools (Strumenti host).
    * **Terraformer:** Aggiunge il pulsante World Editor alla relativa interfaccia.
    * **Progetto pilota:** Aggiunge funzionalità di volo per l'utente. NOTA: è necessario abilitarla in Impostazioni/Input/Fly
    * **Performer Disodato di Musica:** Aggiunge funzionalità e funzionalità associate a eventi di musica e musica.
6. **Blocca utenti elencati:** Se si vuole impedire a un utente di accedere o se un utente è stato rimosso in precedenza dall'evento da un moderatore o da un host e l'evento è duplicato, verrà elencato il nome dell'utente elencato. Gli host eventi o gli amministratori possono aggiungere o rimuovere un utente elencato di blocco in qualsiasi momento.

Dopo aver completato il modulo e averne triplicato il controllo, **selezionare CREATE EVENT**.

> [!IMPORTANT]
> Se l'evento non viene creato correttamente, assicurarsi di avere almeno 10 caratteri nella Descrizione e/o di aver selezionato un modello, se selezionato, il nome del modello verrà impostato da bianco a blu.

## <a name="event-page-actions"></a>Azioni della pagina eventi

Nella pagina Web Evento sono disponibili le azioni e le opzioni seguenti:

1. Selezionare **MODIFICA** per apportare modifiche alle impostazioni dell'evento.
2. Selezionare **END EVENT (FINE** EVENTO) per terminare l'evento (ad esempio, se l'evento è più in anticipo).
3. Selezionare **SET TO DRAFT (IMPOSTA SU BOZZA)** per impostare l'evento su Draft (Bozza) anziché su Active (Attivo).
4. Se è stato apportato un aggiornamento al mondo importato, è necessario selezionare **RE-IMPORT WORLD** per visualizzare le modifiche nell'evento. Non dimenticare di reimpostare lo spazio nell'evento :)
5. Selezionare **DUPLICATE EVENT (DUPLICA** EVENTO) per duplicare l'evento per gli eventi futuri. Questo duplicato verrà quindi visualizzato in Eventi my/My Draft Events. Dovrai aggiornare il nuovo giorno/ora e attivarlo da questa pagina.
6. Selezionare **ADD AS MAIN EVENT (AGGIUNGI COME MAIN EVENT)** per impostare l'evento nell'elenco del calendario.
7. Selezionare **DELETE EVENT (ELIMINA** EVENTO) se si vuole eliminare completamente l'evento (non è possibile ripristinarlo).

Quando si è pronti, passare al menu Eventi > Eventi personali nell'interfaccia di AltspaceVR e immettere lo spazio eventi per Reimpostare lo spazio, esaminare le modifiche o continuare **la** personalizzazione. 

> [!IMPORTANT]
> Si tratta di una copia e le personalizzazioni dello spazio eventi sono solo per questo evento. Se si sta spendendo molto tempo per personalizzare lo spazio dell'evento, potrebbe essere meglio creare un mondo per l'evento **di uso ripetuto**.

Per altre informazioni sulla personalizzazione dello spazio eventi o sulla creazione di un mondo dello spazio eventi originale da importare:

* [Ricerca per categorie concedono ruoli ad altre persone nei miei Worlds?](../world-building/granting-roles.md)
* [Ricerca per categorie lasciare che le persone volino (o hanno altre capacità) nel mio mondo?](../world-building/adding-user-abilities.md)
* [Dove è possibile ottenere assistenza per la creazione di un mondo?](../world-building/getting-help.md)
* [Ricerca per categorie gestire i miei Worlds?](../world-building/managing-worlds.md)
* [Domande frequenti sulla creazione di un mondo](../world-building/world-building-faq.md)
* [Ricerca per categorie aggiungere punti di generazione personalizzati a Worlds?](../world-building/adding-custom-spawn-points.md)
* [Ricerca per categorie caricare i propri kit?](../world-building/uploading-custom-kits.md)
* [Ricerca per categorie iniziare a usare World Building Toolkit (Unity Uploader)?](../world-building/world-building-toolkit-getting-started.md)

## <a name="using-the-multimedia-console-for-a-slide-presentation"></a>Uso della console multimediale per una presentazione di una diapositiva

La console multimediale è un ottimo modo per organizzare il contenuto per una presentazione, incluse immagini, audio o video. Seguire le [istruzioni della console Multimediali](multimedia-console.md) per ottenere la configurazione per l'evento.

## <a name="branding-your-event-with-images"></a>Personalizzazione dell'evento con immagini

L'aggiunta di immagini allo spazio eventi, al logo e alla personalizzazione dell'azienda o persino a fotografie di se stessi, del team o di altri contenuti visivi è facile in AltspaceVR.

I requisiti dell'immagine sono:
* I file JPG o PNG sono accettati
* Dimensioni massime dell'immagine: 1920x1080
* Risoluzione: 72 DPI
* Dimensioni file: meno di 250 KB per file

Il processo prevede il caricamento dell'immagine in [AltspaceVR Photos,](https://account.altvr.com/photos)quindi l'uso di Photos in the World Editor in-world per importarle e posizionarle nello spazio del mondo degli eventi.

1. Passare a [Foto](https://account.altvr.com/photos) nel sito Web altspaceVR.
2. Selezionare **Carica**.
3. Selezionare **Sfoglia** per aprire una finestra di dialogo nel computer e individuare e selezionare l'immagine ottimizzata.
4. Selezionare **Open** (Apri).
5. Selezionare **CREATE PHOTO**.
6. Ripetere questa operazione per tutte le immagini.

In AltspaceVR e nel mondo degli eventi posizionarsi vicino al punto in cui si vuole posizionare l'immagine. Se si sta creando questa operazione per un evento **Di** uso ripetuto, assicurarsi di essere nel proprio mondo e non nello spazio eventi.

1. Nell'angolo inferiore destro dell'interfaccia utente selezionare **World Editor/Editor Panel (Editor mondo/Pannello editor)**
2. Fare clic **sulla scheda Miniera** nella parte inferiore.
3. Selezionare **Foto.**
4. Le foto vengono archiviate in ordine cronologico di caricamento, quindi l'immagine più recente caricata deve essere la prima immagine nell'elenco. Selezionarlo per aggiungerlo al mondo.
5. Usando il cursore del dispositivo, afferrare l'immagine e posizionarla nel punto desiderato.
    * Puoi ridimensionarlo usando i controller (in genere scorrendo il cursore orizzontalmente sul touch pad nella realtà virtuale o usando il mouse in modalità 2D).
    * Per ottimizzare la posizione e la rotazione dell'immagine, selezionare il simbolo **GEAR** nell'immagine nell'editor e impostare rotazione e posizione in modo appropriato.
    * È anche possibile ridimensionare l'immagine con la funzionalità Scala.

> [!NOTE]
> Quando la modalità di modifica è attivata (testo arancione), si avrà automaticamente la possibilità di eseguire il fly, consentendo uno spostamento più semplice per posizionare le immagini più in alto nel mondo degli eventi.

6. Ripetere questa operazione per ogni posizionamento dell'immagine.
7. Quando le immagini sono impostate  sul posto, selezionare Blocca tutto se non sono state bloccate singolarmente, quindi disattivare la modalità di modifica e chiudere l'editor.
8. Usare solo un massimo di cinque foto per evento.

## <a name="adding-3d-objects-using-world-editor-and-kits"></a>Aggiunta di oggetti 3D usando World Editor e kit

AltspaceVR consente di importare oggetti 3D nei mondo con World Editor. Sono attualmente disponibili molti World Editors Kit per l'uso e altri ancora. Sono presenti spaceship, razzi, animali animati, animali, alberi, piante e molti oggetti diversi. Oppure è possibile aggiungere i propri kit alla raccolta pubblica o per uso personale oppure prendere in considerazione l'uso di una delle app [AltspaceVR MRE,](../world-building/using-mixed-reality-extensions.md)che portano oggetti con interazione nel proprio mondo, ad esempio bambini, ali, abbigliamento, hat o altri oggetti con cui è possibile interagire. Si prevede che l'elenco di oggetti si espandono a breve.

Le istruzioni sono incentrate sull'uso di elementi già presenti nei kit. Per altre informazioni sull'aggiunta e l'importazione di oggetti 3D in AltspaceVR, vedere "Come importare modelli [glTF nei miei worlds?"](../world-building/importing-models.md) e ["Ricerca per categorie i miei kit?"](../world-building/uploading-custom-kits.md).

Per aggiungere un oggetto 3D esistente da World Building Kit nel mondo degli eventi, con l'opzione World Editor/Editor Panel aperta e la modalità di modifica abilitata:

1. Esplorare i kit per l'oggetto da importare e selezionarlo.
2. Selezionare l'oggetto kit con il cursore e posizionarlo. Usare l'icona a forma di ingranaggio sull'oggetto nell'editor globale per usare le opzioni Posizione, Ruota e Scala per l'immissione manuale dei numeri.
3. Quando l'oggetto viene posizionato nella posizione corretta, bloccarlo facendo clic sull'icona Blocca.
4. Se si vuole, aggiungere un altro oggetto. Per migliorare il supporto degli utenti di Oculus Quest, è possibile aggiungere oggetti 3D, mantenendo le selezioni su un massimo di elementi di cinque diversi kit singoli. Non usare più di 200 oggetti in un mondo.
5. Al termine, bloccare tutti gli elementi, disattivare la modalità di modifica e chiudere World Editor. Passeggiare. Invita alcuni tester a visitarlo e a consultarlo e prepararti per il tuo evento eccezionale.

Per altre informazioni sui World Editor Kit e sull'aggiunta di oggetti 3D ad AltspaceVR:

* [Che cos'è il Programma di accesso anticipato?](../world-building/early-access.md)
* [Come importare modelli glTF in Worlds?](../world-building/importing-models.md)
* [Ricerca per categorie usare un MRE nel mondo?](../world-building/using-mixed-reality-extensions.md)

## <a name="how-to-record-or-live-stream-my-event"></a>Come registrare o Live Stream Evento

Per istruzioni sulla registrazione o lo streaming live dell'evento, vedere il documento di supporto seguente:

* [Come registrare o Live Stream Evento](recording-and-live-streaming.md)