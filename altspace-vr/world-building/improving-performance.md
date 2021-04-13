---
title: Miglioramento delle prestazioni del mondo
description: Scopri come misurare, risolvere i problemi e migliorare le prestazioni dei tuoi AltspaceVR mondi usando gli strumenti di diagnostica.
ms.date: 03/11/2021
ms.topic: article
keywords: prestazioni, risoluzione dei problemi
ms.openlocfilehash: 558ce2e089aecc206445c6b7bf99423f2d5c45cc
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212633"
---
# <a name="improving-world-performance"></a>Miglioramento delle prestazioni del mondo

Si vuole che gli utenti abbiano una buona esperienza, quindi le prestazioni o il modo in cui il mondo viene eseguito su cuffie VR è molto importante. Il nostro sistema di compilazione globale è progettato per prestazioni ottimali per i casi d'uso più comuni. Questa guida è destinata a massimizzare la presenza. Altspace aspira a supportare tutte le piattaforme hardware. Sebbene si incoraggino i compilatori del mondo a eseguire il push dei limiti, per i mondi pubblici è consigliabile usare l'Oculus missione e qualsiasi piattaforma basata su PC come la realtà mista di Windows, Oculus Rift/Rift S o HTC vive. Per mantenerlo semplice, se il mondo viene eseguito correttamente in una ricerca, è probabilmente ideale per Altspace.

## <a name="tools-and-measurement"></a>Strumenti e misurazione

La diagnostica dell'amministratore è uno strumento offline disponibile sul nostro sito Web, altvr.com. Se si passa a [worlds > My](https://account.altvr.com/users/sign_in)Worlds, trovare il mondo e selezionare "Diagnostics" (diagnostica), verrà visualizzato un risultato simile al seguente:

![Finestra di diagnostica dell'amministratore](images/performance.png)

Queste sono altre linee guida rispetto ai requisiti. Le prestazioni dipendono dal numero di oggetti disponibili e dal modo in cui sono disposti. Se, ad esempio, si dispone di 500 oggetti distribuiti su 2 chilometri, le prestazioni saranno probabilmente ottimali. Tuttavia, se si inseriscono gli stessi oggetti 500 in un'area strettamente compressa, probabilmente si noterà un problema. Ciò è dovuto al fatto che le prestazioni dipendono da ciò che si trova all'interno del campo di visualizzazione di una persona. Il modo migliore per testare è passare a Altspace e Teleport in tutto il mondo. Se si riscontrano problemi o si verificano problemi, si tratta di punti problematici che è opportuno esaminare.

Attenendosi a queste indicazioni, l'utente si configura per il successo. Esaminiamo questo esempio di diagnostica preso da un mondo in primo piano: 

* **Oggetti** : numero totale di oggetti nel mondo. Tutto è un oggetto, ovvero elementi, foto, punti di spawn e così via. Si consiglia di restare sotto un certo numero, ma questa operazione è flessibile. Se si procede, viene indicato il problema con un punto esclamativo giallo, come illustrato di seguito. Tuttavia, in questo caso esistono due aree separate in questo mondo, quindi la densità non è alta.
* **Kit** : numero totale di esclusivi kit di compilazione globale usati. Questa operazione influisca sul tempo di download iniziale durante il caricamento del mondo. I kit contengono elementi, il menu degli oggetti che è possibile generare in tutto il mondo. 

> [!NOTE] 
> Se un singolo artefatto viene usato da un kit, è necessario scaricare gli asset del kit. Quindi, è molto costoso usare solo alcuni artefatti da un singolo kit. 

* **Kit--mobile** -dimensione totale di tutte le risorse del kit che una persona in una missione deve scaricare prima di entrare nel mondo. Provare a non fare in modo che gli utenti attendano 5 minuti per scaricare tutti gli elementi necessari per il mondo.
* **Foto** : numero totale di foto utilizzate, che tendono a avere un maggiore effetto sulle prestazioni rispetto agli artefatti. Usare con moderazione.
Modello--mobile: se si usa l'Uploader Unity, è possibile ridurre le dimensioni di download.
* **SKYBOX--mobile** -se si usa un skybox personalizzato, è possibile ridurre le dimensioni del file in modo che gli utenti non ottengano la "schermata nera" (esaurimento della memoria video).
* **Kit/artefatti mancanti/non validi** -riferimenti a kit o artefatti problematici... Si ha un'idea per una metrica? Inviaci informazioni
Ancora una volta, questi non sono i requisiti per visualizzare le icone di stato verde, giallo e rosso. Anche un mondo con una serie di indicatori rossi potrebbe essere ancora in primo piano. Il test viene testato in Altspace. [Se ti serve assistenza, contattaci](getting-help.md). 

## <a name="load-time"></a>Tempo di caricamento

Quando una persona inizia a viaggiare al mondo (tenta di immettere), caricherà innanzitutto il modello. Verranno scaricati gli asset del modello (file) per la piattaforma e verrà visualizzato il "caricamento dell'ambiente". Quindi scaricheranno le risorse di SKYBOX e kit. Infine, caricherà tutti gli oggetti mentre vedranno "caricamento di oggetti". Il download di tutti gli asset può richiedere più di pochi minuti, a seconda della larghezza di banda Internet. il caricamento degli oggetti è piuttosto rapido. Mentre gli asset vengono scaricati da server veloci in tutto il mondo, Altspace usa le tecniche di memorizzazione nella cache per evitare di riscaricare ripetutamente gli stessi file. Tecnicamente, il tempo di caricamento iniziale non influisce sulle prestazioni di una persona dopo l'ingresso nel mondo, ma fa parte dell'esperienza complessiva, quindi provare a non far aspettare troppo tempo quando si viaggia al mondo. Si consiglia di valutare con attenzione i kit da usare e di avere un'immaginazione maggiore con minore.

## <a name="troubleshooting-and-tips"></a>Risoluzione dei problemi e suggerimenti

Gli **utenti vedono una "schermata nera"** In genere, ciò è dovuto al fatto che il dispositivo ha esaurito la memoria del video. Provare a ridurre il numero di oggetti nell'area problematica del mondo e ridurre le dimensioni di elementi come il SKYBOX o il modello o il numero di foto. Questi tipi tendono a avere un effetto maggiore sull'utilizzo della memoria video.

**Persone arrestate in modo anomalo**
    * A volte un kit o un artefatto danneggiato può causare questa operazione.
    * Anche gli shader o le animazioni folli potrebbero causare questa situazione.
    * Guarda gli elementi in modelli e kit personalizzati.
    * Esegui il backup del mondo spesso, soprattutto durante le fasi iniziali dello sviluppo. Usare questi backup per affinare gli elementi aggiunti di recente che causano l'arresto anomalo degli utenti.

**Lascia "altezza"**
    * Tenere presente che è possibile che si disponga di 20-30 persone nel mondo nello stesso momento. Cosa accade se tutti gli utenti sono stati ammucchiati intorno a un falò. Si vuole comunque mettere a fuoco 200 ciottoli? Probabilmente non è consigliabile. Lascia spazio per gli avatar e Interactables (ad esempio basket).
    * Meno è meglio.

**Pianificare in anticipo** Si pensi a cosa si vuole creare e allo spazio. È facile da aggirare in Altspace.

**Usare lo strumento di diagnostica in anticipo e spesso** Aggiungere un segnalibro e aggiornarlo una sola volta. Infine, in VR saranno disponibili strumenti simili che saranno più accessibili.

**Crea amici con gli utenti di Oculus quest** Invito a entrare nel mondo per aiutarti a eseguire il test. Eseguire test approfonditi e spesso. Testare i mondi di ogni altro. Il test non è mai stato fatto.

**Aggiungere amici come "amministratori" per il mondo** Modificare il mondo e aggiungere gli amici all'elenco degli amministratori. Questo consentirà di visualizzare lo strumento di diagnostica per il mondo. Prestare attenzione perché possono anche modificare altri aspetti del mondo. 

**L'ottimizzazione delle prestazioni è molto difficile, quindi la nostra community è ansiosa di aiutarti** Partecipa alla [discordia ufficiale di AltspaceVR](https://discordapp.com/invite/altspacevr) * visita il canale per la creazione di #world per assistenza generale con i mondi.
    * Visitare i canali SDK di MRE per assistenza specifica con la guida più tecnica e relativa all'Uploader Unity (modelli e kit personalizzati)