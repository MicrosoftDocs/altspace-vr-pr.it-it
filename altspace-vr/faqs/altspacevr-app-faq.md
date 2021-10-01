---
title: Domande frequenti sull'app AltspaceVR
description: Risoluzione dei problemi e supporto per l'app AltspaceVR.
ms.date: 8/16/2021
author: qianw211
ms.author: v-qianwen
ms.topic: article
keywords: vr, AltspaceVR, risoluzione dei problemi, supporto
ms.openlocfilehash: a0df1e100ef8511fe3c9129548529577964c2336
ms.sourcegitcommit: 5c452a9092297c0bfbc8efabebf395e7ee31853f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/30/2021
ms.locfileid: "129311896"
---
# <a name="frequently-asked-questions-about-the-altspacevr-app"></a>Domande frequenti sull'app AltspaceVR

## <a name="finding-the-altspacevr-app-version"></a>Ricerca della versione dell'app AltspaceVR

Durante la risoluzione di un problema, potrebbe essere richiesta la versione dell'app AltspaceVR attualmente in esecuzione.

### <a name="in-altspacevr"></a>In AltspaceVR

Per trovare la versione dell'app in AltspaceVR, passare al **menu delle impostazioni** e selezionare **Informazioni** su sulla barra di spostamento a sinistra. La "Versione dell'app" viene segnalata qui, come illustrato nello screenshot seguente.

![Impostazioni menu aperto con il pannello Informazioni su aperto](images/app-version-img-01.png)

### <a name="in-windows-system-settings"></a>In Windows sistema Impostazioni

Se AltspaceVR è stato installato tramite il Microsoft Store, è anche possibile trovare la versione dell'app nelle impostazioni Windows di sistema.  Questo scenario è una buona opzione quando si segnala la versione dell'app se non è possibile accedere correttamente al client.

Per trovare la versione dell'app Windows di sistema, aprire il **menu Start,** digitare **App & Funzionalità** e selezionare il risultato. Passare ad **AltspaceVR nell'elenco** delle app. Fare clic con il pulsante destro del mouse su AltspaceVR e **scegliere Opzioni** avanzate dal menu visualizzato.

![Il menu App e funzionalità viene aperto con l'opzione avanzata evidenziata](images/app-version-img-02.png)

In **Opzioni avanzate,** sotto l'intestazione **Specifiche,** la versione **dell'app** deve essere elencata a destra dell'etichetta **Versione.**

![Opzioni avanzate aperte con la versione dell'app evidenziata](images/app-version-img-03.png)

### <a name="app-version-in-client-logs"></a>Versione dell'app nei log client

AltspaceVR segnala la versione dell'app nel file di log del client come "Altspace Version" durante l'avvio dell'applicazione. Si tratta di un'opzione valida per ottenere la versione dell'app se non è possibile accedere correttamente al client, ma si è tentato di avviarla prima che si verificasse un errore.

### <a name="windows"></a>Windows

In Windows, il file di log client è disponibile Windows Explorer all'indirizzo:

```
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player.log
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player-prev.log
```

Questo file viene sovrascritto ogni volta che si avvia AltspaceVR. 'Player.log' rappresenta la sessione più recente e 'Player-prev.log' rappresenta la sessione precedente.

### <a name="via-powershell"></a>Tramite PowerShell

Gli utenti avanzati possono cercare questa stringa nei log client tramite PowerShell come indicato di seguito:

Input:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Output:

[2.047] AltspaceVR Versione: 3.2.23.e66c2

## <a name="how-do-i-upload-my-client-logs"></a>Ricerca per categorie i log client?

L'applicazione client AltspaceVR mantiene un log di dati di diagnostica ed eventi che si verificano durante l'uso di AltspaceVR. Durante la risoluzione di un problema, potrebbe essere richiesto di "caricare i log" in modo che il team possa esaminarli. Si tratta di una funzionalità di AltspaceVR che consente di inviare al team il contenuto del log locale per risolvere il problema.

### <a name="in-altspacevr"></a>In AltspaceVR

Per caricare i log client in AltspaceVR, passare al **menu delle impostazioni** e selezionare **Supporto** nella barra di spostamento a sinistra. Qui sono disponibili diverse opzioni per caricare i log, come illustrato nello screenshot seguente.

![Impostazioni menu con il pannello di supporto aperto e i campi di log evidenziati](images/help-altvr-uploadlogs.png)

### <a name="fields"></a>Campi

**"What Went Wrong?"**
Descrivere ciò che è successo: ad esempio, se si trova un bug, descrivere ciò che si prevedeva accadesse a differenza di quanto effettivamente accaduto. Queste informazioni verranno inviate insieme al log quando si preme carica.

**"Upload log"** Questo pulsante carica i log dalla sessione corrente. Usare questa opzione se si trova un problema nella stessa sessione (ad esempio, se non è stato chiuso il client AltspaceVR) e si vuole segnalarlo.

**"Upload ultimi log"** Questo pulsante carica i log dalla sessione precedente.

**"Upload ultimo log di arresto anomalo"** Questo pulsante carica altri contenuti di log dall'arresto anomalo più recente riscontrato.

### <a name="in-client-logs"></a>Nei log del client

È anche possibile recuperare i file di log dal computer. Le istruzioni su come recuperare questi log sono disponibili [qui.](#app-version-in-client-logs)


Dopo aver individuato questi file, aprire un [ticket di supporto](https://help.altvr.com/hc/en-us/requests/new) e caricare i log nella richiesta di ticket prima di fare clic su Invia.

## <a name="what-do-i-do-if-i-cant-launch-altspacevr"></a>Cosa fare se non è possibile avviare AltspaceVR

Esistono diversi motivi per cui AltspaceVR potrebbe non essere avviato per l'utente. Provare i passaggi seguenti per assicurarsi che l'applicazione sia installata correttamente con il software di terze parti necessario.

### <a name="if-youre-trying-to-launch-altspacevr-for-the-first-time"></a>Se si sta tentando di avviare AltspaceVR per la prima volta:

1. Verificare che il dispositivo sia supportato e soddisfi i [requisiti minimi specificati.](../getting-started/system-requirements.md)
2. Assicurarsi di avere installato la versione più recente di [Oculus Software](https://www.oculus.com/setup) e che Impostazioni-> General-> Unknown Devices sia impostato su ON. Se si avvia in modalità 2D, Oculus non è necessario installato.
3. Assicurarsi di avere una connessione Internet funzionante. Se si sta tentando di avviare Altspace dall'interno di un firewall di rete, aprire le porte UDP 5055 e 5056 e le porte TCP 80 e 443. Se si è all'interno della rete di un firewall aziendale o didattico, potrebbe essere necessario contattare l'amministratore di rete o il reparto IT.
4. Vedere anche la pagina relativa alla
    * [Installazione di AltspaceVR per Oculus Quest](../getting-started/oculus-installation.md)
    * [Installazione di AltspaceVR per Windows Mixed Reality](../getting-started/wmr-installation.md)

### <a name="if-altspacevr-reports-that-the-current-version-is-out-of-date"></a>Se AltspaceVR segnala che la versione corrente non è aggiornata:

* La versione dell'applicazione in uso non è più supportata. Se AltspaceVR è stato scaricato tramite una vetrina, l'aggiornamento potrebbe essere stato avviato di recente prima che il negozio fosse in grado di aggiornare il client.
* Se si vuole forzare l'aggiornamento, è possibile farlo tramite le varie vetrine:
    * **Microsoft Store:** [Microsoft Store supporto tecnico - Ottenere aggiornamenti per app](https://support.microsoft.com/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f) e giochi in Microsoft Store
    * **Oculus:** Aprire oculus Library e passare a "Updates" (Aggiornamenti) nella barra di spostamento a sinistra.
    * **Problemi di installazione** [dell'& di Steam: Supporto di Steam](https://support.steampowered.com/kb_article.php?ref=2274-IFLV-5334)

### <a name="if-the-program-was-working-but-ceased-to-launch-after-update"></a>Se il programma funzionava, ma ha smesso di essere avviato dopo l'aggiornamento:

* Eseguire una "reinstallazione pulita" del software. A questo scopo è necessario disinstallare o rimuovere le versioni esistenti dell'applicazione. Dopo la rimozione completa dal sistema, installare Altspace tramite Steam, Oculus o Microsoft Store.
* Se si verifica un problema durante l'avvio di AltspaceVR, è possibile contattarci tramite un [ticket di supporto.](https://help.altvr.com/hc/requests/new) Includere un [file di log](altspacevr-app-faq.md#how-do-i-upload-my-client-logs) dalla sessione.

### <a name="if-altspacevr-fails-to-launch-after-customizing-your-home-space"></a>Se AltspaceVR non viene avviato dopo la personalizzazione dello spazio iniziale:

* Passare al sito [Web dello spazio principale.](https://account.altvr.com/users/sign_in)
* Verificare che il modello del mondo esista ancora. Se il modello è stato condiviso con l'utente, potrebbe essere stato eliminato dal proprietario, causando un errore di caricamento dello spazio di casa.
    * Se il modello è stato eliminato, è sufficiente "Modificare" il mondo nel pannello "World Tools" a sinistra, sostituire il modello esistente con un altro modello e "Update" per salvare le modifiche.
* Rimuovere tutti gli oggetti che potrebbero non essere caricati selezionando "Oggetti" nel pannello "World Tools" a sinistra. Gli oggetti problematici possono includere:
    * Oggetti da kit eliminati o oggetti eliminati dai kit, che sono ancora presenti nel mondo.
    * GLTF sperimentali.
* Dopo aver indirizzato gli elementi precedenti, provare a eseguire di nuovo AltspaceVR.

Il supporto più avanzato per gli amministratori di rete o i reparti IT, inclusi gli intervalli IP di Azure e i tag di servizio, è disponibile nei dettagli [del download.](https://www.microsoft.com/en-us/download/details.aspx?id=56519)

## <a name="support"></a>Supporto

Domande o commenti e suggerimenti per il team altspaceVR? 

> [!div class="nextstepaction"]
> [Fare clic qui per inviare una richiesta di supporto](https://help.altvr.com/hc/requests/new)