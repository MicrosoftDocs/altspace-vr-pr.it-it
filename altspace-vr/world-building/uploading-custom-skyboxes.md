---
title: Caricamento di SKYBOX personalizzati
description: Istruzioni dettagliate sul caricamento e la risoluzione dei problemi di SKYBOX personalizzati in AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: SKYBOX, risoluzione dei problemi
ms.openlocfilehash: 02d5bc762dc36d4195100e8155d6250789e833f7
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213261"
---
# <a name="uploading-custom-skyboxes"></a><span data-ttu-id="08e0b-104">Caricamento di SKYBOX personalizzati</span><span class="sxs-lookup"><span data-stu-id="08e0b-104">Uploading custom Skyboxes</span></span>

<span data-ttu-id="08e0b-105">Un skybox è un modo per creare uno **sfondo** per il mondo che rende l'esperienza più immersiva.</span><span class="sxs-lookup"><span data-stu-id="08e0b-105">A Skybox is a way to create a **background** for your World that makes the experience more immersive.</span></span> <span data-ttu-id="08e0b-106">Sono disponibili diversi tipi di SKYBOX, ma è attualmente supportata la **equirettangolare**.</span><span class="sxs-lookup"><span data-stu-id="08e0b-106">There are different kinds of Skyboxes but we currently support **equirectangular**.</span></span> <span data-ttu-id="08e0b-107">Di seguito è riportato un esempio con una fotocamera 360 (altro esempio [qui](http://moments.mankindforward.com/)):</span><span class="sxs-lookup"><span data-stu-id="08e0b-107">Here's an example taken with a 360 camera (more example [here](http://moments.mankindforward.com/)):</span></span> 

![360 visualizzazione equirettangolare di una sala da lavoro](images/custom-skyboxes-img-01.jpeg)

<span data-ttu-id="08e0b-109">È anche possibile usare l'utilità di [caricamento Unity](world-building-toolkit-getting-started.md) ma questo approccio è più semplice.</span><span class="sxs-lookup"><span data-stu-id="08e0b-109">You can also use the [Unity Uploader](world-building-toolkit-getting-started.md) but this approach is simpler.</span></span>

1. <span data-ttu-id="08e0b-110">Passare a [worlds > SKYBOX](https://account.altvr.com/skyboxes) e fare clic sul pulsante **Create (crea** ) a destra.</span><span class="sxs-lookup"><span data-stu-id="08e0b-110">Navigate to [Worlds > Skyboxes](https://account.altvr.com/skyboxes) and press the **Create** button on the right</span></span>

![Pagina del sito Web Worlds aperta al pannello SKYBOX](images/custom-skyboxes-img-02.png)

2. <span data-ttu-id="08e0b-112">Immettere un nome e specificare l'immagine 360.</span><span class="sxs-lookup"><span data-stu-id="08e0b-112">Fill in a name and specify your 360 image.</span></span> <span data-ttu-id="08e0b-113">Non è necessario che sia una foto, sono disponibili programmi che consentono di creare un progetto personalizzato oppure è possibile eseguire ricerche in linea.</span><span class="sxs-lookup"><span data-stu-id="08e0b-113">It doesn't have to be a photo, there are programs that let you draw your own or you can search for some online.</span></span> <span data-ttu-id="08e0b-114">Al termine, selezionare **Crea**.</span><span class="sxs-lookup"><span data-stu-id="08e0b-114">When you're ready, select **Create**.</span></span> 

![Form creazione SKYBOX](images/custom-skyboxes-img-03.png)

3. <span data-ttu-id="08e0b-116">Facoltativamente, è possibile caricare un'immagine di **Anteprima** per poter identificare facilmente questo skybox.</span><span class="sxs-lookup"><span data-stu-id="08e0b-116">You can optionally upload a **preview** image so you can easily identify this skybox.</span></span> <span data-ttu-id="08e0b-117">È anche possibile caricare audio di ambiente in formato WAV.</span><span class="sxs-lookup"><span data-stu-id="08e0b-117">You can also upload ambient audio in WAV format.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="08e0b-118">Quando si carica l'immagine 360, è consigliabile caricare separatamente immagini di anteprima e audio di ambiente.</span><span class="sxs-lookup"><span data-stu-id="08e0b-118">We recommend you upload preview images and ambient audio separately, after you upload the 360 image.</span></span> <span data-ttu-id="08e0b-119">Se vengono caricati insieme, le dimensioni dei file possono essere sufficientemente grandi per bloccare il processo.</span><span class="sxs-lookup"><span data-stu-id="08e0b-119">If you upload them together the file sizes can be large enough to stall the process.</span></span> <span data-ttu-id="08e0b-120">[Pronipoti World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) è un ottimo esempio di come usare un Skybox con audio ambiente.</span><span class="sxs-lookup"><span data-stu-id="08e0b-120">[Jetsons World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) is a great example of how to use a Skybox with ambient audio.</span></span> <span data-ttu-id="08e0b-121">Si noti che il generatore mondiale ha mantenuto il volume audio basso e che i suoni che si sentono sono sporadici in modo che gli utenti non siano annoiati.</span><span class="sxs-lookup"><span data-stu-id="08e0b-121">Notice how the World-Builder kept the audio volume low and sounds you hear are sporadic so people don't get annoyed.</span></span> 

4. <span data-ttu-id="08e0b-122">Entra nel mondo e Apri l'editor mondiale.</span><span class="sxs-lookup"><span data-stu-id="08e0b-122">Enter your World and open the World Editor.</span></span> <span data-ttu-id="08e0b-123">In SKYBOX selezionare il nuovo skybox.</span><span class="sxs-lookup"><span data-stu-id="08e0b-123">Under Skyboxes, select your new Skybox.</span></span> <span data-ttu-id="08e0b-124">In pochi secondi, il cielo cambierà letteralmente.</span><span class="sxs-lookup"><span data-stu-id="08e0b-124">In a few seconds, the sky will literally change.</span></span> <span data-ttu-id="08e0b-125">Gli altri utenti del mondo vedranno anche il cambiamento in cielo.</span><span class="sxs-lookup"><span data-stu-id="08e0b-125">Others in your World will also see the sky change.</span></span> <span data-ttu-id="08e0b-126">Per tornare indietro, scegliere il SKYBOX **predefinito** nello stesso elenco.</span><span class="sxs-lookup"><span data-stu-id="08e0b-126">To switch back, choose the **default** skybox in that same list.</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="08e0b-127">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="08e0b-127">Troubleshooting</span></span>

<span data-ttu-id="08e0b-128">**C'è una linea di giunzione o una linea nella:-(cielo.**</span><span class="sxs-lookup"><span data-stu-id="08e0b-128">**There's a seam or line in the sky :-(.**</span></span> <span data-ttu-id="08e0b-129">Si tratta di un bug che verrà risolto a breve</span><span class="sxs-lookup"><span data-stu-id="08e0b-129">It's a bug that we'll fix soon</span></span>

<span data-ttu-id="08e0b-130">**Caricamento non riuscito**</span><span class="sxs-lookup"><span data-stu-id="08e0b-130">**Upload failed**</span></span>
    * <span data-ttu-id="08e0b-131">provare a caricare solo l'immagine 360 autonomamente</span><span class="sxs-lookup"><span data-stu-id="08e0b-131">try uploading just the 360 image on its own</span></span>
    * <span data-ttu-id="08e0b-132">provare con un altro file più piccolo come test</span><span class="sxs-lookup"><span data-stu-id="08e0b-132">try with another, smaller file as a test</span></span>

<span data-ttu-id="08e0b-133">**Non è possibile trovare una foto di 360**</span><span class="sxs-lookup"><span data-stu-id="08e0b-133">**I can't find a 360 photo**</span></span>
    * <span data-ttu-id="08e0b-134">Flickr è una fonte ideale (modificare i filtri per trovare i Commons creativi)</span><span class="sxs-lookup"><span data-stu-id="08e0b-134">Flickr is a good source (change the filters to find creative commons ones)</span></span>
    * <span data-ttu-id="08e0b-135">Prendi la tua!</span><span class="sxs-lookup"><span data-stu-id="08e0b-135">Take your own!</span></span> <span data-ttu-id="08e0b-136">Abbiamo avuto successo con le fotocamere di Ricoh.</span><span class="sxs-lookup"><span data-stu-id="08e0b-136">We've had success with Ricoh's cameras.</span></span> 
<span data-ttu-id="08e0b-137">**Il cielo sembra granulare o bloccare** Potrebbe essere necessario trovare un'immagine a risoluzione superiore.</span><span class="sxs-lookup"><span data-stu-id="08e0b-137">**The sky looks grainy or blocky** You may need to find a higher-resolution image.</span></span> <span data-ttu-id="08e0b-138">In genere circa 2-5 MB e ~ 5000 px x 2000 px</span><span class="sxs-lookup"><span data-stu-id="08e0b-138">Typically around 2-5 MB and ~5000 px x 2000 px</span></span>

<span data-ttu-id="08e0b-139">**Il framerate del mondo è danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="08e0b-139">**It hurts my World's framerate!**</span></span>
<span data-ttu-id="08e0b-140">L'immagine è probabilmente troppo grande.</span><span class="sxs-lookup"><span data-stu-id="08e0b-140">The image is probably too large.</span></span> <span data-ttu-id="08e0b-141">Alcuni SKYBOX generati possono essere di 8 KB.</span><span class="sxs-lookup"><span data-stu-id="08e0b-141">Some generated skyboxes can be 8k.</span></span> <span data-ttu-id="08e0b-142">Sono in genere dotati di versioni di 2K compatibili con dispositivi mobili.</span><span class="sxs-lookup"><span data-stu-id="08e0b-142">They usually come with mobile-friendly 2k versions--use that.</span></span>

<span data-ttu-id="08e0b-143">**Supporto per l'audio di ambiente**</span><span class="sxs-lookup"><span data-stu-id="08e0b-143">**Help me with the ambient audio**</span></span>
    * <span data-ttu-id="08e0b-144">USA software gratuito come Audacity per abbassare il volume o creare cicli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="08e0b-144">Use free software like Audacity to lower the volume or create your own loops.</span></span> <span data-ttu-id="08e0b-145">Tenere presente che l'audio verrà ripetuto e riprodotto negli orecchi degli utenti, per mantenerlo insufficiente e non fastidioso</span><span class="sxs-lookup"><span data-stu-id="08e0b-145">Remember that the audio will be repeated and playing in people's ears so keep it low and not annoying</span></span>
    * <span data-ttu-id="08e0b-146">Il [suono gratuito](https://freesound.org/) è un'ottima fonte di suoni Royalty-Free</span><span class="sxs-lookup"><span data-stu-id="08e0b-146">[Free Sound](https://freesound.org/) is a good source of royalty-free sounds</span></span>
