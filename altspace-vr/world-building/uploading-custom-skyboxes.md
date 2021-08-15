---
title: Caricamento di Skybox personalizzati
description: Istruzioni dettagliate sul caricamento e sulla risoluzione dei problemi degli skybox personalizzati in Esperienze AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: skyboxes, risoluzione dei problemi
ms.openlocfilehash: 912df5a4c87b7a5817824c6ee75ec8707439636b83b4d46996bbc4129ee6e9de
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126794"
---
# <a name="uploading-custom-skyboxes"></a>Caricamento di Skybox personalizzati

Skybox è un modo per creare uno **sfondo** per il mondo che rende l'esperienza più coinvolgente. Esistono diversi tipi di Skybox, ma attualmente è supporto **equirettangolare**. Ecco un esempio preso con una fotocamera a 360 (altro esempio [qui):](http://moments.mankindforward.com/) 

![360 visualizzazione equirettangolare di un living](images/custom-skyboxes-img-01.jpeg)

È anche possibile usare [Unity Uploader,](world-building-toolkit-getting-started.md) ma questo approccio è più semplice.

1. Passare a [Worlds > Skyboxes](https://account.altvr.com/skyboxes) e premere il **pulsante Crea** a destra

![Pagina del sito Web di Worlds aperta nel pannello skyboxes](images/custom-skyboxes-img-02.png)

2. Immettere un nome e specificare l'immagine 360. Non deve essere una foto, ci sono programmi che consentono di disegnare il proprio o è possibile cercare alcuni online. Al termine, selezionare **Crea**. 

![Modulo di creazione skybox](images/custom-skyboxes-img-03.png)

3. Facoltativamente, è possibile caricare **un'immagine** di anteprima in modo da poter identificare facilmente questo skybox. È anche possibile caricare l'audio di ambiente in formato WAV. 

> [!IMPORTANT]
> Dopo aver caricato l'immagine a 360, è consigliabile caricare separatamente immagini di anteprima e audio di ambiente. Se si caricano insieme, le dimensioni dei file possono essere sufficientemente grandi da bloccare il processo. [Jetsons World è](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) un ottimo esempio di come usare skybox con audio ambientale. Si noti che World-Builder ha mantenuto basso il volume audio e i suoni uditi sono sporadici in modo che le persone non si annoino. 

4. Immettere world e aprire World Editor. In Skyboxes selezionare il nuovo Skybox. In pochi secondi il cielo cambierà letteralmente. Anche altri utenti del mondo potranno vedere il cambiamento del cielo. Per tornare indietro, scegliere la **skybox** predefinita nello stesso elenco. 

## <a name="troubleshooting"></a>Risoluzione dei problemi

**C'è una linea o una linea nel cielo :-(.** Si tratta di un bug che verrà risolto a breve

**Upload non riuscito**
    * provare a caricare solo l'immagine a 360 da sola
    * provare con un altro file più piccolo come test

**Non è possibile trovare una foto a 360**
    * Flickr è una buona fonte (modificare i filtri per trovare quelli creative commons)
    * Prendere il proprio! Abbiamo avuto successo con le fotocamere di Ricoh. 
**Il cielo sembra sgranocchiato o a blocchi** Potrebbe essere necessario trovare un'immagine con risoluzione superiore. In genere circa 2-5 MB e ~5000 px x 2000 px

**Mi fa male il framerate del mondo.**
L'immagine è probabilmente troppo grande. Alcuni skybox generati possono essere 8.000. In genere sono disponibili con versioni di 2.000 per dispositivi mobili. Usare questa opzione.

**Aiutami con l'audio di ambiente**
    * Usare software gratuito come Audacity per ridurre il volume o creare cicli personalizzati. Tenere presente che l'audio verrà ripetuto e riprodotto nelle orecchi delle persone, quindi mantenerlo basso e non fastidioso
    * [Free Sound](https://freesound.org/) è una buona fonte di suoni reali
