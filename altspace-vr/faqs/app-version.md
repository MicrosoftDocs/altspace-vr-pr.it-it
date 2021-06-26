---
title: Ricerca della versione dell'app AltspaceVR
description: Informazioni su come usare l'app AltspaceVR, le impostazioni e i log client per trovare la versione di AltspaceVR attualmente in esecuzione.
ms.date: 02/10/2021
ms.topic: article
keywords: versione dell'app
ms.openlocfilehash: 6b710e1724b890fa7ba0eecfcd774ef63128d5b7
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923178"
---
# <a name="finding-the-altspacevr-app-version"></a>Ricerca della versione dell'app AltspaceVR

Durante la risoluzione di un problema, potrebbe essere richiesta la versione dell'app AltspaceVR attualmente in esecuzione.

## <a name="in-altspacevr"></a>In AltspaceVR

Per trovare la versione dell'app in AltspaceVR, passare al **menu delle impostazioni** e selezionare **Informazioni** su nella barra di spostamento a sinistra. La "versione dell'app" viene segnalata qui, come illustrato nello screenshot seguente.

![Menu Impostazioni aperto con il pannello Informazioni su aperto](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a>In Impostazioni di sistema di Windows

Se AltspaceVR è stato installato tramite il Microsoft Store, è anche possibile trovare la versione dell'app nelle impostazioni di sistema di Windows.  Questo scenario è una buona opzione quando si segnala la versione dell'app se non si riesce ad accedere correttamente al client.

Per trovare la versione dell'app nelle impostazioni di sistema di Windows, aprire il **menu Start,** digitare **App & funzionalità** e selezionare il risultato. Passare ad **AltspaceVR nell'elenco** delle app. Fare clic con il pulsante destro del mouse su ALTspaceVR **e scegliere Opzioni** avanzate dal menu visualizzato.

![Menu App e funzionalità aperto con l'opzione Avanzate evidenziata](images/app-version-img-02.png)

In **Opzioni avanzate,** sotto l'intestazione **Specifiche,** la versione **dell'app** deve essere elencata a destra dell'etichetta **Versione.**

![Opzioni avanzate aperte con la versione dell'app evidenziata](images/app-version-img-03.png)

## <a name="in-client-logs"></a>Nei log del client

AltspaceVR segnala la versione dell'app nel file di log del client come "Altspace Version" durante l'avvio dell'applicazione. Si tratta di un'opzione valida per ottenere la versione dell'app se non è possibile accedere correttamente al client, ma si è tentato di avviarla prima che si verificasse un errore.

## <a name="windows"></a>Windows

In Windows il file di log del client è disponibile Esplora risorse in:

```
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player.log
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player-prev.log
```

Questo file viene sovrascritto ogni volta che si avvia AltspaceVR. 'Player.log' rappresenta la sessione più recente e 'Player-prev.log' rappresenta la sessione precedente.

## <a name="via-powershell"></a>Tramite PowerShell

Gli utenti avanzati possono cercare questa stringa nei log del client tramite PowerShell come indicato di seguito:

Input:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Output:

[2.047] AltspaceVR Versione: 3.2.23.e66c2