---
title: Registrazione e streaming live
description: Informazioni su come registrare e trasmettere in streaming gli eventi AltspaceVR dal PC per promuovere e condividere con gli utenti.
author: qianw211
ms.author: v-qianwen
ms.date: 11/1/2021
ms.topic: article
keywords: streaming, registrazione, video, audio, youtube, obs, live
ms.openlocfilehash: e82960097103df25c50f0b03b76d21e10b1cbbd6
ms.sourcegitcommit: 20605c50a93852f93a3464c5c339f6a7da67a047
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/03/2021
ms.locfileid: "131278980"
---
# <a name="recording-and-live-streaming"></a>Registrazione e streaming live

La registrazione e lo streaming live dell'esperienza AltspaceVR per mostrare ad altri utenti in tutto il mondo è un ottimo modo per promuovere l'evento, AltspaceVR e VR in generale. Di seguito viene illustrato come iniziare.

In questo articolo si apprenderà come:

* [Registrare AltspaceVR in modalità 2D nel PC](#recording-altspacevr-in-2d-mode-on-pc)
* [Streaming live su YouTube in AltspaceVR in modalità 2D su PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## <a name="recording-altspacevr-in-2d-mode-on-pc"></a>Registrazione di AltspaceVR in modalità 2D su PC

### <a name="the-short-version"></a>Versione breve

1. Avere altspaceVR e OBS (Open Broadcaster Software) installati. Avviare AltspaceVR in modalità 2D, avviare OBS, impostare OBS per registrare AltspaceVR e registrare via.

### <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

1. Visita [https://obsproject.com/](https://obsproject.com/)
2. Selezionare **Windows** per scaricare OBS. Questo post usa **OBS v26.1.1**
3. Installare OBS

### <a name="have-altspacevr-running-before-you-run-obs"></a>Fare in modo che ALTspaceVR sia in esecuzione PRIMA di eseguire OBS

1. Scaricare e installare AltspaceVR dal sito Web: [altvr.com/get](https://altvr.com/getaltspacevr)
2. Se si desidera stabilizzare il video VR ed eliminare i movimenti della testa a scatti, assicurarsi di usare il client 2D o avviare AltspaceVR in modalità 2D scollegando il cavo USB del visore dal PC. Se si ha un rift, premere CTRL+ALT+CANC, selezionare Servizi **,** **Oculus VR Runtime Service**, fare clic con il pulsante destro del mouse e scegliere **Arresta**. Questo disabilita Oculus e avvia AltspaceVR in modalità 2D. Ripetere questi passaggi e usare Start per tornare alla modalità VR.
3. È anche possibile registrare l'esperienza in modalità VR usando Game Capture con OBS

A questo punto, Alt-Tab a OBS:

1. In **Scene** selezionare **+** e assegnare un nome alla nuova scena
2. Successivamente, in **Origini** selezionare: **+ > Game Capture > Crea nuovo**
2. Modificare il testo in "AltspaceVR Capture", selezionare Rendi visibile **l'origine** e selezionare **OK**
3. Fare doppio clic su **AltspaceVR Capture** in **Origini**
4. Cambia **modalità in** **Acquisisci finestra specifica**
5. Finestra: [AltspaceVR.exe]: AltspaceVR
6. Priorità corrispondenza finestra: trova titolo corrispondente, in caso contrario trova la finestra dello stesso eseguibile
7. Scorrere verso il basso **fino a Acquisisci cursore**: deselezionare
8. Selezionare **OK**.
9. In questo modo AltspaceVR dovrebbe essere visualizzato in OBS.

A questo punto, per impostare le proprietà seguenti in OBS, passare a **File > Impostazioni**:

|Scheda|Impostazioni|
|---|---|
| **Generale** | Lasciare l'impostazione predefinita |
| **Stream** | Lasciare l'impostazione predefinita |
| **Output** | Passare ad Avanzate |
| **- Scheda Streaming** | Traccia audio 1 <br> Codificatore: x264 <br> Ridimensionamento dell'output: non ancorato <br> Controllo della frequenza: CBR <br> Velocità in bit: 6000 (6000 per 30 fps o 9000 per 60 fps) <br> Intervallo fotogrammi chiave = 2 <br> Set di impostazioni di utilizzo CPU = moltoveloce |
| **-Scheda Registrazione** | Tipo: Standard <br> Percorso di registrazione: D:/Video (passare alla posizione in cui si desidera salvare i file video) <br> Formato di registrazione: mp4 (se si verifica un arresto anomalo durante la registrazione, provare flv qui anziché mp4, se si arresta in modo anomalo, il video sarà ancora utilizzabile con flv) <br> Traccia audio 1 <br> Codificatore: usare il codificatore di flusso |
| **-Scheda Audio** | Velocità in bit audio: 160 (per tutte le tracce) |
| **Scheda -Replay buffer** | Lasciare l'impostazione predefinita |
| **Audio** | Frequenza di campionamento: 44.1khz <br> Canali: Stereo <br> Audio desktop: impostazione predefinita <br> Desktop Audio 2: Disabilita <br> Audio Mic/Aux: predefinito |
| **Video** | Risoluzione di base (canvas): 1920x1080 <br> Risoluzione dell'output (ridimensionato): 1920x1080 <br> Filtro di scalabilità orizzontale: Bicubico (ridimensionamento acuto, 16 esempi) <br> Valori FPS comuni: 30 (o 60) |
| **Tasti** | Lasciare l'impostazione predefinita |
| **Funzionalità avanzate** | Priorità processo: Normale | <br>

<br>A questo punto, assicurarsi di selezionare **Applica** e **quindi OK** per salvare tutte le impostazioni di OBS. 

1. Alt-Tab su AltspaceVR, entra nello spazio/mondo/evento corretto e allinea la fotocamera (ovvero il tuo Avatar) che stiamo per registrare un video.
2. Alt-Tab su OBS e quando si è pronti fare clic **su Avvia registrazione**.

Nella parte inferiore destra di OBS si noterà che **REC:** inizierà a contare e il punto è rosso, ovvero si sta registrando.

Eseguire una registrazione di test in base a questa procedura: 
1. In AltspaceVR aprire/chiudere/eseguire il rollover dei menu per creare suoni dell'interfaccia utente
2. Assicurarsi di aver riattivato l'audio, ad esempio "Sibilance, Sibilance" o di ottenere un altro utente per parlare con l'utente a un volume normale.
3. Esaminare i **livelli Desktop Audio (Audio** desktop) e **Mic/Aux (Mic/Aux) mentre** si fa questa operazione per verificare se l'audio viene rilevato correttamente.

Il microfono/Aux viene in genere disattivato durante la registrazione. Procedere e selezionare l'icona del parlante per Mic/Aux e il colore sarà rosso con una X.

* È molto difficile associare i livelli audio del microfono all'audio dell'altro utente, quindi il microfono è più silenziato quando si registra un evento.
* Un altro problema relativo all'audio è la configurazione di OBS. Acquisisce tutto l'audio dal computer, quindi se si guarda YouTube o si ottengono suoni di notifica nel PC, l'audio verrà registrato.
* Per registrare solo l'audio da AltspaceVR, passare al **mixer** Apri volume (fare clic con il pulsante destro del mouse sull'icona Altoparlante in basso a destra di Windows) e disattivare Suoni di sistema, browser e così via, ma non disattivare OBS o AltspaceVR.

> [IMPORTANTE] Non dimenticare di riattivare le impostazioni del mixer volume dopo la registrazione.

A questo punto, tornare a OBS e selezionare **Arresta registrazione**. Per trovare il video appena registrato, passare a **File>Mostra registrazioni**. Verrà aperta la cartella con i file video OBS e fare doppio clic sul video di test.

A volte la registrazione è piuttosto forte, quindi abbassa il dispositivo di scorrimento per Desktop Audio in OBS e crea un'altra registrazione da testare.

Pro suggerimento: usare CTRL+ALT+P per attivare la modalità fotografia, rimuoverà l'interfaccia utente dalla visualizzazione per ottenere un'esecuzione pulita.

Congrats you're an AltspaceVR video recorder!

## <a name="live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc"></a>Streaming live su YouTube in modalità AltspaceVR 2D su PC

### <a name="the-short-version"></a>Versione breve

Avere altspaceVR e OBS installati. Avviare AltspaceVR e OBS. È possibile eseguire lo streaming live 'Right Now' o in una data successiva. Su YouTube configurare OBS con la chiave di YouTube Stream. È possibile iniziare a trasmettere in streaming in OBS e su YouTube.

### <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

Vedere la sezione [Recording AltspaceVR in 2D mode on PC](#recording-altspacevr-in-2d-mode-on-pc) (Registrazione di AltspaceVR in modalità 2D su PC) nella parte superiore di questa pagina per istruzioni su come testare la registrazione usando una registrazione locale anziché lo streaming live e come configurare lo schermo della fotocamera.

## <a name="setting-up-live-streaming-on-youtube"></a>Configurazione dello streaming live su YouTube

È possibile ottenere uno streaming live in corso "Adesso" o configurare uno streaming live futuro con "Data successiva".

1. Aprire il browser, accedere [https://www.youtube.com/](https://www.youtube.com/) e quindi passare a [https://studio.youtube.com/](https://studio.youtube.com/)
2. Cercare in alto a destra e selezionare **CREATE (CREA)** e **quindi Go live (Vai in tempo reale)**

**Metodo 'Right now':**

1. Selezionare **Adesso/AVVIA**
1. Selezionare **Software di streaming/GO**
1. Scegliere **MODIFICA** in alto a destra per modificare i dettagli e le personalizzazioni del video
1. In **Flusso Impostazioni** mantenere le impostazioni predefinite
1. Accanto **a Stream key (Incolla nel codificatore)** copiare la chiave in modo da poterla incollare in OBS 
1. Open OBS/Impostazioni   /  **Stream**
1. Nel menu **a** discesa Service (Servizio) selezionare **YouTube - RTMPS**
1. Incollare la chiave stream da YouTube nel **campo Stream Key (Chiave di** flusso) in OBS
1. Fare **clic su Applica** e quindi su **OK**
1. Selezionare Start Streaming in OBS **(Avvia** streaming in OBS)
1. Passare a YouTube per vedere che ora si è live su YouTube.
1. Per visualizzare la pagina effettiva del video di streaming live di YouTube, è necessario selezionare l'icona CONDIVIDI in alto a destra
1. Fare clic sul collegamento "Video" per visualizzare e ascoltare lo streaming live di YouTube 
1. Questo URL è il collegamento per lo streaming live e può essere condiviso con tutti i canali social :)
1. Per arrestare lo streaming live, selezionare END STREAM su YouTube e quindi Stop Streaming on OBS (Arresta lo streaming in OBS)

Metodo '**Later date**':
1. In alto a sinistra scegliere **l'icona** Gestisci
1. Selezionare **SCHEDULE STREAM (PIANIFICA FLUSSO)** in alto a destra
1. Aggiungere Titolo, Descrizione, Categoria, Anteprima (1280x720), quindi **AVANTI**
1. Opzioni di live chat, quindi **AVANTI**
1. Privato, Non in elenco o Pubblico (scegliere Pubblico)
1. Pianificare la data e l'ora in cui si vuole passare alla pubblicazione, quindi fare clic **su FINE**

 **Quando si è pronti per avviare lo streaming live in futuro:**
1. In Flusso Impostazioni mantenere le impostazioni predefinite
1. Accanto **a Stream key (Incolla nel codificatore)** copiare la chiave in modo da poterla incollare in OBS 
1. Open OBS/Impostazioni   /  **Stream**
* Nel menu **a** discesa Service (Servizio) selezionare **YouTube - RTMPS**
1. Incollare la chiave stream da YouTube nel **campo Stream Key (Chiave di** flusso) in OBS
1. Fare **clic su Applica** e quindi su **OK**
1. Selezionare Start Streaming in OBS **(Avvia** streaming in OBS)
1. Passare a YouTube per vedere che ora si è live su YouTube.
1. Per visualizzare la pagina effettiva del video di streaming live di YouTube, è necessario selezionare l'icona CONDIVIDI in alto a destra
1. Fare clic sul collegamento "Video" per visualizzare e ascoltare lo streaming live di YouTube 
1. Questo URL è il collegamento per lo streaming live e può essere condiviso con tutti i canali social :)
1. Per arrestare lo streaming live, selezionare **END STREAM** su YouTube e quindi Stop Streaming on OBS **(Arresta lo streaming** in OBS)

Per i punti bonus, condividi i video sui social network e assicurati di aggiungere un tag @AltspaceVR :)