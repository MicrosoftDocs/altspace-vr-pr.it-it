---
title: Miglioramento delle prestazioni del mondo
description: Informazioni su come misurare, risolvere i problemi e migliorare le prestazioni dei mondi AltspaceVR usando gli strumenti di diagnostica.
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

Vogliamo che le persone abbiano un'esperienza ottimale in modo che le prestazioni, o il livello di prestazioni del mondo nei visori VR, sia estremamente importante. Il sistema World Building è progettato per prestazioni ottimali per i casi d'uso più comuni. Se si sta cercando di ottimizzare La presenza, questa guida è il modo più utile. Altspace desidera supportare ogni piattaforma hardware. Anche se è consigliabile che World Builders eserviti il push dei limiti, per i mondi pubblici è consigliabile scegliere come destinazione Oculus Quest e qualsiasi piattaforma basata su PC come Windows Mixed Reality, Oculus Rift/Rift S o l'opzione DISAAAA. Per semplicità, se il mondo viene eseguito bene in una ricerca, è probabilmente ideale per Altspace.

## <a name="tools-and-measurement"></a>Strumenti e misurazione

Diagnostica amministratore è uno strumento offline disponibile nel sito Web, altvr.com. Se si passa a [Worlds > My Worlds](https://account.altvr.com/users/sign_in), si trova il proprio mondo e si seleziona "Diagnostics", verrà visualizzato un messaggio simile al seguente:

![Finestra di diagnostica dell'amministratore](images/performance.png)

Queste sono più linee guida rispetto ai requisiti. Le prestazioni dipendono dal numero di oggetti e dal modo in cui sono disposti. Ad esempio, se si dispone di 500 oggetti distribuiti su 2 chilometri, le prestazioni probabilmente andranno bene. Tuttavia, se si mettono gli stessi 500 oggetti in un'area strettamente imballata, è probabile che si verificano problemi. Ciò è dovuto al fatto che le prestazioni dipendono da ciò che si trova all'interno del campo di visualizzazione di una persona. Il modo migliore per testare è quello di saltare in Altspace e teletrasportarsi in tutto il mondo. Se si verificano problemi o si verificano problemi, si tratta di punti problematici da analizzare.

Se si attenersi a queste raccomandazioni, si è configurato per il successo. Si esamini ora questo esempio di diagnostica tratto da un mondo in primo piano effettivo: 

* **Oggetti** : numero totale di oggetti nel mondo. Tutto è un oggetto, Artifacts, Foto, Genera punti e così via. È consigliabile rimanere sotto un determinato numero, ma questo è flessibile. Se si va oltre, viene indicato il problema con un punto esclamativo giallo, come illustrato di seguito. Tuttavia, in questo caso, esistono due aree separate in questo mondo, quindi la densità non è elevata.
* **Kit:** numero totale di kit di world building univoci usati. Ciò influisce sul tempo di download iniziale durante il caricamento di World. I kit contengono Artifacts, il menu oggetti che è possibile generare nel mondo. 

> [!NOTE] 
> Se un singolo artefatto viene usato da un kit, è necessario scaricare gli asset di tale kit. È quindi estremamente costoso usare solo pochi Artifacts da un singolo kit. 

* **Kits--Mobile:** dimensioni totali di tutti gli asset del kit che una persona in una ricerca deve scaricare prima di entrare nel mondo. Provare a non fare in modo che le persone attendano 5 minuti per scaricare tutto il necessario per il mondo.
* **Foto:** numero totale di foto usate, che tendono ad avere un impatto sulle prestazioni superiore rispetto a Artifacts. Usare con parsimonio.
Modello--Mobile: se si usa Unity Uploader, mantenere le dimensioni del download ridotte.
* **Skybox--Mobile:** se si usano skybox personalizzati, mantenere le dimensioni del file ridotte in modo che gli utenti non osno ottenere lo "schermo nero" (memoria video insufficiente).
* **Kit mancanti/non validi/Artifacts:** riferimenti a kit o Artifacts ... Hai un'idea per una metrica? Facci sapere!
Anche in questo caso, questi non sono requisiti, quindi vengono visualizzate le icone di stato verdi, gialle e rosse. Anche un mondo con un gruppo di indicatori rossi può ancora essere in primo piano. Viene testato in Altspace, quindi è consigliabile farlo anche tu. [Contattare Microsoft per ottenere assistenza.](getting-help.md) 

## <a name="load-time"></a>Tempo di caricamento

Quando una persona inizia a recarsi nel mondo (tenta di entrare), carica prima il modello. Scaricano gli asset del modello (file) per la piattaforma e visualizzano "Ambiente di caricamento". Verranno quindi scaricati gli asset Skybox e Kit. Infine, caricano tutti gli oggetti mentre visualizzano "Caricamento di oggetti". Il download di tutti gli asset può richiedere alcuni minuti a seconda della larghezza di banda Internet. Il caricamento degli oggetti è piuttosto rapido. Mentre gli asset vengono scaricati da server veloci in tutto il mondo, Altspace usa tecniche di memorizzazione nella cache per evitare il ricaricamento ripetuto degli stessi file. Tecnicamente, il tempo di caricamento iniziale non influisce sulle prestazioni di una persona dopo l'accesso al mondo, ma fa parte dell'esperienza complessiva, quindi cerca di non far attendere troppo a lungo quando viaggia nel tuo mondo. È consigliabile considerare attentamente i kit da usare e da immaginare facendo di più con meno.

## <a name="troubleshooting-and-tips"></a>Risoluzione dei problemi e suggerimenti

**Gli utenti vedono una "schermata nera"** In genere, ciò è dovuto al fatto che il dispositivo ha esaurito la memoria video. Provare a ridurre il numero di oggetti nell'area problematica del mondo e a ridurre le dimensioni di elementi come Skybox o Template o il numero di Foto. Questi tipi tendono ad avere il massimo impatto sull'utilizzo della memoria video.

**Arresto anomalo delle persone**
    * A volte un kit o un artefatto danneggiato può causare questo problema.
    * Anche questo potrebbe essere causato da shader o animazioni pazzesche.
    * Fare attenzione alle operazioni in modelli e kit personalizzati.
    * Eseguire spesso il backup del mondo, soprattutto durante lo sviluppo anticipato. Usare questi backup per affinarsi su ciò che è stato aggiunto di recente che causa l'arresto anomalo delle persone.

**Lasciare "headroom"**
    * Tenere presente che possono essere presenti 20-30 persone nel mondo contemporaneamente. Cosa succede se tutte queste persone sono state invase da un falò. Si vogliono comunque mettere 200 ciottoli dall'incendio? Probabilmente non è una buona idea. Lasciare un po' di spazio per Avatars e Interactables (ad esempio basket).
    * Meno è meglio.

**Pianificare in anticipo** Pensare a ciò che si vuole creare e spaziare le cose. È facile spostarsi in Altspace.

**Usare lo strumento di diagnostica in anticipo e spesso** Aggiungere un segnalibro e aggiornarlo una volta ogni tanto. Alla fine, nella realtà virtuale saranno disponibili strumenti simili che saranno più accessibili.

**Fare amici con gli utenti di Oculus Quest** Invitali a entrare nel tuo mondo per testarli. Eseguire test accurati e spesso. Testare i mondi degli altri. Nulla supera il test sulla cosa reale.

**Aggiungere amici come "Amministratori" per il mondo** Modificare il mondo e aggiungere gli amici all'elenco Amministratore. In questo modo verranno visualizzati gli strumenti di diagnostica per il mondo. Prestare attenzione, tuttavia, perché possono anche modificare altri aspetti del mondo. 

**L'ottimizzazione delle prestazioni è difficile, quindi la community è desiderosa di aiutare** Partecipa alla [discordia altspaceVR](https://discordapp.com/invite/altspacevr) ufficiale *Visita il canale #world-building per assistenza generale con i mondi.
    * Visitare i canali di MRE SDK per assistenza specifica con informazioni più tecniche e su Unity Uploader (modelli e kit personalizzati)