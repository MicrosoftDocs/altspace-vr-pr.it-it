---
title: Altri utenti non possono ascoltare l'utente
description: Informazioni su come identificare e risolvere i problemi relativi ad altri utenti che non sono in grado di ascoltare l'utente in AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Domande frequenti
ms.openlocfilehash: 189d96790207085a2a2c47e964c0db8a08ed95a76d91d2ced3026ba3455b45e3
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128093"
---
# <a name="other-users-cant-hear-me"></a>Altri utenti non possono ascoltare l'utente

Prima di tutto, determinare se AltspaceVR sta rilevando l'audio dal microfono. È possibile determinare questo problema esaminando se l'icona del microfono in basso a sinistra nella visualizzazione lampeggia quando si parla. Se l'icona lampeggia quando si parla, il microfono funziona. Se l'icona è rossa, l'audio viene disattivato. Selezionare l'icona per disattivare o riattivare l'audio manualmente.

Se l'icona del microfono non lampeggia dopo la riattivazione, potrebbe essere necessario modificare le impostazioni del microfono in AltspaceVR, passare a Menu/Impostazioni/Audio/Audio Input Selection (Selezione input audio/audio). Usare quindi i pulsanti freccia per selezionare il microfono che si desidera usare.
 
## <a name="oculus-quest"></a>Oculus Quest 

Assicurarsi di concedere le autorizzazioni per usare l'audio del microfono durante l'installazione di AltspaceVR. Un altro controllo che è possibile eseguire è cercare in: Menu /Impostazioni/Audio/Audio Input Selection (Selezione input audio/audio) e verificare che sia impostato su Input audio Android (ovvero il microfono predefinito di Quest/Quest2).
 
## <a name="windows-mixed-reality-oculus-rift-htc-vive-or-2d-mode"></a>Windows Mixed Reality, Oculus Rift, STANDBY Vive o modalità 2D

Assicurarsi di avere le impostazioni corrette del microfono in AltspaceVR: Menu/Impostazioni/Audio/Audio Input Selection (Selezione input audio/audio). Usare quindi i pulsanti freccia per selezionare il microfono che si desidera usare.

Prima di avviare AltspaceVR assicurarsi che il microfono appropriato sia impostato come dispositivo di registrazione predefinito in Windows. Oculus Rift e LASE Vive hanno entrambi un microfono incorporato. Se è presente un altro microfono collegato ad AltspaceVR, è possibile che si stia tentando di usare tale dispositivo.
 
Per modificare il dispositivo di registrazione predefinito in Windows:
* Fare clic con il pulsante destro del mouse sull'icona del parlante Windows e **selezionare Dispositivi di riproduzione**
* Passare alla **scheda Registrazione**
* Trovare il microfono che si desidera usare. Il microfono DI RIFT Vive verrà etichettato con l'etichetta **Microfono -** Dispositivo audio USB e il microfono Oculus Rift con etichetta **Microfono - Rift Audio**.
* Fare clic con il pulsante destro del mouse sul microfono e **scegliere Imposta come dispositivo predefinito**
* Dopo il riavvio di AltspaceVR, il microfono verrà prelevato
 
Se dopo aver seguito questa procedura si verificano ancora problemi, esistono alcuni altri problemi che potrebbero interessare l'utente:
* Se si Alt-Tab per più di 30 secondi, AltspaceVR riattiva automaticamente l'utente, è possibile disabilitarlo usando la scelta rapida da tastiera: barra spaziatrice per attivare/disattivare l'audio.
* Il sistema audio AltspaceVR ha una soglia di volume che potrebbe essere inferiore. Impostare i livelli del microfono su max, impostare il microfono più vicino alla propria voce e parlare al volume normale.
* Uscire dalla realtà virtuale e provare a collegare il cavo USB dal visore VR a una porta USB 3.0 alternativa. In questa esperienza, alcune porte USB 3.0 causano problemi.

AltspaceVR potrebbe non riconoscere le modifiche apportate alle impostazioni audio durante il gioco, quindi potrebbe essere necessario riavviare AltspaceVR delle modifiche apportate al microfono precedente per avere effetto.  Quando si rienta il gioco, osservare l'icona del microfono e verificare se lampeggia. Se l'icona lampeggia, il microfono funziona.