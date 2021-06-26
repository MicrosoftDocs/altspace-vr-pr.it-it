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
# <a name="finding-the-altspacevr-app-version"></a><span data-ttu-id="c179d-104">Ricerca della versione dell'app AltspaceVR</span><span class="sxs-lookup"><span data-stu-id="c179d-104">Finding the AltspaceVR app version</span></span>

<span data-ttu-id="c179d-105">Durante la risoluzione di un problema, potrebbe essere richiesta la versione dell'app AltspaceVR attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c179d-105">In the course of troubleshooting an issue, you may be asked what version of the AltspaceVR app you're currently running.</span></span>

## <a name="in-altspacevr"></a><span data-ttu-id="c179d-106">In AltspaceVR</span><span class="sxs-lookup"><span data-stu-id="c179d-106">In AltspaceVR</span></span>

<span data-ttu-id="c179d-107">Per trovare la versione dell'app in AltspaceVR, passare al **menu delle impostazioni** e selezionare **Informazioni** su nella barra di spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="c179d-107">To find the app version in AltspaceVR, navigate to the **settings menu** and select **About** in the left navigation bar.</span></span> <span data-ttu-id="c179d-108">La "versione dell'app" viene segnalata qui, come illustrato nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="c179d-108">The 'App Version' is reported here, as shown in the screenshot below.</span></span>

![Menu Impostazioni aperto con il pannello Informazioni su aperto](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a><span data-ttu-id="c179d-110">In Impostazioni di sistema di Windows</span><span class="sxs-lookup"><span data-stu-id="c179d-110">In Windows System Settings</span></span>

<span data-ttu-id="c179d-111">Se AltspaceVR è stato installato tramite il Microsoft Store, è anche possibile trovare la versione dell'app nelle impostazioni di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="c179d-111">If you installed AltspaceVR via the Microsoft Store, you can additionally find the app version in the Windows system settings.</span></span>  <span data-ttu-id="c179d-112">Questo scenario è una buona opzione quando si segnala la versione dell'app se non si riesce ad accedere correttamente al client.</span><span class="sxs-lookup"><span data-stu-id="c179d-112">This scenario is a good fit when reporting the app version if you're unable to successfully log into the client.</span></span>

<span data-ttu-id="c179d-113">Per trovare la versione dell'app nelle impostazioni di sistema di Windows, aprire il **menu Start,** digitare **App & funzionalità** e selezionare il risultato.</span><span class="sxs-lookup"><span data-stu-id="c179d-113">To find the app version in Windows system settings, open the **Start Menu**, type in **Apps & Features**, and select the result.</span></span> <span data-ttu-id="c179d-114">Passare ad **AltspaceVR nell'elenco** delle app.</span><span class="sxs-lookup"><span data-stu-id="c179d-114">Navigate to **AltspaceVR** in the list of apps.</span></span> <span data-ttu-id="c179d-115">Fare clic con il pulsante destro del mouse su ALTspaceVR **e scegliere Opzioni** avanzate dal menu visualizzato.</span><span class="sxs-lookup"><span data-stu-id="c179d-115">Left-click AltspaceVR and select **Advanced Options** from the menu that appears.</span></span>

![Menu App e funzionalità aperto con l'opzione Avanzate evidenziata](images/app-version-img-02.png)

<span data-ttu-id="c179d-117">In **Opzioni avanzate,** sotto l'intestazione **Specifiche,** la versione **dell'app** deve essere elencata a destra dell'etichetta **Versione.**</span><span class="sxs-lookup"><span data-stu-id="c179d-117">In the **Advanced Options**, under the **Specifications** header, the **App Version** should be listed to the right of the **Version** label.</span></span>

![Opzioni avanzate aperte con la versione dell'app evidenziata](images/app-version-img-03.png)

## <a name="in-client-logs"></a><span data-ttu-id="c179d-119">Nei log del client</span><span class="sxs-lookup"><span data-stu-id="c179d-119">In Client Logs</span></span>

<span data-ttu-id="c179d-120">AltspaceVR segnala la versione dell'app nel file di log del client come "Altspace Version" durante l'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c179d-120">AltspaceVR reports the app version in the client logs file as "Altspace Version" during application startup.</span></span> <span data-ttu-id="c179d-121">Si tratta di un'opzione valida per ottenere la versione dell'app se non è possibile accedere correttamente al client, ma si è tentato di avviarla prima che si verificasse un errore.</span><span class="sxs-lookup"><span data-stu-id="c179d-121">This would be a good option to get the app version if you can't successfully log into the client, but it did attempt to start before failing.</span></span>

## <a name="windows"></a><span data-ttu-id="c179d-122">Windows</span><span class="sxs-lookup"><span data-stu-id="c179d-122">Windows</span></span>

<span data-ttu-id="c179d-123">In Windows il file di log del client è disponibile Esplora risorse in:</span><span class="sxs-lookup"><span data-stu-id="c179d-123">On Windows, the client logs file can be found via Windows Explorer at:</span></span>

```
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player.log
%userprofile%\AppData\LocalLow\Microsoft\AltspaceVR\Player-prev.log
```

<span data-ttu-id="c179d-124">Questo file viene sovrascritto ogni volta che si avvia AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="c179d-124">This file is overwritten each time you launch AltspaceVR.</span></span> <span data-ttu-id="c179d-125">'Player.log' rappresenta la sessione più recente e 'Player-prev.log' rappresenta la sessione precedente.</span><span class="sxs-lookup"><span data-stu-id="c179d-125">'Player.log' represents your latest session, and 'Player-prev.log' represents the previous session.</span></span>

## <a name="via-powershell"></a><span data-ttu-id="c179d-126">Tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="c179d-126">Via PowerShell</span></span>

<span data-ttu-id="c179d-127">Gli utenti avanzati possono cercare questa stringa nei log del client tramite PowerShell come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c179d-127">Advanced users can search the client logs for this string via PowerShell as follows:</span></span>

<span data-ttu-id="c179d-128">Input:</span><span class="sxs-lookup"><span data-stu-id="c179d-128">Input:</span></span>

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

<span data-ttu-id="c179d-129">Output:</span><span class="sxs-lookup"><span data-stu-id="c179d-129">Output:</span></span>

<span data-ttu-id="c179d-130">[2.047] AltspaceVR Versione: 3.2.23.e66c2</span><span class="sxs-lookup"><span data-stu-id="c179d-130">[2.047] AltspaceVR Version: 3.2.23.e66c2</span></span>