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
# <a name="finding-the-altspacevr-app-version"></a><span data-ttu-id="ef71b-104">Ricerca della versione dell'app AltspaceVR</span><span class="sxs-lookup"><span data-stu-id="ef71b-104">Finding the AltspaceVR app version</span></span>

<span data-ttu-id="ef71b-105">Nel corso della risoluzione di un problema, è possibile che venga richiesta la versione dell'app AltspaceVR attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ef71b-105">In the course of troubleshooting an issue, you may be asked what version of the AltspaceVR app you're currently running.</span></span>

## <a name="in-altspacevr"></a><span data-ttu-id="ef71b-106">In AltspaceVR</span><span class="sxs-lookup"><span data-stu-id="ef71b-106">In AltspaceVR</span></span>

<span data-ttu-id="ef71b-107">Per trovare la versione dell'app in AltspaceVR, passare al **menu Settings (impostazioni** ) e selezionare **About (informazioni** ) nella barra di spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="ef71b-107">To find the app version in AltspaceVR, navigate to the **settings menu** and select **About** in the left navigation bar.</span></span> <span data-ttu-id="ef71b-108">La versione dell'app è riportata qui, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ef71b-108">The 'App Version' is reported here, as shown in the screenshot below.</span></span>

![Menu impostazioni aperto con informazioni sul pannello Apri](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a><span data-ttu-id="ef71b-110">In impostazioni di sistema Windows</span><span class="sxs-lookup"><span data-stu-id="ef71b-110">In Windows System Settings</span></span>

<span data-ttu-id="ef71b-111">Se è stato installato AltspaceVR tramite il Microsoft Store, è anche possibile trovare la versione dell'app nelle impostazioni di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef71b-111">If you installed AltspaceVR via the Microsoft Store, you can additionally find the app version in the Windows system settings.</span></span>  <span data-ttu-id="ef71b-112">Questo scenario è adatto quando si segnala la versione dell'app se non si riesce ad accedere al client.</span><span class="sxs-lookup"><span data-stu-id="ef71b-112">This scenario is a good fit when reporting the app version if you're unable to successfully log into the client.</span></span>

<span data-ttu-id="ef71b-113">Per trovare la versione dell'app nelle impostazioni di sistema di Windows, aprire il **menu Start**, digitare **app & funzionalità** e selezionare il risultato.</span><span class="sxs-lookup"><span data-stu-id="ef71b-113">To find the app version in Windows system settings, open the **Start Menu**, type in **Apps & Features**, and select the result.</span></span> <span data-ttu-id="ef71b-114">Passare a **AltspaceVR** nell'elenco delle app.</span><span class="sxs-lookup"><span data-stu-id="ef71b-114">Navigate to **AltspaceVR** in the list of apps.</span></span> <span data-ttu-id="ef71b-115">Fare clic con il pulsante destro del mouse su AltspaceVR e scegliere **Opzioni avanzate** dal menu visualizzato.</span><span class="sxs-lookup"><span data-stu-id="ef71b-115">Left-click AltspaceVR and select **Advanced Options** from the menu that appears.</span></span>

![Menu app e funzionalità aperto con l'opzione avanzate evidenziata](images/app-version-img-02.png)

<span data-ttu-id="ef71b-117">Nelle **Opzioni avanzate**, sotto l'intestazione **specifiche** , la **versione dell'app** deve essere elencata a destra dell'etichetta **versione** .</span><span class="sxs-lookup"><span data-stu-id="ef71b-117">In the **Advanced Options**, under the **Specifications** header, the **App Version** should be listed to the right of the **Version** label.</span></span>

![Opzioni avanzate aperte con la versione dell'app evidenziata](images/app-version-img-03.png)

## <a name="in-client-logs"></a><span data-ttu-id="ef71b-119">Nei log del client</span><span class="sxs-lookup"><span data-stu-id="ef71b-119">In Client Logs</span></span>

<span data-ttu-id="ef71b-120">AltspaceVR segnala la versione dell'app nel file di log del client come "versione Altspace" durante l'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ef71b-120">AltspaceVR reports the app version in the client logs file as "Altspace Version" during application startup.</span></span> <span data-ttu-id="ef71b-121">Si tratta di un'opzione valida per ottenere la versione dell'app se non è possibile accedere al client, ma si è tentato di avviare prima di avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ef71b-121">This would be a good option to get the app version if you can't successfully log into the client, but it did attempt to start before failing.</span></span>

## <a name="windows"></a><span data-ttu-id="ef71b-122">Windows</span><span class="sxs-lookup"><span data-stu-id="ef71b-122">Windows</span></span>

<span data-ttu-id="ef71b-123">In Windows è possibile trovare il file di log del client tramite Esplora risorse all'indirizzo:</span><span class="sxs-lookup"><span data-stu-id="ef71b-123">On Windows, the client logs file can be found via Windows Explorer at:</span></span>

```
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player.log
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player-prev.log
```

<span data-ttu-id="ef71b-124">Questo file viene sovrascritto ogni volta che si avvia AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="ef71b-124">This file is overwritten each time you launch AltspaceVR.</span></span> <span data-ttu-id="ef71b-125">' Player. log ' rappresenta la sessione più recente è Player-Prev. log ' rappresenta la sessione precedente.</span><span class="sxs-lookup"><span data-stu-id="ef71b-125">'Player.log' represents your latest session, and 'Player-prev.log' represents the previous session.</span></span>

## <a name="via-powershell"></a><span data-ttu-id="ef71b-126">Tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef71b-126">Via PowerShell</span></span>

<span data-ttu-id="ef71b-127">Gli utenti avanzati possono cercare questa stringa tramite PowerShell nei log del client, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ef71b-127">Advanced users can search the client logs for this string via PowerShell as follows:</span></span>

<span data-ttu-id="ef71b-128">Input:</span><span class="sxs-lookup"><span data-stu-id="ef71b-128">Input:</span></span>

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

<span data-ttu-id="ef71b-129">Output:</span><span class="sxs-lookup"><span data-stu-id="ef71b-129">Output:</span></span>

<span data-ttu-id="ef71b-130">[2,047] AltspaceVR versione: 3.2.23. e66c2</span><span class="sxs-lookup"><span data-stu-id="ef71b-130">[2.047] AltspaceVR Version: 3.2.23.e66c2</span></span>