---
title: Caricamento di SKYBOX personalizzati
description: Istruzioni dettagliate sul caricamento e la risoluzione dei problemi di SKYBOX personalizzati in AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: SKYBOX, risoluzione dei problemi
ms.openlocfilehash: 02d5bc762dc36d4195100e8155d6250789e833f7
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213261"
---
# <a name="uploading-custom-skyboxes"></a>Caricamento di SKYBOX personalizzati

Un skybox è un modo per creare uno **sfondo** per il mondo che rende l'esperienza più immersiva. Sono disponibili diversi tipi di SKYBOX, ma è attualmente supportata la **equirettangolare**. Di seguito è riportato un esempio con una fotocamera 360 (altro esempio [qui](http://moments.mankindforward.com/)): 

![360 visualizzazione equirettangolare di una sala da lavoro](images/custom-skyboxes-img-01.jpeg)

È anche possibile usare l'utilità di [caricamento Unity](world-building-toolkit-getting-started.md) ma questo approccio è più semplice.

1. Passare a [worlds > SKYBOX](https://account.altvr.com/skyboxes) e fare clic sul pulsante **Create (crea** ) a destra.

![Pagina del sito Web Worlds aperta al pannello SKYBOX](images/custom-skyboxes-img-02.png)

2. Immettere un nome e specificare l'immagine 360. Non è necessario che sia una foto, sono disponibili programmi che consentono di creare un progetto personalizzato oppure è possibile eseguire ricerche in linea. Al termine, selezionare **Crea**. 

![Form creazione SKYBOX](images/custom-skyboxes-img-03.png)

3. Facoltativamente, è possibile caricare un'immagine di **Anteprima** per poter identificare facilmente questo skybox. È anche possibile caricare audio di ambiente in formato WAV. 

> [!IMPORTANT]
> Quando si carica l'immagine 360, è consigliabile caricare separatamente immagini di anteprima e audio di ambiente. Se vengono caricati insieme, le dimensioni dei file possono essere sufficientemente grandi per bloccare il processo. [Pronipoti World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) è un ottimo esempio di come usare un Skybox con audio ambiente. Si noti che il generatore mondiale ha mantenuto il volume audio basso e che i suoni che si sentono sono sporadici in modo che gli utenti non siano annoiati. 

4. Entra nel mondo e Apri l'editor mondiale. In SKYBOX selezionare il nuovo skybox. In pochi secondi, il cielo cambierà letteralmente. Gli altri utenti del mondo vedranno anche il cambiamento in cielo. Per tornare indietro, scegliere il SKYBOX **predefinito** nello stesso elenco. 

## <a name="troubleshooting"></a>Risoluzione dei problemi

**C'è una linea di giunzione o una linea nella:-(cielo.** Si tratta di un bug che verrà risolto a breve

**Caricamento non riuscito**
    * provare a caricare solo l'immagine 360 autonomamente
    * provare con un altro file più piccolo come test

**Non è possibile trovare una foto di 360**
    * Flickr è una fonte ideale (modificare i filtri per trovare i Commons creativi)
    * Prendi la tua! Abbiamo avuto successo con le fotocamere di Ricoh. 
**Il cielo sembra granulare o bloccare** Potrebbe essere necessario trovare un'immagine a risoluzione superiore. In genere circa 2-5 MB e ~ 5000 px x 2000 px

**Il framerate del mondo è danneggiato.**
L'immagine è probabilmente troppo grande. Alcuni SKYBOX generati possono essere di 8 KB. Sono in genere dotati di versioni di 2K compatibili con dispositivi mobili.

**Supporto per l'audio di ambiente**
    * USA software gratuito come Audacity per abbassare il volume o creare cicli personalizzati. Tenere presente che l'audio verrà ripetuto e riprodotto negli orecchi degli utenti, per mantenerlo insufficiente e non fastidioso
    * Il [suono gratuito](https://freesound.org/) è un'ottima fonte di suoni Royalty-Free
