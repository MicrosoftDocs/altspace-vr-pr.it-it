---
title: Concessione dei ruoli internazionali
description: Informazioni sul sistema dei ruoli e delle funzionalità e istruzioni dettagliate per fornire agli utenti i ruoli nei AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Ruoli
ms.openlocfilehash: f8cd55fbd8ede6cedd199724a3e6b2413c5bc3e6
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212792"
---
# <a name="granting-world-roles"></a><span data-ttu-id="b6af7-104">Concessione dei ruoli internazionali</span><span class="sxs-lookup"><span data-stu-id="b6af7-104">Granting world roles</span></span>

<span data-ttu-id="b6af7-105">Altspace dispone di un sistema Roles and Capacity.</span><span class="sxs-lookup"><span data-stu-id="b6af7-105">Altspace has a Roles and Abilities system.</span></span> <span data-ttu-id="b6af7-106">Ogni persona può avere più ruoli e i relativi ruoli possono essere diversi a seconda della posizione in cui si trovano.</span><span class="sxs-lookup"><span data-stu-id="b6af7-106">Each person can have multiple roles and their roles can be different depending on where they are.</span></span> <span data-ttu-id="b6af7-107">Ogni ruolo, a sua volta, offre una o più funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b6af7-107">Each role, in turn, gives you one or more abilities.</span></span> <span data-ttu-id="b6af7-108">Ad esempio, quando ci si trova nel proprio evento, si ricevono automaticamente i ruoli **Presenter** e **Moderator** .</span><span class="sxs-lookup"><span data-stu-id="b6af7-108">For example, when you're in your own event, you automatically receive the **presenter** and **moderator** roles.</span></span> <span data-ttu-id="b6af7-109">Con questi due ruoli è possibile avviare gli utenti indisciplinati e forse rilasciare i coriandoli.</span><span class="sxs-lookup"><span data-stu-id="b6af7-109">With those two roles you can kick unruly users, be on stage, and maybe release the confetti.</span></span> 

1. <span data-ttu-id="b6af7-110">Modificare il mondo e scorrere verso il basso fino alla sezione **in VR** ([How to Manage Worlds](managing-worlds.md))</span><span class="sxs-lookup"><span data-stu-id="b6af7-110">Edit your World and scroll down to the **In VR** section ([How to manage Worlds](managing-worlds.md))</span></span>

![Modifica dei ruoli nella sezione VR del mondo](images/granting-roles.png)

2. <span data-ttu-id="b6af7-112">Modificare il campo **ruoli** se si desidera concedere ruoli specifici a utenti specifici solo per questo mondo.</span><span class="sxs-lookup"><span data-stu-id="b6af7-112">Edit the **Roles** field if you want to grant specific roles to specific users just for this World.</span></span> <span data-ttu-id="b6af7-113">Se, ad esempio, si desidera concedere a un moderatore **Presenter**  +   e a calen **Moderator**, aggiungere quanto segue e selezionare **Salva**.</span><span class="sxs-lookup"><span data-stu-id="b6af7-113">For example, if you want to give me **presenter** + **moderator** and give Calen **moderator**, you would add the following and select **Save**.</span></span> <span data-ttu-id="b6af7-114">Il formato è **{Role}, {username o email}** in ogni riga.</span><span class="sxs-lookup"><span data-stu-id="b6af7-114">The format is **{role},{username or email}** on each line.</span></span> <span data-ttu-id="b6af7-115">Il nome utente non distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b6af7-115">Username is case-insensitive.</span></span> 

```
presenter,jimmy
moderator,jimmy
moderator,calen
```

3. <span data-ttu-id="b6af7-116">Se si seleziona nuovamente **modifica** , verrà visualizzato quanto segue sopra il campo ruoli.</span><span class="sxs-lookup"><span data-stu-id="b6af7-116">If you select **Edit** again, you should see the following above the Roles field.</span></span> <span data-ttu-id="b6af7-117">Questo è il modo in cui si conosce l'aggiornamento nel database.</span><span class="sxs-lookup"><span data-stu-id="b6af7-117">That's how you know updated in the database.</span></span>

```
Presenters: jimmy
Moderators: jimmy,calen
```

* <span data-ttu-id="b6af7-118">Per rendere effettive le modifiche in Altspace, è necessario reimpostare il mondo, forzando la riaggiunta di tutti.</span><span class="sxs-lookup"><span data-stu-id="b6af7-118">In order for the change to take effect in Altspace, you should reset the world, forcing everyone to rejoin.</span></span> <span data-ttu-id="b6af7-119">Di seguito è riportato un elenco completo dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="b6af7-119">There's a full list of roles below.</span></span>

4. <span data-ttu-id="b6af7-120">Modificare il campo dei **ruoli contestuali** se si vuole concedere un ruolo a tutti gli utenti che si uniscono al mondo.</span><span class="sxs-lookup"><span data-stu-id="b6af7-120">Edit the **Contextual Roles** field if you want to grant a role to every one that joins your World.</span></span> <span data-ttu-id="b6af7-121">Se, ad esempio, si desidera consentire agli utenti di volare e utilizzare il megafono in modo da poterli ascoltare a vicenda, aggiungere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b6af7-121">For example, if you want to let people fly and use the megaphone so they can hear each other while far part, add the following:</span></span>

```
pilot,megaphone_only
```

<span data-ttu-id="b6af7-122">Dopo aver selezionato **Aggiorna**, reimpostare il mondo.</span><span class="sxs-lookup"><span data-stu-id="b6af7-122">After you select **Update**, reset the World.</span></span> <span data-ttu-id="b6af7-123">Questa operazione avrà effetto solo su questo mondo.</span><span class="sxs-lookup"><span data-stu-id="b6af7-123">This will only affect this World.</span></span> <span data-ttu-id="b6af7-124">Se si vuole concedere i ruoli a un intero universo, modificare gli stessi campi nell'universo.</span><span class="sxs-lookup"><span data-stu-id="b6af7-124">If you want to grant roles to an entire Universe, edit the same fields on the Universe.</span></span> 

## <a name="roles"></a><span data-ttu-id="b6af7-125">Ruoli</span><span class="sxs-lookup"><span data-stu-id="b6af7-125">Roles</span></span> 

* <span data-ttu-id="b6af7-126">**Relatore** -capacità come essere in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="b6af7-126">**Presenter** - abilities like being able to be on stage</span></span>
* <span data-ttu-id="b6af7-127">**Moderatore** -capacità come **Kick** per la manutenzione del decoro</span><span class="sxs-lookup"><span data-stu-id="b6af7-127">**Moderator** - abilities like **kick** to maintain decorum</span></span>
* <span data-ttu-id="b6af7-128">Responsabile della **bonifica** -possibilità di usare l'editor globale</span><span class="sxs-lookup"><span data-stu-id="b6af7-128">**Terraformer** - ability to use the World Editor</span></span>
* <span data-ttu-id="b6af7-129">**Progetto pilota** : possibilità di impostare la modalità di volo e generare lo strumento 6DOF Flight</span><span class="sxs-lookup"><span data-stu-id="b6af7-129">**Pilot** - ability to toggle fly mode and spawn the 6DOF flight tool</span></span>
* <span data-ttu-id="b6af7-130">**Megaphone_only** la possibilità di comunicare con le orecchie degli utenti ovunque si trovino nel mondo</span><span class="sxs-lookup"><span data-stu-id="b6af7-130">**Megaphone_only** - ability to speak into users' ears wherever they are in the World</span></span>
* <span data-ttu-id="b6af7-131">**Showcase_new_sdk** la possibilità di generare app MRE SDK</span><span class="sxs-lookup"><span data-stu-id="b6af7-131">**Showcase_new_sdk** - ability to spawn MRE SDK apps</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b6af7-132">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="b6af7-132">Troubleshooting</span></span>

<span data-ttu-id="b6af7-133">**È possibile eliminare I ruoli?**</span><span class="sxs-lookup"><span data-stu-id="b6af7-133">**Can I delete roles?**</span></span>
<span data-ttu-id="b6af7-134">Non dal form in questo momento, quindi è possibile archiviare un Richiesta di supporto in help.altvr.com, che verrà preso in considerazione</span><span class="sxs-lookup"><span data-stu-id="b6af7-134">Not from the form right now so file a Support request at help.altvr.com and we'll take care of it for you</span></span>

<span data-ttu-id="b6af7-135">**I ruoli vengono copiati quando un mondo viene importato da un altro?**</span><span class="sxs-lookup"><span data-stu-id="b6af7-135">**Are roles copied when a World is importing from another?**</span></span>
<span data-ttu-id="b6af7-136">No, i ruoli non vengono copiati</span><span class="sxs-lookup"><span data-stu-id="b6af7-136">No, roles aren't copied</span></span>