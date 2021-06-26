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
# <a name="granting-world-roles"></a>Concessione di ruoli del mondo

Altspace ha un sistema ruoli e capacità. Ogni persona può avere più ruoli e i relativi ruoli possono essere diversi a seconda della posizione. Ogni ruolo, a sua volta, offre una o più capacità. Ad esempio, quando si è nel proprio evento, si ricevono automaticamente i ruoli **host** **e moderatore.** Con questi due ruoli è possibile avviare utenti indisciplinati, essere sul palco e magari rilasciare i coriandoli.

1. Modificare il mondo e cercare ruoli contestuali nella colonna destra **(** Come [gestire Worlds](managing-worlds.md))

![Modifica dei ruoli nella sezione Ruoli contestuali dei mondi](images/granting-roles.png)

2. Fare **clic su Aggiungi** utente nel campo Ruoli **contestuali** per concedere ruoli specifici a utenti specifici solo per questo mondo. Ad esempio, se si vuole assegnare il **moderatore host,** è necessario aggiungere l'elemento precedente  +  e selezionare **Salva**. Il formato è **username,** username non fa distinzione tra maiuscole e minuscole, scegli il ruolo dal menu a discesa **Terraformer,** fai clic su Aggiungi utente più volte per mantenere l'aggiunta di altri utenti e quindi fai clic su **Aggiorna**.

* Per fare in modo che la modifica abbia effetto in Altspace, è necessario reimpostare lo spazio nel mondo forzando tutti a ricongiungersi o a fare in modo che ogni utente con un nuovo ruolo si ricongiunti al mondo.

3. Modificare il **campo Ruoli contestuali** predefiniti, nella **sezione In VR,** se si vuole concedere un ruolo a ogni utente che si unisce al mondo. Ad esempio, se si vuole consentire agli utenti di usare il megafono per potersi ascoltare mentre sono in una parte lontana, aggiungere quanto segue:

```
pilot,megaphone_only
```

Dopo aver selezionato **Aggiorna**, Reimposta spazio nel mondo. Questo avrà effetto solo su questo mondo. Se si vogliono concedere ruoli a un intero universo, modificare gli stessi campi nell'universo. Lo stesso vale per gli eventi, se si vuole che tutti gli utenti dell'evento abbia questi ruoli, è necessario aggiungerli ai ruoli **contexuali** predefiniti dell'evento stesso.

## <a name="roles"></a>Ruoli

* **Megaphone_only:** possibilità di parlare alle orecchini degli utenti ovunque si trova nel mondo
* **Moderatore:** capacità come **kick** per mantenere il decoro
* **Pilota:** possibilità di attivare/disattivare la modalità fly e generare lo strumento di volo 6DOF
* **Host:** capacità come la possibilità di essere sul palco, avere un megafono
* **Terraformer:** possibilità di usare World Editor Altre informazioni su ([Ruoli in eventi, mondi, gruppi e in AltspaceVR](../getting-started/roles.md))

## <a name="troubleshooting"></a>Risoluzione dei problemi

**È possibile eliminare i ruoli?**
Sì, modificare il mondo, fare clic **su Rimuovi** sotto il ruolo che si desidera eliminare e fare clic su **Aggiorna**

**I ruoli vengono copiati quando un mondo viene importato da un altro?**
No, i ruoli non vengono copiati