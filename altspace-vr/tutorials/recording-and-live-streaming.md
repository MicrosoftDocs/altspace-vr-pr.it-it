---
title: Registrazione e streaming live
description: Informazioni su come registrare ed eseguire lo streaming live degli eventi altspaceVR dal PC per promuovere e condividere con gli utenti.
ms.date: 04/26/2021
ms.topic: article
keywords: streaming, registrazione, video, audio, youtube, obs
ms.openlocfilehash: 95a742cb2bfe5c277e698175bd9f657fcac5923d181c3eeb6905004d25f81aa6
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126108"
---
# <a name="recording-and-live-streaming"></a>Registrazione e streaming live

La registrazione e lo streaming live dell'esperienza AltspaceVR per mostrare ad altri utenti in tutto il mondo sono un ottimo modo per promuovere l'evento, AltspaceVR e la realtà virtuale in generale. Di seguito viene illustrato come iniziare:

In questo articolo si apprenderà come:

* [Registrare AltspaceVR in modalità 2D nel PC](#recording-altspacevr-in-2d-mode-on-pc)
* [Streaming live su YouTube in AltspaceVR in modalità 2D su PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## <a name="recording-altspacevr-in-2d-mode-on-pc"></a>Registrazione di AltspaceVR in modalità 2D nel PC

### <a name="the-short-version"></a>Versione breve

1. Avere altspaceVR e OBS installati. Avviare AltspaceVR in modalità 2D, avviare OBS, impostare OBS per registrare AltspaceVR e registrare.

### <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

1. visita [https://obsproject.com/](https://obsproject.com/)
2. Selezionare **Windows** per scaricare OBS. Questo post usa **OBS v22.0.2**
3. Installare OBS

### <a name="have-altspacevr-running-in-2d-mode-before-you-run-obs"></a>Fare in modo che AltspaceVR sia in esecuzione in modalità 2D PRIMA di eseguire OBS

1. Scaricare e installare AltspaceVR dal sito Web: [altvr.com/get](https://altvr.com/getaltspacevr)
2. Assicurarsi di avviare AltspaceVR in modalità 2D scollegando il cavo USB del dispositivo HMD dal PC o se si dispone di una barra spaziata: CTRL+ALT+CANC, Servizi, Servizio di runtime oculus VR, clic con il pulsante destro del mouse, Arresta. 
    * In questo modo Si disabilita Oculus e si avvia AltspaceVR in modalità 2D, si ripeteranno questi passaggi e si userà Start per tornare alla modalità VR.

A questo punto, Alt-Tab a OBS:

1. In Sources (Origini) selezionare **+ > Game Capture > Create New (Crea nuovo)**
2. Modificare il testo in "AltspaceVR Capture", selezionare **Make source visible**(Rendi visibile l'origine) e selezionare OK
3. Fare doppio clic su **AltspaceVR Capture** in Sources (Origini)
4. Modificare **la modalità** in **Acquisisci finestra specifica**
5. Finestra: [AltspaceVR.exe]: AltspaceVR
6. Priorità di corrispondenza della finestra: trova titolo, altrimenti trova la finestra dello stesso eseguibile
7. Scorrere verso il basso fino a Acquisisci cursore: untick
8. Selezionare OK.

In questo modo AltspaceVR dovrebbe essere visualizzato in OBS. A questo punto, per impostare le proprietà seguenti in OBS, passare a **File > Impostazioni**:

|Scheda|Impostazioni|
|---|---|
| **Generale** | Lasciare l'impostazione predefinita |
| **Stream** | Lasciare l'impostazione predefinita |
| Modalità output | Passare ad Avanzate |
| Scheda Streaming | Traccia audio 1 <br> Codificatore: x264 <br> Rescale Output: unticked <br> Controllo della frequenza: CBR <br> Velocità in bit: 6000 (6000 per 30 fps o 9000 per 60 fps) <br> Intervallo fotogrammi chiave = 2 <br> Cpu Usage Preset = veryfast |
| Scheda Registrazione | Tipo: Standard <br> Percorso di registrazione: D:/Video (passare alla posizione in cui si desidera salvare il file video) <br> Formato di registrazione: mp4 (se si verifica un arresto anomalo durante la registrazione, provare flv qui anziché mp4, se si arresta in modo anomalo il video sarà ancora utilizzabile con flv) <br> Traccia audio 1 <br> Codificatore: usare il codificatore di flusso |
| Scheda Audio | Velocità in bit audio: 160 (per tutte le tracce) |
| Scheda Buffer di riproduzione | Lasciare l'impostazione predefinita |
| **Audio** | Frequenza di campionamento: 48 kZ <br> Canali: Stereo <br> Dispositivo audio desktop: predefinito <br> Dispositivo audio desktop 2: Disabilita <br> Dispositivo audio Mic/Aux: predefinito |
| **Video** | Risoluzione di base (canvas): 1920x1080 <br> Risoluzione dell'output (con scalabilità): 1920x1080 <br> Filtro di scalabilità orizzontale: Bicubico (ridimensionamento acuto, 16 campioni) <br> Valori FPS comuni: 30 |
| **Tasti** | Lasciare l'impostazione predefinita |
| **Funzionalità avanzate** | Priorità processo: Normale | <br>

<br>A questo punto assicurarsi di selezionare **Applica** e quindi **OK** per salvare tutte le impostazioni di OBS. 

1. Alt-Tab su AltspaceVR, entra nello spazio/mondo/evento corretto e allinea la fotocamera (ovvero, il tuo Avatar) che stiamo per registrare un video.
2. Alt-Tab su OBS e quando si è pronti fare clic su **Avvia registrazione.**

Nella parte inferiore destra di OBS si noterà che REC: inizierà a contare e il punto è rosso, ovvero si sta registrando.

Eseguire una registrazione di test da: 
1. In AltspaceVR aprire/chiudere/eseguire il rollover dei menu per creare suoni dell'interfaccia utente
2. Assicurarsi di aver riattivato il audio, ad esempio "Sibilance, Sibilance" o di far parlare un altro utente a un volume normale.
3. Esaminare i livelli Audio desktop e Mic/Aux come si fa per verificare se funziona.

Il microfono/Aux viene in genere disattivato durante la registrazione. Procedere e selezionare l'icona dell'altoparlante per Mic/Aux, che verrà visualizzata in rosso con una X.

* È molto difficile associare l'audio e l'audio dell'altro utente in modo che il microfono sia disattivato al meglio quando si registra un evento.
* Un altro problema relativo all'audio è la configurazione di OBS. Acquisisce tutto l'audio dal computer, quindi se si sta guardando YouTube sul PC, verrà registrato l'audio o le notifiche discord.
* Per registrare solo l'audio da AltspaceVR, passare a Volume Mixer (fare clic con il pulsante destro del mouse sull'icona Voce nella parte inferiore destra di Windows) e disattivare i suoni del sistema, i browser e così via, ma non disattivare OBS o AltspaceVR.

> [!IMPORTANT]
> Non dimenticare di riattivare queste impostazioni di Mixer volume dopo la registrazione.

Tornare a OBS e selezionare **Stop Recording** from File (Arresta registrazione da **file)>Show Recordings (Mostra registrazioni).** Verrà aperta la cartella con i file video OBS e fare doppio clic sul video di test.

A volte la registrazione è piuttosto alta, quindi ridurre il dispositivo di scorrimento per Audio desktop ed eseguire un'altra registrazione da testare.


## <a name="live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc"></a>Streaming live su YouTube in modalità AltspaceVR 2D su PC

### <a name="the-short-version"></a>Versione breve

Avere altspaceVR e OBS installati. Avvia AltspaceVR in modalità 2D, avvia OBS, streaming live o crea un nuovo evento live su YouTube, configura OBS con la chiave di streaming di YouTube, avvia lo streaming in OBS, inizia lo streaming su YouTube e sei in corsa.

### <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

1. visita [https://obsproject.com/](https://obsproject.com/)
2. Selezionare **Windows** scaricare OBS (questo post usa OBS v22.0.2)
3. Installare OBS

Fare in modo che AltspaceVR sia in esecuzione in modalità 2D PRIMA di eseguire OBS
1. Scaricare AltspaceVR dal sito Web: [https://account.altvr.com/downloads](https://account.altvr.com/downloads)
2. Per assicurarsi di avviare AltspaceVR in modalità 2D, scollegare il cavo USB del dispositivo HMD dal PC o se si dispone di un dispositivo Rift: CTRL+ALT+CANC, Servizi, Oculus VR Runtime Service, fare clic con il pulsante destro del mouse su Arresta. Questo disabilita Oculus Home e avvia AltspaceVR in modalità 2D, ripeti questi passaggi e inizia a ottenere di nuovo la modalità VR.

3. Alt-Tab su OBS

4. In Origini selezionare , Selezionare Game Capture, Crea nuovo, Modifica testo **+** in 'AltspaceVR Capture', selezionare Rendi visibile l'origine, OK
5. Fare doppio clic su AltspaceVR Capture
6. Modalità: acquisisci una finestra specifica
7. Finestra: [AltspaceVR.exe]: AltspaceVR
8. Priorità corrispondenza finestra: trova titolo corrispondente, in caso contrario trova la finestra dello stesso file eseguibile
9. Scorrere verso il basso fino a Acquisisci cursore: deselezionare OK

In questo modo AltspaceVR dovrebbe essere visualizzato in OBS. Ottimo.

Ora in OBS passa a File>Impostazioni:

| Scheda | Impostazioni |
|---|---|
| Generale | Selezionare Registra automaticamente durante lo streaming (registra un file video nel computer in aggiunta allo streaming live) |
| Stream | Tipo di flusso: Servizi di streaming <br> Servizio: YouTube/YouTube Gaming (può anche trasmettere in streaming a Contrazione, Mixer, Facebook Live e così via)<br>Server: server di inserimento youtube primario <br>Chiave di streaming: incollare la chiave di streaming da YouTube*** (vedere "Configurazione dello streaming live su YouTube" più avanti) |
| Output | Modalità di output: passare ad Avanzate |
| Streaming | Traccia audio 1 <br>Codificatore: x264 <br>Applicare le impostazioni del codificatore del servizio di streaming: tick <br>Ridimensionamento dell'output: non ancorato <br>Controllo della frequenza: CBR <br>Velocità in bit: 6000 (6000 per 30 fps o 9000 per 60 fps) <br>Intervallo fotogrammi chiave = 2 <br>Set di impostazioni di utilizzo CPU = moltofast |
| Registrazione | Tipo: Standard <br>Percorso di registrazione: D:/Video (passare alla posizione in cui si desidera salvare il file video se è stata selezionata l'opzione "Registra automaticamente durante lo streaming" in precedenza) <br>Formato di registrazione: mp4 (se si verifica un arresto anomalo durante la registrazione, provare flv qui anziché mp4, se si arresta il video sarà ancora utilizzabile con flv) <br>Traccia audio 1 <br>Codificatore: usare il codificatore di flusso |
| Audio | Velocità in bit audio: 160 (per tutte le tracce) Frequenza di campionamento: 48khz <br>Canali: Stereo <br>Dispositivo audio desktop: predefinito <br>Dispositivo audio desktop 2: Disabilita <br>Dispositivo audio Mic/Aux: predefinito |
| Buffer di riproduzione | Lasciare l'impostazione predefinita |
| Video | Risoluzione di base (canvas): 1920x1080 <br>Risoluzione dell'output (ridimensionato): 1920x1080 <br>Filtro di scalabilità orizzontale: Bicubico (ridimensionamento acuto, 16 esempi) <br>Valori FPS comuni: 30 |
| Tasti | Lasciare l'impostazione predefinita |
| Avanzato | Priorità processo: Normale |
|||

<br>A questo punto, assicurarsi di fare clic su Applica, quindi su OK, quindi chiudere e riaprire OBS. In questo modo verranno salvate tutte le impostazioni di OBS. Ricerca di :)

Vedere la sezione precedente "Come registrare AltspaceVR in modalità 2D su PC" per istruzioni su come testare la registrazione usando una registrazione locale anziché il flusso live e come ottenere la configurazione della fotocamera prima della registrazione.

Un altro problema relativo all'audio è la configurazione di OBS. Acquisisce tutto l'audio dal computer, quindi se si guarda YouTube registra l'audio o Teams messaggi o suoni di notifica.

Per registrare solo l'audio da AltspaceVR, passare a Volume Mixer (fare clic con il pulsante destro del mouse sull'icona Altoparlante in basso a destra di Windows) e disattivare Suoni di sistema, Browser e così via, ma non disattivare OBS o AltspaceVR.

Non dimenticare di riattivare l'audio dopo la registrazione ;)

Congrats you're an AltspaceVR video recorder!

## <a name="setting-up-live-streaming-on-youtube"></a>Configurazione dello streaming live su YouTube

È possibile ottenere rapidamente un flusso live in corso (**Stream**) o configurare un evento di flusso live futuro (**Gestione**). È consigliabile configurarlo in modo "Gestisci".

1. Aprire il browser e accedere [https://www.youtube.com/](https://www.youtube.com/) e quindi passare a [https://www.youtube.com/my_live_events](https://www.youtube.com/my_live_events)
2. Selezionare l'icona Account in alto a destra, selezionare Creator Studio nell'elenco a discesa
3. LIVE STREAMING sul lato sinistro della pagina.

Metodo **'Stream now':**

* Selezionare MODIFICA per immettere le informazioni sul flusso live<br>
* In Flusso Impostazioni mantenere le impostazioni predefinite<br>
* Tasto di flusso (incolla nel codificatore), selezionare 'Reveal' e copiare questa chiave in modo da poterla incollare in OBS<br>
* Aprire OBS/Impostazioni/Stream<br>
* Incollare la chiave di flusso da YouTube nel campo Stream Key (Chiave di flusso) in OBS<br>
* Applica, quindi OK<br>
* Selezionare Avvia streaming in OBS<br>
* Passare a YouTube per vedere che ora si è live su YouTube.<br>
* Per visualizzare la pagina video di YouTube live stream effettiva, è necessario selezionare l'icona CONDIVIDI in alto a destra.<br>
* Copiare e incollare il collegamento Video in una nuova scheda del browser. Verrà visualizzata la pagina dello streaming live di YouTube.<br>
* Questo URL è il collegamento al flusso live e può essere condiviso con tutti i canali di social :)<br>
* Per arrestare lo streaming live, selezionare Stop Streaming on OBS (Arresta streaming in OBS) per terminare lo streaming live su YouTube.<br>
* Arrestare quindi lo streaming su YouTube<br>

Metodo '**Manage**':
* Selezionare 'Pianifica flusso'
* Crea nuovo o Riutilizza Impostazioni se è già stato configurato un flusso live gestito precedente
* Aggiungere titolo, data, ora di inizio, descrizione, Upload anteprima e tag: non dimenticare di contrassegnare AltspaceVR :)
* Scegliere Pubblico dal menu a discesa (l'impostazione predefinita è "Non in elenco")
* Valori predefiniti
* Copiare la chiave stream (incollare nel codificatore)
* Per visualizzare la pagina video di YouTube live stream effettiva, è necessario selezionare l'icona CONDIVIDI in alto a destra. Questo è il collegamento all'evento dello streaming live di YouTube, che può essere condiviso su Social way prima dell'evento effettivo.
* Aprire ora OBS
* File/Impostazioni
* Stream
* Incollare la chiave di flusso copiata nel campo Chiave di flusso
* Applica, quindi OK
* Selezionare "Avvia streaming"
* Tornando a YouTube, si vedrà che la finestra "Anteprima" mostra il flusso e GO LIVE è ora acceso in alto a destra.
* Selezionare GO LIVE
* A questo punto si è in tempo reale.
* Passare alla scheda del browser con il collegamento "Visualizza nella pagina espressioni di controllo" aperto per assicurarsi che il video sia stato visualizzato. TENERE presente che l'audio non viene udito perché l'audio è stato disattivato dai browser quando è stato disattivato l'audio in Windows volume Mixer. Controllare l'audio sul telefono o chiedere a un amico di controllare l'audio.
* L'aspetto è positivo.
* Alt-Tab tornare ad AltspaceVR per spostare la fotocamera (ovvero l'Avatar) nell'evento.
* Al termine dello streaming live, tornare alla pagina "Live Control Room" di YouTube
* Selezionare "Arresta streaming"
* Verrà visualizzata la finestra di dialogo in cui viene chiesto se si vuole interrompere lo streaming dell'evento live, OK
* Passare a OBS e selezionare anche Stop Streaming (Arresta streaming).
* Congrats, you're now an AltspaceVR streamer!

Per i punti bonus, condividi i tuoi video con il mondo sui social media e assicurati di aggiungere tag @AltspaceVR :)