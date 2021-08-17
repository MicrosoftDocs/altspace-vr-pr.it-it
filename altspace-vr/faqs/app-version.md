---
title: Ricerca della versione dell'app AltspaceVR
description: Informazioni su come usare l'app AltspaceVR, le impostazioni e i log client per trovare la versione di AltspaceVR attualmente in esecuzione.
ms.date: 02/10/2021
ms.topic: article
keywords: versione dell'app
ms.openlocfilehash: fbf67a8302a67ddb916772420949cf0509a0d4a60c472711975c651862438b93
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128253"
---
# <a name="finding-the-altspacevr-app-version"></a>Ricerca della versione dell'app AltspaceVR

Durante la risoluzione di un problema, potrebbe essere richiesta la versione dell'app AltspaceVR attualmente in esecuzione.

## <a name="in-altspacevr"></a>In AltspaceVR

Per trovare la versione dell'app in AltspaceVR, passare al **menu delle impostazioni** e selezionare **Informazioni** su sulla barra di spostamento a sinistra. La "Versione dell'app" viene segnalata qui, come illustrato nello screenshot seguente.

![Impostazioni menu aperto con il pannello Informazioni su aperto](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a>In Windows sistema Impostazioni

Se AltspaceVR è stato installato tramite il Microsoft Store, è anche possibile trovare la versione dell'app nelle Windows di sistema.  Questo scenario è una buona opzione quando si segnala la versione dell'app se non è possibile accedere correttamente al client.

Per trovare la versione dell'app nelle Windows di sistema, aprire il **menu Start,** digitare **App & Funzionalità** e selezionare il risultato. Passare ad **AltspaceVR nell'elenco** delle app. Fare clic con il pulsante destro del mouse su AltspaceVR e **scegliere Opzioni** avanzate dal menu visualizzato.

![Il menu App e funzionalità viene aperto con l'opzione avanzate evidenziata](images/app-version-img-02.png)

In **Opzioni avanzate,** sotto l'intestazione **Specifiche,** la versione **dell'app** deve essere elencata a destra dell'etichetta **Versione.**

![Opzioni avanzate aperte con la versione dell'app evidenziata](images/app-version-img-03.png)

## <a name="in-client-logs"></a>Nei log del client

AltspaceVR segnala la versione dell'app nel file di log del client come "Altspace Version" durante l'avvio dell'applicazione. Si tratta di un'opzione valida per ottenere la versione dell'app se non è possibile accedere correttamente al client, ma si è tentato di avviarla prima che si verificasse un errore.

## <a name="windows"></a>Windows

In Windows, il file di log client è disponibile Windows Explorer all'indirizzo:

```
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player.log
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player-prev.log
```

Questo file viene sovrascritto ogni volta che si avvia AltspaceVR. 'Player.log' rappresenta la sessione più recente e 'Player-prev.log' rappresenta la sessione precedente.

## <a name="via-powershell"></a>Tramite PowerShell

Gli utenti avanzati possono cercare questa stringa nei log client tramite PowerShell come indicato di seguito:

Input:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Output:

[2.047] AltspaceVR Versione: 3.2.23.e66c2