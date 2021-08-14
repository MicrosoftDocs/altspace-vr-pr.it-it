---
title: Caricamento di Skybox personalizzati
description: Istruzioni dettagliate sul caricamento e la risoluzione dei problemi dei skybox personalizzati nelle esperienze altspaceVR.
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

Skybox è un modo per creare uno **sfondo per** il mondo che rende l'esperienza più coinvolgente. Esistono diversi tipi di Skybox, ma attualmente è disponibile **il supporto di equirettangolare**. Ecco un esempio preso con una fotocamera 360 (altro esempio [qui):](http://moments.mankindforward.com/) 

![Visualizzazione a 360 elementi equirettangolari di un locale](images/custom-skyboxes-img-01.jpeg)

È anche possibile usare [Unity Uploader,](world-building-toolkit-getting-started.md) ma questo approccio è più semplice.

1. Passare a [Worlds > Skyboxes](https://account.altvr.com/skyboxes) e premere il **pulsante Create (Crea)** a destra

![Pagina del sito Web Worlds aperta nel pannello Skyboxes](images/custom-skyboxes-img-02.png)

2. Immettere un nome e specificare l'immagine 360. Non deve essere una foto, sono disponibili programmi che consentono di disegnarlo o è possibile cercarlo online. Al termine, selezionare **Crea**. 

![Modulo per la creazione di Skybox](images/custom-skyboxes-img-03.png)

3. Facoltativamente, è possibile caricare **un'immagine** di anteprima in modo da poter identificare facilmente questo skybox. È anche possibile caricare l'audio di ambiente in formato WAV. 

> [!IMPORTANT]
> È consigliabile caricare separatamente le immagini di anteprima e l'audio di ambiente, dopo aver caricato l'immagine 360. Se si caricano insieme, le dimensioni dei file possono essere sufficientemente grandi da bloccare il processo. [Jetsons World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) è un ottimo esempio di come usare skybox con audio ambientale. Si noti che World-Builder ha mantenuto basso il volume audio e i suoni uditi sono sporadici, in modo che le persone non siano infastidite. 

4. Immettere world e aprire World Editor. In Skyboxes selezionare il nuovo Skybox. In pochi secondi, il cielo cambierà letteralmente. Anche altri utenti del mondo potranno vedere il cambiamento del cielo. Per tornare indietro, scegliere il **valore** predefinito skybox nello stesso elenco. 

## <a name="troubleshooting"></a>Risoluzione dei problemi

**C'è una linea o una linea nel cielo :-(.** Si tratta di un bug che verrà risolto a breve

**Upload non riuscito**
    * provare a caricare solo l'immagine 360 da sola
    * Provare con un altro file più piccolo come test

**Non è possibile trovare una foto a 360**
    * Lo sfarfallio è una buona fonte (modificare i filtri per trovare quelli creative comuni)
    * Take Your Own! Abbiamo avuto successo con le fotocamere di Ricoh. 
**Il cielo sembra granulare o bloccante** Potrebbe essere necessario trovare un'immagine con risoluzione superiore. In genere circa 2-5 MB e ~5000 px x 2000 px

**Mi danneggia la frequenza dei fotogrammi del mondo.**
L'immagine è probabilmente troppo grande. Alcuni skybox generati possono essere di 8 KB. In genere vengono usate con versioni 2K per dispositivi mobili.

**Aiutami con l'audio di ambiente**
    * Usare il software gratuito, ad esempio IlVaty, per ridurre il volume o creare cicli personalizzati. Tenere presente che l'audio verrà ripetuto e riprodotto nelle persone, quindi mantenerlo basso e non fastidioso
    * [Free Sound](https://freesound.org/) è una buona fonte di suoni gratuiti
