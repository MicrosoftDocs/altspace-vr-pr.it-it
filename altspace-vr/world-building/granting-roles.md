---
title: Concessione di ruoli del mondo
description: Informazioni sul sistema di ruoli e capacità e istruzioni dettagliate per fornire agli utenti ruoli nel mondo AltspaceVR.
ms.date: 04/14/2021
ms.topic: article
keywords: Ruoli
ms.openlocfilehash: 3a1d0f138b29fe545f52d851ff00062f156a860e
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923194"
---
# <a name="granting-world-roles"></a><span data-ttu-id="f21c3-104">Concessione di ruoli del mondo</span><span class="sxs-lookup"><span data-stu-id="f21c3-104">Granting world roles</span></span>

<span data-ttu-id="f21c3-105">Altspace ha un sistema ruoli e capacità.</span><span class="sxs-lookup"><span data-stu-id="f21c3-105">Altspace has a Roles and Abilities system.</span></span> <span data-ttu-id="f21c3-106">Ogni persona può avere più ruoli e i relativi ruoli possono essere diversi a seconda della posizione.</span><span class="sxs-lookup"><span data-stu-id="f21c3-106">Each person can have multiple roles and their roles can be different depending on where they are.</span></span> <span data-ttu-id="f21c3-107">Ogni ruolo, a sua volta, offre una o più capacità.</span><span class="sxs-lookup"><span data-stu-id="f21c3-107">Each role, in turn, gives you one or more abilities.</span></span> <span data-ttu-id="f21c3-108">Ad esempio, quando si è nel proprio evento, si ricevono automaticamente i ruoli **host** **e moderatore.**</span><span class="sxs-lookup"><span data-stu-id="f21c3-108">For example, when you're in your own event, you automatically receive the **host** and **moderator** roles.</span></span> <span data-ttu-id="f21c3-109">Con questi due ruoli è possibile avviare utenti indisciplinati, essere sul palco e magari rilasciare i coriandoli.</span><span class="sxs-lookup"><span data-stu-id="f21c3-109">With those two roles you can kick unruly users, be on stage, and maybe release the confetti.</span></span>

1. <span data-ttu-id="f21c3-110">Modificare il mondo e cercare ruoli contestuali nella colonna destra **(** Come [gestire Worlds](managing-worlds.md))</span><span class="sxs-lookup"><span data-stu-id="f21c3-110">Edit your World and look over to the right column for **Contextual Roles** ([How to manage Worlds](managing-worlds.md))</span></span>

![Modifica dei ruoli nella sezione Ruoli contestuali dei mondi](images/granting-roles.png)

2. <span data-ttu-id="f21c3-112">Fare **clic su Aggiungi** utente nel campo Ruoli **contestuali** per concedere ruoli specifici a utenti specifici solo per questo mondo.</span><span class="sxs-lookup"><span data-stu-id="f21c3-112">Click **Add User** under the **Contextual Roles** field if you want to grant specific roles to specific users just for this World.</span></span> <span data-ttu-id="f21c3-113">Ad esempio, se si vuole assegnare il **moderatore host,** è necessario aggiungere l'elemento precedente  +  e selezionare **Salva**.</span><span class="sxs-lookup"><span data-stu-id="f21c3-113">For example, if you want to give me **host** + **moderator**, you would add the above and select **Save**.</span></span> <span data-ttu-id="f21c3-114">Il formato è **username,** username non fa distinzione tra maiuscole e minuscole, scegli il ruolo dal menu a discesa **Terraformer,** fai clic su Aggiungi utente più volte per mantenere l'aggiunta di altri utenti e quindi fai clic su **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="f21c3-114">The format is **username**, username is case-insensitive, choose the role from the dropdown menu **Terraformer**, click Add User multiple times to keeping adding more users and then click **Update**.</span></span>

* <span data-ttu-id="f21c3-115">Per fare in modo che la modifica abbia effetto in Altspace, è necessario reimpostare lo spazio nel mondo forzando tutti a ricongiungersi o a fare in modo che ogni utente con un nuovo ruolo si ricongiunti al mondo.</span><span class="sxs-lookup"><span data-stu-id="f21c3-115">In order for the change to take effect in Altspace, you should Reset Space the world forcing everyone to rejoin or have each user with a new role rejoin the world.</span></span>

3. <span data-ttu-id="f21c3-116">Modificare il **campo Ruoli contestuali** predefiniti, nella **sezione In VR,** se si vuole concedere un ruolo a ogni utente che si unisce al mondo.</span><span class="sxs-lookup"><span data-stu-id="f21c3-116">Edit the **Default Contextual Roles** field, under the **In VR** section, if you want to grant a role to every one that joins your World.</span></span> <span data-ttu-id="f21c3-117">Ad esempio, se si vuole consentire agli utenti di usare il megafono per potersi ascoltare mentre sono in una parte lontana, aggiungere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f21c3-117">For example, if you want to let people fly and use the megaphone so they can hear each other while far part, add the following:</span></span>

```
pilot,megaphone_only
```

<span data-ttu-id="f21c3-118">Dopo aver selezionato **Aggiorna**, Reimposta spazio nel mondo.</span><span class="sxs-lookup"><span data-stu-id="f21c3-118">After you select **Update**, Reset Space in the World.</span></span> <span data-ttu-id="f21c3-119">Questo avrà effetto solo su questo mondo.</span><span class="sxs-lookup"><span data-stu-id="f21c3-119">This will only affect this World.</span></span> <span data-ttu-id="f21c3-120">Se si vogliono concedere ruoli a un intero universo, modificare gli stessi campi nell'universo.</span><span class="sxs-lookup"><span data-stu-id="f21c3-120">If you want to grant roles to an entire Universe, edit the same fields on the Universe.</span></span> <span data-ttu-id="f21c3-121">Lo stesso vale per gli eventi, se si vuole che tutti gli utenti dell'evento abbia questi ruoli, è necessario aggiungerli ai ruoli **contexuali** predefiniti dell'evento stesso.</span><span class="sxs-lookup"><span data-stu-id="f21c3-121">The same goes for events, if you want everyone in your event to have these roles you'll need to add this to the **Default Contexual Roles** of the event itself.</span></span>

## <a name="roles"></a><span data-ttu-id="f21c3-122">Ruoli</span><span class="sxs-lookup"><span data-stu-id="f21c3-122">Roles</span></span>

* <span data-ttu-id="f21c3-123">**Megaphone_only:** possibilità di parlare alle orecchini degli utenti ovunque si trova nel mondo</span><span class="sxs-lookup"><span data-stu-id="f21c3-123">**Megaphone_only** - ability to speak into users' ears wherever they are in the World</span></span>
* <span data-ttu-id="f21c3-124">**Moderatore:** capacità come **kick** per mantenere il decoro</span><span class="sxs-lookup"><span data-stu-id="f21c3-124">**Moderator** - abilities like **kick** to maintain decorum</span></span>
* <span data-ttu-id="f21c3-125">**Pilota:** possibilità di attivare/disattivare la modalità fly e generare lo strumento di volo 6DOF</span><span class="sxs-lookup"><span data-stu-id="f21c3-125">**Pilot** - ability to toggle fly mode and spawn the 6DOF flight tool</span></span>
* <span data-ttu-id="f21c3-126">**Host:** capacità come la possibilità di essere sul palco, avere un megafono</span><span class="sxs-lookup"><span data-stu-id="f21c3-126">**Host** - abilities like being able to be on stage, have megaphone</span></span>
* <span data-ttu-id="f21c3-127">**Terraformer:** possibilità di usare World Editor Altre informazioni su ([Ruoli in eventi, mondi, gruppi e in AltspaceVR](../getting-started/roles.md))</span><span class="sxs-lookup"><span data-stu-id="f21c3-127">**Terraformer** - ability to use the World Editor More information about ([Roles in events, worlds, groups, and in AltspaceVR](../getting-started/roles.md))</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f21c3-128">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="f21c3-128">Troubleshooting</span></span>

<span data-ttu-id="f21c3-129">**È possibile eliminare i ruoli?**</span><span class="sxs-lookup"><span data-stu-id="f21c3-129">**Can I delete roles?**</span></span>
<span data-ttu-id="f21c3-130">Sì, modificare il mondo, fare clic **su Rimuovi** sotto il ruolo che si desidera eliminare e fare clic su **Aggiorna**</span><span class="sxs-lookup"><span data-stu-id="f21c3-130">Yes, edit your world, click **Remove** below the role you'd like to delete and click **Update**</span></span>

<span data-ttu-id="f21c3-131">**I ruoli vengono copiati quando un mondo viene importato da un altro?**</span><span class="sxs-lookup"><span data-stu-id="f21c3-131">**Are roles copied when a World is importing from another?**</span></span>
<span data-ttu-id="f21c3-132">No, i ruoli non vengono copiati</span><span class="sxs-lookup"><span data-stu-id="f21c3-132">No, roles aren't copied</span></span>