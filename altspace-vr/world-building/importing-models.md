---
title: Importazione di modelli glTF
description: Informazioni su come importare correttamente i modelli glTF 3D nelle esperienze di AltspaceVR e risolvere eventuali problemi.
ms.date: 03/11/2021
ms.topic: article
keywords: modelli, glTF, importazione, Sketchfab, risoluzione dei problemi
ms.openlocfilehash: 4489f90832bd1cf85ff161caed11684257cce6ab
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213260"
---
# <a name="importing-gltf-models"></a><span data-ttu-id="e9b41-104">Importazione di modelli glTF</span><span class="sxs-lookup"><span data-stu-id="e9b41-104">Importing glTF models</span></span>

> [!NOTE]
> <span data-ttu-id="e9b41-105">Questa funzionalità è disponibile per gli utenti selezionati nel programma di accesso anticipato al momento.</span><span class="sxs-lookup"><span data-stu-id="e9b41-105">This feature is available for select users in the Early Access program at this time.</span></span>

<span data-ttu-id="e9b41-106">Un modo per portare i modelli e le scene 3D in Altspace consiste nell'usare lo [standard glTF](https://en.wikipedia.org/wiki/GlTF).</span><span class="sxs-lookup"><span data-stu-id="e9b41-106">One way to bring 3D models and scenes into Altspace is using the [glTF standard](https://en.wikipedia.org/wiki/GlTF).</span></span> <span data-ttu-id="e9b41-107">È possibile caricare un file con estensione GLB (compresso glTF) per creare un modello che è possibile generare in un secondo momento nell'editor mondiale.</span><span class="sxs-lookup"><span data-stu-id="e9b41-107">You can upload a .glb file (packed glTF) to create a Model that you can later spawn in the World Editor.</span></span> <span data-ttu-id="e9b41-108">Si tratta di un'alternativa al [caricamento di kit personalizzati](uploading-custom-kits.md).</span><span class="sxs-lookup"><span data-stu-id="e9b41-108">It's an alternative to [uploading your own Kits](uploading-custom-kits.md).</span></span> <span data-ttu-id="e9b41-109">È consigliabile creare modelli per dimostrazioni rapide perché non è necessario usare Unity e kit quando si desidera ottimizzare le prestazioni e la riusabilità.</span><span class="sxs-lookup"><span data-stu-id="e9b41-109">We recommend creating Models for quick demonstrations because you won't need to use Unity, and Kits when you want to maximize performance and reusability.</span></span> 

1. <span data-ttu-id="e9b41-110">Trovare alcune risorse glTF 3D.</span><span class="sxs-lookup"><span data-stu-id="e9b41-110">Find some glTF 3D assets.</span></span> <span data-ttu-id="e9b41-111">Una posizione in cui eseguire la ricerca è Sketchfab (provare a filtrare per modelli **scaricabili** come [questo](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models)).</span><span class="sxs-lookup"><span data-stu-id="e9b41-111">One place to search is Sketchfab (try filtering for **Downloadable** models like [this](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models)).</span></span> <span data-ttu-id="e9b41-112">Una volta individuato, selezionare **Scarica modello 3D**:</span><span class="sxs-lookup"><span data-stu-id="e9b41-112">Once you find it, select **Download 3D Model**:</span></span>

![modello Dog 3D da Sketchfab](images/importing-models-img-01.png)

2. <span data-ttu-id="e9b41-114">Copiare il collegamento al modello e leggere i requisiti di licenza.</span><span class="sxs-lookup"><span data-stu-id="e9b41-114">Copy the link to the model and read the licensing requirements.</span></span> 
3. <span data-ttu-id="e9b41-115">Scaricare la versione **glTF (autoconverted Format)**</span><span class="sxs-lookup"><span data-stu-id="e9b41-115">Download the **Autoconverted Format (glTF)** version</span></span>

![Opzioni di download di Sketchfab con formato convertito automaticamente evidenziato](images/importing-models-img-02.png)

4. <span data-ttu-id="e9b41-117">Aprire il sito di [GLB Packer](https://glb-packer.glitch.me) e selezionare la casella **Converti png in JPEG (beta)**</span><span class="sxs-lookup"><span data-stu-id="e9b41-117">Open the [GLB Packer](https://glb-packer.glitch.me) site and check the box **Convert PNG to JPEG (beta)**</span></span>
5. <span data-ttu-id="e9b41-118">Decomprimere i file glTF scaricati e trascinarli tutti contemporaneamente nella scheda del browser GLB Packer</span><span class="sxs-lookup"><span data-stu-id="e9b41-118">Uncompress the glTF files you downloaded and drag them all at once into the GLB Packer browser tab</span></span>

![Finestra che mostra la decompressione del modello](images/importing-models-img-03.png)

6. <span data-ttu-id="e9b41-120">A seconda del numero e delle dimensioni dei file, l'elaborazione potrebbe richiedere del tempo.</span><span class="sxs-lookup"><span data-stu-id="e9b41-120">Depending on the number and size of the files, it may take a while to process.</span></span> <span data-ttu-id="e9b41-121">Al termine dell'elaborazione, verrà scaricato un file **out. glb** .</span><span class="sxs-lookup"><span data-stu-id="e9b41-121">When processing is done, an **out.glb** file will be downloaded.</span></span> <span data-ttu-id="e9b41-122">Rinominare il file con informazioni informative: si tratta del nome dell'oggetto in tutto il mondo, ad esempio **Low Poly Wolf. glb**</span><span class="sxs-lookup"><span data-stu-id="e9b41-122">Rename that file to something informative--this will be the name of the object in the world (e.g **Low Poly Wolf.glb**)</span></span>
7. <span data-ttu-id="e9b41-123">Passare a [altvr.com > altri modelli di >](https://account.altvr.com/users/sign_in) e selezionare **Crea**</span><span class="sxs-lookup"><span data-stu-id="e9b41-123">Navigate to [altvr.com > More > Models](https://account.altvr.com/users/sign_in) and select **Create**</span></span>
8. <span data-ttu-id="e9b41-124">Specificare il percorso del file con estensione GLB e assicurarsi di copiare il collegamento Sketchfab nella descrizione per l'attribuzione.</span><span class="sxs-lookup"><span data-stu-id="e9b41-124">Specify the location of the .glb file and make sure you copy the Sketchfab link into the description for attribution.</span></span> <span data-ttu-id="e9b41-125">Se lo si desidera, è possibile specificare un'immagine di anteprima, quindi selezionare **Crea modello**:</span><span class="sxs-lookup"><span data-stu-id="e9b41-125">You can specify a preview image if you want, then select **Create Model**:</span></span>

![Anteprima modello in AltspaceVR](images/importing-models-img-04.png)

9. <span data-ttu-id="e9b41-127">Selezionare **copia negli Appunti**</span><span class="sxs-lookup"><span data-stu-id="e9b41-127">Select **Copy to Clipboard**</span></span>
10. <span data-ttu-id="e9b41-128">Aprire l' **Editor del mondo > Altspace > nozioni di base > GLTF**</span><span class="sxs-lookup"><span data-stu-id="e9b41-128">Open the **World Editor > Altspace > Basics > GLTF**</span></span>
11. <span data-ttu-id="e9b41-129">Incollare l'URL e selezionare **conferma**</span><span class="sxs-lookup"><span data-stu-id="e9b41-129">Paste in your url and select **Confirm**</span></span>

<span data-ttu-id="e9b41-130">Congratulazioni.</span><span class="sxs-lookup"><span data-stu-id="e9b41-130">Congrats!</span></span> <span data-ttu-id="e9b41-131">È stato appena generato il primo modello.</span><span class="sxs-lookup"><span data-stu-id="e9b41-131">You just spawned your first Model.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e9b41-132">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="e9b41-132">Troubleshooting</span></span>

<span data-ttu-id="e9b41-133">**Quando si fa clic su **conferma** non è successo nulla**</span><span class="sxs-lookup"><span data-stu-id="e9b41-133">**When I clicked **Confirm** nothing happened**</span></span>
    * <span data-ttu-id="e9b41-134">È attualmente disponibile un limite di 100.000 poligoni.</span><span class="sxs-lookup"><span data-stu-id="e9b41-134">We currently have a 100k polygon limit.</span></span> <span data-ttu-id="e9b41-135">In caso di errore, eliminare l'oggetto per evitare potenziali problemi relativi agli utenti che si uniscono al mondo</span><span class="sxs-lookup"><span data-stu-id="e9b41-135">If it fails, delete the Object to avoid potential problems with users joining your World</span></span>
    * <span data-ttu-id="e9b41-136">Potrebbero esserci altri problemi con l'asset.</span><span class="sxs-lookup"><span data-stu-id="e9b41-136">There may be other problems with the asset.</span></span> <span data-ttu-id="e9b41-137">Provare a usare asset con il minor numero di poligoni possibile.</span><span class="sxs-lookup"><span data-stu-id="e9b41-137">Try to use assets with as few polygons as possible.</span></span>
    * <span data-ttu-id="e9b41-138">Il modello che si sta inserendo può essere piccolo o grande.</span><span class="sxs-lookup"><span data-stu-id="e9b41-138">The model you're bringing in may be small or large.</span></span> <span data-ttu-id="e9b41-139">Provare ad aumentare o ridurre la scala o spostare l'avatar in un modello.</span><span class="sxs-lookup"><span data-stu-id="e9b41-139">Try increasing/decreasing the Scale or move your avatar around, you might be standing inside the model!</span></span>

<span data-ttu-id="e9b41-140">**Il caricamento è lento** La velocità di caricamento da parte di altri utenti in tutto il mondo dipenderà dalla velocità di connessione.</span><span class="sxs-lookup"><span data-stu-id="e9b41-140">**It's slow to load** How quickly other users in the World load it will depend on their connection speeds.</span></span> <span data-ttu-id="e9b41-141">Inoltre, non viene memorizzato nella cache come asset Kit.</span><span class="sxs-lookup"><span data-stu-id="e9b41-141">It's also not cached like Kit assets.</span></span> <span data-ttu-id="e9b41-142">Se ne viene inserito uno nella Home page, si esaurirà il download dello stesso modello ogni volta che si partecipa, che non è eccezionale.</span><span class="sxs-lookup"><span data-stu-id="e9b41-142">If you place one in your Home, you'll end up redownloading the same Model every time you join, which isn't great.</span></span>

<span data-ttu-id="e9b41-143">Non **ci sono collisioni** Per impostazione predefinita, non esiste alcuna collisione sugli oggetti portati in questo modo</span><span class="sxs-lookup"><span data-stu-id="e9b41-143">**There's no collision** By default there's no collision on the objects that are brought in this way</span></span>

<span data-ttu-id="e9b41-144">**Quando viene generato, perdo i miei controlli su sei DOF o sono all'interno di, quindi è difficile modificarlo** Sì, sono consapevoli di questi problemi e ci auguriamo di risolverli a breve.</span><span class="sxs-lookup"><span data-stu-id="e9b41-144">**When I spawn it, I lose my controls on six DOF or I'm inside so it's hard to manipulate it** Yes, we're aware of these issues and hope to address them soon.</span></span>  