---
title: Registrazione e streaming live
description: Informazioni su come registrare e trasmettere in streaming live gli eventi AltspaceVR dal PC per promuovere e condividere con gli utenti.
ms.date: 02/10/2021
ms.topic: article
keywords: streaming, registrazione
ms.openlocfilehash: 80d54407915af1a0d4b7783858446f54205e6a2a
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213501"
---
# <a name="recording-and-live-streaming"></a>Registrazione e streaming live

Registrare e trasmettere in streaming live l'esperienza AltspaceVR per mostrare ad altri utenti in tutto il mondo è un ottimo modo per promuovere l'evento, AltspaceVR e VR in generale. Per informazioni su come iniziare, vedere:

In questo articolo si apprenderà come:

* [Come registrare AltspaceVR in modalità 2D sul PC](#recording-altspacevr-in-2d-mode-on-pc)
* [Come eseguire lo streaming live in YouTube in AltspaceVR in modalità 2D sul PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## <a name="recording-altspacevr-in-2d-mode-on-pc"></a>Registrazione di AltspaceVR in modalità 2D sul PC

### <a name="the-short-version"></a>Versione breve

Installare AltspaceVR ed OBS. Avviare AltspaceVR in modalità 2D, avviare OBS, impostare OBS per registrare AltspaceVR e registrare i dati.

### <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

1. Visitare [https://obsproject.com/](https://obsproject.com/)
2. Selezionare **Windows** per scaricare OBS. Questo post usa **OBS v 22.0.2**
3. Installare OBS

### <a name="have-altspacevr-running-in-2d-mode-before-you-run-obs"></a>Eseguire AltspaceVR in modalità 2D prima di eseguire OBS

1. Scaricare e installare AltspaceVR dal sito Web: [altvr.com/Get](https://altvr.com/getaltspacevr)
2. Assicurarsi di avviare AltspaceVR in modalità 2D scollegando il cavo USB di HMD dal PC o se è presente una frattura: CTRL + ALT + CANC, servizi, Oculus VR Runtime Service, fare clic con il pulsante destro del mouse su, arrestare. 
    * Questa operazione consente di disabilitare Oculus e avviare AltspaceVR in modalità 2D, ripetere questi passaggi e usare Start per ottenere la modalità VR.

A questo punto, Alt-Tab a OBS:

1. In origini selezionare **+ > Game Capture > Crea nuovo**
2. Modificare il testo in "AltspaceVR Capture", selezionare **Rendi visibile l'origine** e selezionare OK.
3. Fare doppio clic su **AltspaceVR Capture** in origini
4. Modificare la **modalità** per **acquisire una finestra specifica**
5. Finestra: [AltspaceVR.exe]: AltspaceVR
6. Priorità di corrispondenza finestra: titolo della corrispondenza; in caso contrario, trova finestra dello stesso eseguibile
7. Scorri verso il basso fino a Acquisisci cursore: deseleziona OK

Questa operazione dovrebbe far apparire AltspaceVR in OBS. A questo punto, per impostare le proprietà seguenti in OBS, passare a **File > impostazioni**:

| Scheda | Impostazioni |
|---|---|
| Generale | Lasciare l'impostazione predefinita |
| Stream | Lasciare l'impostazione predefinita |
| Modalità di output: passa a avanzate | Scheda streaming <br> Traccia audio 1 <br> Codificatore: x264 <br> Applicare le impostazioni del codificatore del servizio di streaming: seleziona <br> Ridimensionare l'output: non selezionato <br> Controllo della velocità: CBR <br> Velocità in bit: 6000 (6000 per 30 fps o 9000 per 60 fps) <br> Intervallo fotogramma chiave = 2 <br> Set di impostazioni utilizzo CPU = veryfast |
| Registrazione | Tipo: standard <br> Percorso di registrazione: D:/video (passare alla posizione in cui si vuole salvare il file video) <br> Formato di registrazione: MP4 (se si è verificato un arresto anomalo durante la registrazione, provare a usare FLV qui anziché MP4, se si arresta un arresto anomalo, il video sarà comunque utilizzabile con FLV) <br> Traccia audio 1 <br> Codificatore: usare il codificatore di flusso |
| Audio | Velocità in bit audio: 160 (per tutte le tracce) |
| Buffer di riproduzione | Lasciare l'impostazione predefinita |
| Audio | Frequenza di campionamento: 48 kHz <br> Canali: stereo <br> Dispositivo audio desktop: predefinito <br> Dispositivo audio desktop 2: disabilitato <br> Dispositivo audio MIC/AUX: predefinito |
| Video | Risoluzione di base (Canvas): 1920x1080 <br> Risoluzione output (ridimensionata): 1920x1080 <br> Filtro downscaling: bicubico (ridimensionamento affilato, 16 esempi) <br> Valori FPS comuni: 30 |
| Tasti | Lasciare l'impostazione predefinita |
| Avanzato | Priorità processo: normale |

Bene. Assicurarsi di selezionare **applica** e quindi **OK** per salvare tutte le impostazioni di OBS. 

1. Alt-Tab a AltspaceVR, passare allo spazio/mondo/evento corretto e allineare la fotocamera (ovvero, l'avatar) che sta per registrare un video.
2. Alt-Tab a OBS e, quando si è pronti, fare clic su **Avvia registrazione**.

Nella parte inferiore destra di OBS si noterà che REC: inizierà il conteggio, il che significa che si sta registrando.

Eseguire una registrazione del test: 
1. In AltspaceVR aprire/chiudere/eseguire il rollover dei menu per rendere i suoni dell'interfaccia utente
2. Pronunciare "sibilanti, sibilanti" e ottenere un altro utente per comunicare con l'utente in un volume normale o guardare un video sullo schermo 2D.
3. Esaminare i livelli audio e MIC/AUX del desktop mentre si esegue questa operazione per verificarne il funzionamento.

In genere, il MIC/AUX viene disattivato durante la registrazione. Procedere e selezionare l'icona dell'altoparlante per MIC/AUX, che diventerà rossa con una X.

* È molto difficile abbinare l'audio e l'audio dell'altro utente, in modo che il MIC venga disattivato.
* Un altro problema con l'audio è il modo in cui viene configurato OBS. Acquisisce tutti i dati audio dal computer, quindi, se si sta guardando YouTube, registrerà l'audio, i messaggi Slack o i suoni di notifica.
* Per registrare solo l'audio da AltspaceVR, passare a mixer volume (fare clic con il pulsante destro del mouse sull'icona dell'altoparlante nella parte inferiore destra di Windows) e disattivare i suoni di sistema, i browser e così via, ma non disattivare OBS o AltspaceVR.

> [!IMPORTANT]
> Non dimenticare di attivare di nuovo le impostazioni del mixer del volume dopo la registrazione.

A questo punto, tornare a OBS e selezionare **Interrompi registrazione** da **file>Mostra registrazioni**. Verrà visualizzata la cartella con i file video OBS, facendo doppio clic sul video di test.

A volte la registrazione è piuttosto forte, quindi abbassare il dispositivo di scorrimento per l'audio del desktop e fare in modo che venga testata un'altra registrazione.

<!-- Missing image -->

## <a name="live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc"></a>Streaming live su YouTube in modalità 2D AltspaceVR su PC

### <a name="the-short-version"></a>Versione breve

Installare AltspaceVR ed OBS. Avviare AltspaceVR in modalità 2D, avviare OBS, Live Stream o creare un "nuovo evento live" su YouTube, configurare OBS con la chiave di flusso di YouTube, avviare lo streaming in OBS, avviare lo streaming su YouTube e si è pronti per le corse.

### <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

1. Visitare [https://obsproject.com/](https://obsproject.com/)
2. Fare clic su **Windows** per scaricare Obs (questo post USA OBS v 22.0.2)
3. Installare OBS

Eseguire AltspaceVR in modalità 2D prima di eseguire OBS
1. Scaricare AltspaceVR dal sito Web: [https://account.altvr.com/downloads](https://account.altvr.com/downloads)
2. Per assicurarsi di avviare AltspaceVR in modalità 2D, scollegare il cavo USB di HMD dal PC o se è presente una frattura: CTRL + ALT + CANC, servizi, Oculus VR Runtime Service, fare clic con il pulsante destro del mouse su, stop. Questa operazione consente di disabilitare Oculus Home e avviare AltspaceVR in modalità 2D, ripetere questi passaggi e iniziare a ottenere nuovamente la modalità VR.

Alt-Tab a OBS

1. In sources selezionare **+** , Game Capture, create new, Edit Text to ' AltspaceVR Capture ', fare clic su Make source Visible, OK
2. Fare doppio clic su AltspaceVR Capture
3. Modalità: Acquisisci finestra specifica
4. Finestra: [AltspaceVR.exe]: AltspaceVR
5. Priorità di corrispondenza finestra: titolo della corrispondenza; in caso contrario, trova finestra dello stesso eseguibile
6. Scorri verso il basso fino a Acquisisci cursore: deseleziona OK

Questa operazione dovrebbe far apparire AltspaceVR in OBS. Ottimo.

Ora in OBS passa a file>impostazioni

| Scheda | Impostazioni |
|---|---|
| Generale | Seleziona automaticamente registra durante il flusso (questo registra un file video nel computer in aggiunta allo streaming live) |
| Stream | Tipo di flusso: Servizi di streaming <br> Servizio: YouTube/YouTube Gaming (può anche trasmettere a TIC, mixer, Facebook Live e così via)<br>Server: server di inserimento YouTube primario <br>Chiave del flusso: incollare la chiave del flusso da YouTube * * _ (vedere la pagina relativa alla configurazione in tempo reale <br>Streaming su YouTube ' di seguito |
| Output | Modalità di output: passa a avanzate |
| Streaming | Traccia audio 1 <br>Codificatore: x264 <br>casella di selezione applica impostazioni del codificatore del servizio di streaming <br>Ridimensionare l'output: non selezionato <br>Controllo della velocità: CBR <br>Velocità in bit: 6000 (6000 per 30 fps o 9000 per 60 fps) <br>Intervallo fotogramma chiave = 2 <br>Set di impostazioni utilizzo CPU = veryfast |
| Registrazione | Tipo: standard <br>Percorso di registrazione: D:/video (passare alla posizione in cui si desidera salvare il file video se è stata selezionata l'opzione ' registra automaticamente durante il flusso ') <br>Formato di registrazione: MP4 (se si è verificato un arresto anomalo durante la registrazione, provare a usare FLV qui anziché MP4, se si arresta un arresto anomalo, il video sarà comunque utilizzabile con FLV) <br>Traccia audio 1 <br>Codificatore: usare il codificatore di flusso |
| Audio | Velocità in bit audio: 160 (per tutte le tracce) frequenza di campionamento: 48 kHz <br>Canali: stereo <br>Dispositivo audio desktop: predefinito <br>Dispositivo audio desktop 2: disabilitato <br>Dispositivo audio MIC/AUX: predefinito |
| Buffer di riproduzione | Lasciare l'impostazione predefinita |
| Video | Risoluzione di base (Canvas): 1920x1080 <br>Risoluzione output (ridimensionata): 1920x1080 <br>Filtro downscaling: bicubico (ridimensionamento affilato, 16 esempi) <br>Valori FPS comuni: 30 |
| Tasti | Lasciare l'impostazione predefinita |
| Avanzato | Priorità processo: normale |

Bene. ora, assicurarsi di fare clic su Applica, quindi su OK, quindi chiudere e riaprire OBS. Che salverà tutte le impostazioni di OBS. Aspetto positivo:)

Vedere la sezione "come registrare AltspaceVR in modalità 2D nel PC" riportata sopra per istruzioni su come testare la registrazione usando una registrazione locale anziché il flusso live e anche come ottenere la configurazione della fotocamera prima della registrazione.

Un altro problema con l'audio è il modo in cui viene configurato OBS. Acquisisce tutti i dati audio dal computer, quindi, se si sta guardando YouTube, registrerà l'audio, i messaggi dei team o i suoni di notifica.

Per registrare solo l'audio da AltspaceVR, passare a mixer volume (fare clic con il pulsante destro del mouse sull'icona dell'altoparlante nella parte inferiore destra di Windows) e disattivare i suoni di sistema, i browser e così via, ma non disattivare OBS o AltspaceVR.

Non dimenticare di riattivare il backup dopo la registrazione;)

### <a name="setting-up-live-streaming-on-youtube"></a>Impostazione dello streaming live su YouTube

È possibile ottenere rapidamente un flusso Live in corso (STREAMING LIVE) o configurare un evento Live Stream futuro (nuovo evento Live). Suggerisco di impostare il "nuovo evento live".

1. Aprire il browser e accedere [https://www.youtube.com/](https://www.youtube.com/)
2. Selezionare sull'icona dell'account, in alto a destra, selezionare Creator Studio dall'elenco a discesa
3. STREAMING LIVE sul lato sinistro della pagina.

Anteprima di modifica del metodo ' Stream Now ' se è necessario modificare l'impostazione di base del CODIFICAtore, Mantieni URL del server come valore predefinito _ * * nome flusso/chiave, fai clic su' rivela ' e copia questa chiave Apri OBS impostazioni flusso incolla questo nella chiave del flusso applica, quindi OK fare clic su Avvia streaming passa a YouTube e vedrai che sei ora disponibile su YouTube.
Per visualizzare la pagina effettiva del video di YouTube Live Stream, è necessario scorrere verso il basso e cercare il collegamento Condividi in basso a destra.
Copiare e incollare il contenuto in una nuova scheda del browser, quindi fare clic su video. nell'elenco verrà visualizzato il video, che verrà visualizzato in tempo reale, fare clic su di esso per visualizzare la pagina di streaming live di YouTube.
Questo URL è il collegamento Live Stream e può essere condiviso con tutti i canali sociali:) Per arrestare il flusso Live, fare clic su Interrompi streaming su OBS. verrà terminato il flusso live su YouTube.

Metodo ' Events ': https://www.youtube.com/my_live_events fare clic su' nuovo evento Live ' Aggiungi titolo, data, ora di inizio, descrizione e tag-non dimenticare di contrassegnare AltspaceVR:) Scegliere pubblico dal menu a discesa Tipo: personalizzato fare clic su "Crea evento" Se si vuole aggiungere un'anteprima personalizzata fare clic su Sfoglia e caricare l'immagine. (1280x720 funziona meglio) Select: chiave del flusso monouso selezionare il codificatore: altri codificatori copia il nome del flusso (chiave di flusso)

A questo punto, fare clic con il pulsante destro del mouse sulla pagina "Visualizza in controllo" e "Apri collegamento in nuova scheda".

Questo è il collegamento all'evento di streaming live di YouTube, che può essere condiviso in modo socialmente più avanti rispetto all'evento effettivo.

A questo punto, aprire il file OBS>impostazioni flusso incollare la chiave del flusso appena copiata nel campo chiave flusso, quindi fare clic su YouTube,' Salva modifiche ' fare clic con il pulsante destro del mouse su' Live Control Room ' è Apri collegamento in una nuova scheda ' ora torna a OBS per fare clic su' avvia streaming ' di nuovo su YouTube. si noterà che il pulsante "anteprima" è ora blu. fare clic sulla finestra di dialogo pulsante anteprima, in cui viene chiesto se si desidera visualizzare in anteprima l'evento Live, attendere qualche istante. verrà visualizzato il pulsante "avvia streaming", quindi viene visualizzata la finestra di dialogo ' avvia streaming ', in cui viene chiesto se si desidera trasmettere l'evento Live, OK

Sei ora disponibile!

Passare alla scheda del browser con il collegamento ' Visualizza sulla pagina di controllo ' aperta per assicurarsi che il video sia valido. TENERE presente che l'audio non è stato sentito perché è stata disattivata dai browser quando sono stati disattivati in mixer del volume di Windows. Controllare l'audio sul telefono o chiedere a un amico di controllare l'audio.

Aspetto positivo.

Alt-Tab di nuovo a AltspaceVR per spostare la fotocamera (ovvero l'avatar) nell'evento.

Al termine del flusso Live, tornare alla pagina ' Live Control Room ' di YouTube

Fare clic su' Interrompi streaming '

Viene visualizzata la finestra di dialogo in cui viene chiesto se si desidera arrestare lo streaming dell'evento Live, OK

Passare a OBS, quindi fare clic su Interrompi streaming.

Si tratta di un flusso di AltspaceVR.


Recording_AltspaceVR_.png


Per i punti di bonus, Condividi i tuoi video con il mondo sui social media e assicurati di contrassegnarci @AltspaceVR :)