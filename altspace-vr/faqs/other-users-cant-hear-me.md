---
title: Altri utenti non possono ascoltarmi
description: Informazioni su come identificare e risolvere i problemi correlati ad altri utenti che non sono in grado di ricevere informazioni in AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Domande frequenti
ms.openlocfilehash: b6248e46b62e1a29324e831e686aee7b1de4505a
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213364"
---
# <a name="other-users-cant-hear-me"></a>Altri utenti non possono ascoltarmi

Per prima cosa, determinare se AltspaceVR sta rilevando l'audio dal microfono. È possibile determinare questo aspetto esaminando se l'icona del microfono in basso a sinistra della visualizzazione lampeggia durante la conversazione. Se l'icona lampeggia quando si parla, il microfono funziona. Se l'icona è rossa, l'utente viene disattivato. Selezionare l'icona per disattivare o demutare manualmente.

Se l'icona del microfono non viene visualizzata in modo lampeggiante dopo la demuting, potrebbe essere necessario modificare le impostazioni del microfono in AltspaceVR, passare a menu/impostazioni/audio/input audio (selezione). Quindi, usando i pulsanti freccia per selezionare il MIC che si vuole usare.
 
## <a name="oculus-quest"></a>Oculus-ricerca 

Assicurarsi di concedere le autorizzazioni per l'uso dell'audio mic durante l'installazione di AltspaceVR. Un altro controllo che è possibile eseguire è: menu/impostazioni/audio/audio input selection (Selezione input audio/audio) e impostazione dell'input audio Android (il MIC predefinito di quest/Quest2's).
 
## <a name="windows-mixed-reality-oculus-rift-htc-vive-or-2d-mode"></a>Realtà mista di Windows, Oculus Rift, HTC vive o modalità 2D

Assicurarsi di avere le impostazioni corrette del microfono in AltspaceVR: menu/impostazioni/audio/input audio selezione. Quindi, usando i pulsanti freccia per selezionare il MIC che si vuole usare.

Prima di avviare AltspaceVR, verificare che il microfono appropriato sia impostato come dispositivo di registrazione predefinito in Windows. Gli Oculus Rift e HTC vive hanno entrambi un microfono integrato. se è presente un altro microfono collegato in AltspaceVR, è possibile che si stia tentando di usare il dispositivo.
 
Per modificare il dispositivo di registrazione predefinito in Windows:
* Fare clic con il pulsante destro del mouse sull'icona dell'altoparlante in Windows e scegliere **riproduzione dispositivi**
* Passare alla scheda **registrazione**
* Trovare il microfono che si vuole usare. Il microfono di HTC vive verrà etichettato come **dispositivo audio microfono-USB** e il microfono Oculus Rift verrà etichettato come **audio di Rift**.
* Fare clic con il pulsante destro del mouse sul microfono e selezionare **Imposta come dispositivo predefinito**
* Dopo il riavvio di AltspaceVR, il microfono verrà ora selezionato
 
Se dopo aver seguito questi passaggi si verificano ancora problemi, è possibile che si verifichino problemi:
* Se si Alt-Tab di distanza per più di 30 secondi, AltspaceVR verrà disabilitato in modo autodisattivato utilizzando il tasto di scelta rapida: barra spaziatrice per attivare/disattivare il silenziamento.
* Il sistema audio AltspaceVR ha una soglia di volume che può essere riportata di seguito. Impostare i livelli mic su Max, impostare il MIC più vicino alla bocca e parlare al volume normale.
* Uscire da VR, provare a collegare il cavo USB dall'auricolare a una porta USB 3,0 alternativa. In questa esperienza alcune porte USB 3,0 generano problemi.

AltspaceVR non è in grado di riconoscere le modifiche delle impostazioni audio effettuate durante il gioco, quindi potrebbe essere necessario riavviare AltspaceVR delle modifiche al microfono sopra indicate per rendere effettive le modifiche.  Quando si riimmette il gioco, esaminare l'icona del microfono per verificare se lampeggia. Se l'icona lampeggia, il microfono funziona.