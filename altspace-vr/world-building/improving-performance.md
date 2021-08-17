---
title: Miglioramento delle prestazioni del mondo
description: Informazioni su come misurare, risolvere i problemi e migliorare le prestazioni dei sistemi AltspaceVR usando gli strumenti di diagnostica.
ms.date: 03/11/2021
ms.topic: article
keywords: prestazioni, risoluzione dei problemi
ms.openlocfilehash: 79d2bc43858c99652439aafa159c23f48eb3aa299c2b183936e40b1794fe444e
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126925"
---
# <a name="improving-world-performance"></a>Miglioramento delle prestazioni del mondo

Vogliamo che le persone abbiano un'esperienza ottimale in modo che le prestazioni, o il livello di prestazioni del mondo sui visori VR, sono estremamente importanti. Il sistema World Building è progettato per prestazioni ottimali per i casi d'uso più comuni. Per ottimizzare la presenza, vedere questa guida. Altspace scade per supportare ogni piattaforma hardware. Anche se si consiglia ai World Builder di effettuare il push dei limiti, per i worlds pubblici è consigliabile scegliere come destinazione Oculus Quest e qualsiasi piattaforma basata su PC come Windows Mixed Reality, Oculus Rift/Rift S o LASE Vive. Per semplicità, se il mondo viene eseguito bene in una ricerca, è probabilmente ideale per Altspace.

## <a name="tools-and-measurement"></a>Strumenti e misurazione

Diagnostica amministratore è uno strumento offline disponibile nel sito Web, altvr.com. Se si passa a [Worlds > My Worlds](https://account.altvr.com/users/sign_in), si trova world e si seleziona "Diagnostics", verrà visualizzato un messaggio simile al seguente:

![Finestra Diagnostica amministratore](images/performance.png)

Queste sono più linee guida rispetto ai requisiti. Le prestazioni dipendono dal numero di oggetti e dalla modalità di disposta. Ad esempio, se si dispone di 500 oggetti distribuiti in 2 chilometri, le prestazioni saranno probabilmente ottimali. Tuttavia, se si inseriranno gli stessi 500 oggetti in un'area strettamente compatta, probabilmente si verificano problemi. Ciò è dovuto al fatto che le prestazioni dipendono dal contenuto del campo di visualizzazione di una persona. Il modo migliore per testare è l'hop in Altspace e il teletrasporto in tutto il mondo. Se si notano problemi o si verificano problemi, si tratta di punti problematici da analizzare.

Se si attenersi a queste raccomandazioni, è possibile configurare se stessi per il successo. Esamini ora questo esempio di diagnostica tratto da un mondo in primo piano effettivo: 

* **Oggetti** : numero totale di oggetti nel mondo. Tutto è un oggetto, Artifacts, Foto, genera punti e così via. È consigliabile rimanere sotto un determinato numero, ma questo è flessibile. Se si va oltre, viene indicato il problema con un punto esclamativo giallo, come illustrato di seguito. Tuttavia, in questo caso ci sono due aree separate in questo mondo, quindi la densità non è elevata.
* **Kit:** numero totale di kit world building univoci usati. Ciò influisce sul tempo di download iniziale durante il caricamento di World. I kit contengono Artifacts, il menu degli oggetti che è possibile generare nel mondo. 

> [!NOTE] 
> Se si usa un singolo artefatto da un kit, è necessario scaricare gli asset del kit. È quindi estremamente costoso usare solo pochi Artifacts da un singolo kit. 

* **Kits--Mobile** : dimensioni totali di tutti gli asset del kit che una persona in una ricerca deve scaricare prima di entrare nel Mondo. Provare a non fare in modo che gli utenti attendano 5 minuti per scaricare tutto il necessario per il mondo.
* **Foto:** numero totale di foto usate, che tendono ad avere un impatto maggiore sulle prestazioni rispetto Artifacts. Usare con parsimonio.
Modello- Dispositivi mobili: se si usa Unity Uploader, mantenere le dimensioni del download ridotte.
* **Skybox--Mobile:** se si usano skybox personalizzati, mantenere le dimensioni del file ridotte in modo che gli utenti non osercitino lo "schermo nero" (memoria video insufficiente).
* **Kit mancanti/non validi/Artifacts:** riferimenti a kit o Artifacts... Si ha un'idea per una metrica? È possibile farlo sapere.
Anche in questo caso, questi non sono requisiti, quindi vengono visualizzate icone di stato verdi, gialle e rosse. Anche un mondo con una serie di indicatori rossi può essere ancora in primo piano. Viene testato anche in Altspace. [Per assistenza, contattare](getting-help.md)Microsoft. 

## <a name="load-time"></a>Tempo di caricamento

Quando una persona inizia a recarsi nel mondo (tenta di entrare), carica prima il modello. Gli asset modello (file) verranno scaricati per la piattaforma e verrà visualizzato "Loading Environment" (Ambiente di caricamento). Scarica quindi gli asset Skybox e Kit. Infine, caricano tutti gli oggetti mentre visualizzano "Loading Objects". Il download di tutti gli asset può richiedere alcuni minuti a seconda della larghezza di banda Internet. Il caricamento degli oggetti è piuttosto rapido. Anche se gli asset vengono scaricati da server veloci in tutto il mondo, Altspace usa tecniche di memorizzazione nella cache per evitare di scaricare ripetutamente gli stessi file. Tecnicamente, il tempo di caricamento iniziale non influisce sulle prestazioni di una persona dopo l'accesso al Mondo, ma fa parte dell'esperienza complessiva, quindi cerca di non far attendere troppo a lungo le persone durante il viaggio nel mondo. È consigliabile valutare attentamente i kit da usare e essere fantasiosi facendo di più con meno.

## <a name="troubleshooting-and-tips"></a>Risoluzione dei problemi e suggerimenti

**Le persone vedono una "schermata nera"** In genere, ciò è dovuto al fatto che la memoria video del dispositivo è esaurita. Provare a ridurre il numero di oggetti nell'area problematica del mondo e a ridurre le dimensioni di elementi come Skybox o Template o il numero di Foto. Questi tipi tendono ad avere l'impatto più elevato sull'utilizzo della memoria video.

**Si stanno arrestando in modo anomalo le persone**
    * A volte un kit o un artefatto danneggiato può causare questo problema.
    * Anche le animazioni o gli shader in shader possono causare questo problema.
    * È possibile fare attenzione ai modelli e ai kit personalizzati.
    * Eseguire spesso il backup del mondo, soprattutto durante lo sviluppo iniziale. Usare questi backup per ottenere informazioni sugli elementi aggiunti di recente che causano l'arresto anomalo delle persone.

**Lasciare "headroom"**
    * Tenere presente che nel mondo possono essere presenti 20-30 persone contemporaneamente. Cosa succede se tutte queste persone si aggirano attorno a un incendio. Si vogliono comunque inserire 200 ciottoli sull'incendio? Probabilmente non è una buona idea. Lasciare un po' di spazio per Avatars e Interactables (come i giocatori).
    * Meno è meglio.

**Pianificare in anticipo** Pensare a ciò che si vuole creare e a creare spazio. È facile spostarsi in Altspace.

**Usare lo strumento di diagnostica in anticipo e spesso** Aggiungere un segnalibro e aggiornarlo una volta ogni tanto. Alla fine, nella realtà virtuale saranno disponibili strumenti simili che saranno più accessibili.

**Fare amici con gli utenti di Oculus Quest** Invitali a entrare nel mondo per testarli. Eseguire test accurati e spesso. Testare i reciproci Worlds! Nulla supera il test sull'oggetto reale.

**Aggiungi amici come "Amministratori" per il tuo mondo** Modifica il tuo mondo e aggiungi gli amici all'elenco Di amministratori. In questo modo potranno visualizzare lo strumento di diagnostica per il mondo. Prestare attenzione, tuttavia, perché possono anche modificare altri aspetti del mondo. 

**L'ottimizzazione delle prestazioni è difficile, quindi la community è desiderosa di assistenza** Partecipare al [discord altspaceVR ufficiale](https://discordapp.com/invite/altspacevr) *Visitare il canale #world-building per assistenza generale con i mondo.
    * Visitare i canali di MRE SDK per assistenza specifica con informazioni più tecniche e guida correlata a Unity Uploader (modelli e kit personalizzati)