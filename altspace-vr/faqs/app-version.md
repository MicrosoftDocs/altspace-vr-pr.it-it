---
title: Ricerca della versione dell'app AltspaceVR
description: Informazioni su come usare l'app, le impostazioni e i log client di AltspaceVR per trovare la versione di AltspaceVR attualmente in esecuzione.
ms.date: 02/10/2021
ms.topic: article
keywords: versione app
ms.openlocfilehash: 5d503d3b89cd213696dd53616c5c7e3013aeef01
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213181"
---
# <a name="finding-the-altspacevr-app-version"></a>Ricerca della versione dell'app AltspaceVR

Nel corso della risoluzione di un problema, è possibile che venga richiesta la versione dell'app AltspaceVR attualmente in esecuzione.

## <a name="in-altspacevr"></a>In AltspaceVR

Per trovare la versione dell'app in AltspaceVR, passare al **menu Settings (impostazioni** ) e selezionare **About (informazioni** ) nella barra di spostamento a sinistra. La versione dell'app è riportata qui, come illustrato nella schermata seguente.

![Menu impostazioni aperto con informazioni sul pannello Apri](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a>In impostazioni di sistema Windows

Se è stato installato AltspaceVR tramite il Microsoft Store, è anche possibile trovare la versione dell'app nelle impostazioni di sistema di Windows.  Questo scenario è adatto quando si segnala la versione dell'app se non si riesce ad accedere al client.

Per trovare la versione dell'app nelle impostazioni di sistema di Windows, aprire il **menu Start**, digitare **app & funzionalità** e selezionare il risultato. Passare a **AltspaceVR** nell'elenco delle app. Fare clic con il pulsante destro del mouse su AltspaceVR e scegliere **Opzioni avanzate** dal menu visualizzato.

![Menu app e funzionalità aperto con l'opzione avanzate evidenziata](images/app-version-img-02.png)

Nelle **Opzioni avanzate**, sotto l'intestazione **specifiche** , la **versione dell'app** deve essere elencata a destra dell'etichetta **versione** .

![Opzioni avanzate aperte con la versione dell'app evidenziata](images/app-version-img-03.png)

## <a name="in-client-logs"></a>Nei log del client

AltspaceVR segnala la versione dell'app nel file di log del client come "versione Altspace" durante l'avvio dell'applicazione. Si tratta di un'opzione valida per ottenere la versione dell'app se non è possibile accedere al client, ma si è tentato di avviare prima di avere esito negativo.

## <a name="windows"></a>Windows

In Windows è possibile trovare il file di log del client tramite Esplora risorse all'indirizzo:

```
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player.log
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player-prev.log
```

Questo file viene sovrascritto ogni volta che si avvia AltspaceVR. ' Player. log ' rappresenta la sessione più recente è Player-Prev. log ' rappresenta la sessione precedente.

## <a name="via-powershell"></a>Tramite PowerShell

Gli utenti avanzati possono cercare questa stringa tramite PowerShell nei log del client, come indicato di seguito:

Input:

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

Output:

[2,047] AltspaceVR versione: 3.2.23. e66c2