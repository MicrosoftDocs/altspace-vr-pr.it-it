---
title: Domande frequenti sull'audio altspaceVR
description: Risoluzione dei problemi e supporto per i problemi relativi all'audio.
ms.date: 8/23/2021
author: qianw211
ms.author: v-qianwen
ms.topic: article
keywords: vr, audio, risoluzione dei problemi, supporto
ms.openlocfilehash: 05c8a477b9e50b5067e62b934fe2ff8bd656f06c
ms.sourcegitcommit: 5c452a9092297c0bfbc8efabebf395e7ee31853f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/30/2021
ms.locfileid: "129311911"
---
# <a name="frequently-asked-questions-about-audio"></a>Domande frequenti sull'audio

## <a name="does-my-vr-headset-have-a-built-in-mic"></a>Il visore VR ha un microfono incorporato?

### <a name="oculus-riftrift-s-oculus-questquest-2-windows-mixed-reality-and-htc-vive"></a>Oculus Rift/Rift S, Oculus Quest/Quest 2, Windows Mixed Reality and PIÙ Vive

Sì, questi visori VR hanno microfoni predefiniti.

### <a name="windows"></a>Windows

Per i visori VR Windows, dovrebbe essere possibile trovare il  microfono elencato sotto Dispositivi di registrazione mentre il visore VR è collegato.

### <a name="further-troubleshooting"></a>Risoluzione dei problemi

* [Supporto altspaceVR - Altri utenti non possono ascoltare l'utente](#what-do-i-do-if-other-users-cant-hear-me)
* [Supporto di AltspaceVR - Gestione delle autorizzazioni per Oculus Quest](../getting-started/oculus-controls.md#managing-permissions)

## <a name="is-there-a-push-to-talk-button"></a>È presente un pulsante di push per parlare?

Non è presente alcun pulsante di push per parlare.  Se si guarda in basso a sinistra nella visualizzazione, è disponibile un'icona del microfono che può essere usata per attivare o disattivare la voce. In alternativa, è possibile usare la scelta rapida da tastiera Barra spaziatrice per disattivare o disattivare l'audio del microfono.

Se l'icona lampeggia quando si parla, il microfono funziona.
 
## <a name="what-do-i-do-if-my-audio-is-choppy"></a>Cosa si può fare se l'audio è molto azzarto?

Alcuni utenti hanno notato che quando un altro avatar pronuncia l'audio si presenta come un'estrazione o con regolari drop-out. In altri casi si potrebbe essere informati da altri utenti che il proprio audio sta passando attraverso un sistema robotico o di tipo robotico.

La prima cosa da provare è accedere sempre allo spazio in cui ci si trova o persino riavviare AltspaceVR se l'operazione non riesce. I problemi audio non sono comuni, ma quando si verificano spesso si tratta di una soluzione semplice. 

Se l'operazione non riesce, è possibile esaminare gli aspetti seguenti:

#### <a name="cpu-performance-for-desktop-users"></a>Prestazioni della CPU per gli utenti desktop

Esaminare le [specifiche di sistema consigliate per](../getting-started/system-requirements.md) l'hardware consigliato per l'esecuzione di AltspaceVR. È stato rilevato che le CPU i3 o inferiori causano problemi non solo con la frequenza dei fotogrammi del video, ma possono contribuire a problemi audio, ad esempio gli drop out e la qualità scadente.

#### <a name="internet-bandwidth-and-network-connection"></a>Larghezza di banda Internet e connessione di rete

Gli utenti con connessioni Internet lente (inferiori a 5 mbps) o in Wi-Fi possono avere problemi audio, ad esempio gli drop-out. È consigliabile una connessione fissa di un cavo Ethernet al computer e una connessione più veloce di 5 mbps. È possibile uscire da tutti i programmi che potrebbero usare la connettività Internet in background.

## <a name="what-do-i-do-if-other-users-cant-hear-me"></a>Cosa fare se altri utenti non sono in grado di ascoltare?

Prima di tutto, determinare se AltspaceVR sta rilevando l'audio dal microfono. È possibile determinare questo problema esaminando se l'icona del microfono in basso a sinistra nella visualizzazione lampeggia quando si parla. Se l'icona lampeggia quando si parla, il microfono funziona. Se l'icona è rossa, l'audio viene disattivato. Selezionare l'icona per disattivare o riattivare l'audio manualmente.

Se l'icona del microfono non lampeggia dopo la riattivazione, potrebbe essere necessario modificare le impostazioni del microfono in AltspaceVR, passare a Menu/Impostazioni/Audio/Audio Input Selection (Selezione input audio/audio). Usare quindi i pulsanti freccia per selezionare il microfono che si desidera usare.
 
### <a name="oculus-questquest-2"></a>Oculus Quest/Quest 2

Assicurarsi di concedere le autorizzazioni per usare l'audio del microfono durante l'installazione di AltspaceVR. Un altro controllo che è possibile eseguire è cercare in: Menu /Impostazioni/Audio/Audio Input Selection (Selezione input audio/audio) e verificare che sia impostato su Input audio Android, ovvero il microfono predefinito di Quest/Quest2.
 
### <a name="windows-mixed-reality-oculus-riftrift-s-htc-vive-or-2d-mode"></a>Windows Mixed Reality, Oculus Rift/Rift S, STANDBY Vive o modalità 2D

Assicurarsi di avere le impostazioni corrette del microfono in AltspaceVR: Menu/Impostazioni/Audio/Audio Input Selection (Selezione input audio/audio). Usare quindi i pulsanti freccia per selezionare il microfono che si desidera usare.

Prima di avviare AltspaceVR assicurarsi che il microfono appropriato sia impostato come dispositivo di registrazione predefinito in Windows. Oculus Rift/Rift S eNEW Vive hanno entrambi un microfono incorporato. Se è presente un altro microfono collegato ad AltspaceVR, è possibile che si stia tentando di usare tale dispositivo.
 
Per modificare il dispositivo di registrazione predefinito in Windows:

* Fare clic con il pulsante destro del mouse sull'icona del parlante Windows e **selezionare Open Sound settings (Apri impostazioni audio).**
* Passare **all'elenco a discesa Input/Scegliere il dispositivo di input.**
* Scegliere il microfono che si desidera usare dal menu a discesa: 
    * Il microfono DELL'EVA Sarà etichettato **Come Microfono - Dispositivo audio USB**.
    * Il microfono Oculus Rift verrà etichettato come **Microfono visore VR (dispositivo audio virtuale Oculus).**
* Dopo il riavvio di AltspaceVR, il microfono verrà prelevato
 
Se dopo aver seguito questa procedura si verificano ancora problemi, è possibile che si siano verificati problemi:

* Se si Alt-Tab per più di 30 secondi, AltspaceVR disattiva automaticamente l'audio. È possibile disabilitare questa opzione in **Menu -> Impostazioni -> Audio -> Disattiva quando AltspaceVR è inattivo.**
* Il sistema audio AltspaceVR ha una soglia di volume che potrebbe essere inferiore. Impostare i livelli del microfono su max, impostare il microfono più vicino alla propria voce e parlare al volume normale.
* Uscire dalla realtà virtuale e provare a collegare il cavo USB dal visore VR a una porta USB 3.0 alternativa. In questa esperienza, alcune porte USB 3.0 causano problemi.

AltspaceVR potrebbe non riconoscere le modifiche apportate alle impostazioni audio durante il gioco, quindi potrebbe essere necessario riavviare AltspaceVR per avere effetto sulle modifiche apportate al microfono precedente.  Quando si immette nuovamente il gioco, osservare l'icona del microfono e verificare se lampeggia quando si parla. Se l'icona lampeggia, il microfono funziona.

## <a name="support"></a>Supporto

Domande o commenti e suggerimenti per il team altspaceVR? 

> [!div class="nextstepaction"]
> [Fare clic qui per inviare una richiesta di supporto](https://help.altvr.com/hc/requests/new)