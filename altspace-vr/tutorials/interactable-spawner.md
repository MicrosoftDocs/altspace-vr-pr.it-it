---
title: Uso di Interactables spawner
description: Informazioni su come creare, usare e personalizzare il interactables spawner per inserire gli elementi negli spazi AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: Generator, interazioni, personalizzazioni
ms.openlocfilehash: 7f4b87591b2e11b2084af4d2bf83748ed51fd193
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213549"
---
# <a name="using-the-interactables-spawner"></a><span data-ttu-id="e293f-104">Uso di Interactables spawner</span><span class="sxs-lookup"><span data-stu-id="e293f-104">Using the Interactables Spawner</span></span>

<span data-ttu-id="e293f-105">Il Interactables spawner consente di inserire elementi interagiscono nell'evento, nel mondo o nello spazio domestico.</span><span class="sxs-lookup"><span data-stu-id="e293f-105">The Interactables Spawner allows you to place interactable items in your event, world, or home-space.</span></span> <span data-ttu-id="e293f-106">Questa funzionalità è attualmente parte del [programma di accesso in primo](../world-building/early-access.md) luogo e non sarà disponibile a meno che non si sia scelto di usare il menu principale.</span><span class="sxs-lookup"><span data-stu-id="e293f-106">This feature is currently part of our [Early Access Program](../world-building/early-access.md) and won't be available unless you've opted in through your Main Menu.</span></span>

> [!NOTE]
> <span data-ttu-id="e293f-107">Sebbene continuiamo a pilotare questa funzionalità, tenere presente che la generazione di un numero eccessivo di interactables potrebbe influire sulle prestazioni dell'ambiente o dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e293f-107">While we continue to pilot this feature please be aware that spawning too many interactables may affect the performance of your environment or event.</span></span> 

## <a name="creating-an-interactable"></a><span data-ttu-id="e293f-108">Creazione di un'interfaccia</span><span class="sxs-lookup"><span data-stu-id="e293f-108">Creating an interactable</span></span>

<span data-ttu-id="e293f-109">Per trasformare l'oggetto in un oggetto interagibile:</span><span class="sxs-lookup"><span data-stu-id="e293f-109">To turn your object into an interactable object:</span></span>

1. <span data-ttu-id="e293f-110">Posizionare l'oggetto nello spazio.</span><span class="sxs-lookup"><span data-stu-id="e293f-110">Place the object in your space.</span></span>
2. <span data-ttu-id="e293f-111">Individuare quindi la voce nell'elenco di oggetti e selezionare l'icona a forma di **ingranaggio** accanto per aprirne le impostazioni:</span><span class="sxs-lookup"><span data-stu-id="e293f-111">Then, find the entry in the object list, and select the **gear icon** next to it to open its settings:</span></span>

![Editor globale aperto con elenco oggetti evidenziato](images/interactables-spawner-img-01.png)

<span data-ttu-id="e293f-113">Nella pagina Settings (impostazioni) si troverà una nuova casella di controllo **"generatore di oggetti"**, che viene usata per renderlo un oggetto interactabile.</span><span class="sxs-lookup"><span data-stu-id="e293f-113">On the settings page you’ll find a new checkbox **“Object spawner“**, which is used to make it an interactable object.</span></span>

1. <span data-ttu-id="e293f-114">Selezionare la casella e selezionare **conferma**.</span><span class="sxs-lookup"><span data-stu-id="e293f-114">Check the box and select **confirm**.</span></span>
2. <span data-ttu-id="e293f-115">In modalità di modifica è possibile spostare la posizione di generazione dell'oggetto nello spazio.</span><span class="sxs-lookup"><span data-stu-id="e293f-115">While in edit mode, you can move around the object’s spawn location in the space.</span></span>
3. <span data-ttu-id="e293f-116">**Uscire dalla modalità di modifica** per abilitare l'interazione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e293f-116">**Exit edit mode** to enable item interaction.</span></span>

![Aggiorna finestra artefatto aperta nell'app AltspaceVR](images/interactables-spawner-img-02.png)

## <a name="other-customizations"></a><span data-ttu-id="e293f-118">Altre personalizzazioni</span><span class="sxs-lookup"><span data-stu-id="e293f-118">Other customizations</span></span>

<span data-ttu-id="e293f-119">Dopo l'abilitazione di **"generatore oggetti"** quando si torna alle proprietà di tale oggetto, è possibile applicare un'impostazione aggiuntiva per la modalità di comportamento dell'oggetto generato.</span><span class="sxs-lookup"><span data-stu-id="e293f-119">After enabling **“Object spawner”** when you go back into the properties for that object, there will be an extra setting you can apply to how the spawned object behaves.</span></span>

> [!NOTE]
> <span data-ttu-id="e293f-120">Scalabilità di oggetti interagiscono: consente di impostare la scala dell'oggetto quando viene prelevato, rispetto alla "scalabilità", che rappresenta la scalabilità della modalità di visualizzazione dell'oggetto in tutto il mondo prima di selezionarlo per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="e293f-120">Interactable object scale: This sets the scale of the object when it gets picked up, compared to “Scale” which is the scale of how the object appears in the world prior to picking it up for the first time.</span></span>

<span data-ttu-id="e293f-121">I creatori di kit possono notare che le modifiche apportate al kit durante l'esecuzione di AltspaceVR non saranno effettive fino al riavvio di AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="e293f-121">Kit makers may notice that changes to your Kit while AltspaceVR is running won't take effect until you restart AltspaceVR.</span></span>

<span data-ttu-id="e293f-122">Di recente è stato aggiunto un pulsante nella scheda **Impostazioni moderate** denominata **ricarica mondi Kit**.</span><span class="sxs-lookup"><span data-stu-id="e293f-122">Recently we’ve added a button under the **Moderate Settings** tab called **Reload Worlds Kits**.</span></span> <span data-ttu-id="e293f-123">Se si fa clic su questo pulsante, è sufficiente immettere nuovamente lo spazio, ricaricando nuovamente tutti i kit, in modo da scaricare solo le nuove versioni dei kit aggiornati mentre si era in AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="e293f-123">Clicking this button causes (just you) to reenter the space, reloading all Kits again, which will download only new versions of the Kits that have been updated while you were in AltspaceVR.</span></span>

![Pannello impostazioni moderato aperto nell'app AltspaceVR](images/interactables-spawner-img-03.png)