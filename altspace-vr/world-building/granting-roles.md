---
title: Concessione di ruoli a livello mondiale
description: Informazioni sul sistema di ruoli e capacità e istruzioni dettagliate per concedere agli utenti ruoli nei propri sistemi AltspaceVR.
ms.date: 04/14/2021
ms.topic: article
keywords: Ruoli
ms.openlocfilehash: f299f637d77c989be5504532279fb42451367b4ac53095d00627f67402dd8552
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127122"
---
# <a name="granting-world-roles"></a>Concessione di ruoli a livello mondiale

Altspace ha un sistema di ruoli e capacità. Ogni persona può avere più ruoli e i relativi ruoli possono essere diversi a seconda di dove si trova. Ogni ruolo, a sua volta, offre una o più capacità. Ad esempio, quando si è nel proprio evento, si ricevono automaticamente i **ruoli di host** e **moderatore.** Con questi due ruoli è possibile avviare utenti indisciplinati, essere sul lavoro e forse rilasciare i coriandoli.

1. Modificare il mondo e cercare la colonna a destra per i ruoli **contestuali** ([Come gestire i world )](managing-worlds.md)

![Modifica dei ruoli nella sezione dei ruoli contestuali dei mondo](images/granting-roles.png)

2. Fare **clic su Add User** (Aggiungi utente) nel campo Contextual Roles **(Ruoli** contestuali) se si vogliono concedere ruoli specifici a utenti specifici solo per questo mondo. Ad esempio, se si vuole assegnare il **moderatore host**, è necessario aggiungere il  +  codice precedente e selezionare **Salva**. Il formato è **nome** utente, nome utente senza distinzione tra maiuscole e minuscole, scegliere il ruolo dal menu a discesa **Terraformer,** fare clic su Aggiungi utente più volte per mantenere l'aggiunta di altri utenti e quindi fare clic su **Aggiorna**.

* Per fare in modo che la modifica abbia effetto in Altspace, è necessario reimpostare lo spazio nel mondo forzando tutti a ricongiungersi o fare in modo che ogni utente con un nuovo ruolo si ricongiunti al mondo.

3. Modificare il **campo Default Contextual Roles (Ruoli** contestuali predefiniti) nella sezione In **VR** (Realtà virtuale) se si vuole concedere un ruolo a ogni utente che si unisce a World. Ad esempio, se si vuole consentire alle persone di far volo e usare il megafono in modo che possano ascoltare l'un l'altro mentre sono da lontano, aggiungere quanto segue:

```
pilot,megaphone_only
```

Dopo aver selezionato **Update (Aggiorna),** Reset Space in the World (Reimposta spazio nel mondo). Ciò influirà solo su questo mondo. Se vuoi concedere ruoli a un intero universo, modifica gli stessi campi nell'Universo. Lo stesso vale per gli eventi. Se si vuole che tutti gli utenti dell'evento abbia questi ruoli, è necessario aggiungerli ai ruoli **predefiniti contexuali** dell'evento stesso.

## <a name="roles"></a>Ruoli

* **Megaphone_only:** la possibilità di parlare nei riti degli utenti ovunque si trova nel mondo
* **Moderatore:** capacità come **il kick** per mantenere il decoro
* **Pilota:** possibilità di attivare/disattivare la modalità a comparsa e generare lo strumento di volo 6DOF
* **Host:** capacità come la possibilità di essere sul stage, avere megaphone
* **Terraformer:** possibilità di usare World Editor Altre informazioni su ([Roles in events, worlds, groups, and in AltspaceVR](../getting-started/roles.md))

## <a name="troubleshooting"></a>Risoluzione dei problemi

**È possibile eliminare i ruoli?**
Sì, modifica il tuo mondo, fai clic **su Rimuovi** sotto il ruolo che vuoi eliminare e fai clic su **Aggiorna**

**I ruoli vengono copiati durante l'importazione di un elemento World da un altro?**
No, i ruoli non vengono copiati