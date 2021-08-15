---
title: Uso dello strumento di generazione interactable
description: Informazioni su come creare, usare e personalizzare lo strumento di generazione di oggetti interactable per inserire elementi negli spazi AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: spawner, interazioni, personalizzazioni
ms.openlocfilehash: abeddec5c2b50e0612db5efb6bc2e3c5bd9de4a8b67c50b19afee18b17c5e746
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127401"
---
# <a name="using-the-interactables-spawner"></a>Uso dello strumento di generazione interactable

Lo spawner Interactables consente di inserire elementi con interazione nell'evento, nel mondo o nello spazio iniziale. Questa funzionalità fa attualmente parte del programma [Ad](../world-building/early-access.md) accesso anticipato e non sarà disponibile a meno che non si sia acconsentito esplicitamente tramite il menu principale.

> [!NOTE]
> Anche se si continua a eseguire il progetto pilota di questa funzionalità, tenere presente che la generazione di un numero troppo grande di interazioni può influire sulle prestazioni dell'ambiente o dell'evento. 

## <a name="creating-an-interactable"></a>Creazione di un oggetto con interazione

Per trasformare l'oggetto in un oggetto che può interagire:

1. Posizionare l'oggetto nello spazio.
2. Trovare quindi la voce nell'elenco di oggetti e selezionare **l'icona** a forma di ingranaggio accanto per aprirne le impostazioni:

![Editor world aperto con l'elenco di oggetti evidenziato](images/interactables-spawner-img-01.png)

Nella pagina delle impostazioni è disponibile una nuova casella di controllo **"Object spawner"**(Genera oggetto), che viene usata per renderla un oggetto con interazione.

1. Selezionare la casella e quindi **confermare**.
2. In modalità di modifica è possibile spostarsi nella posizione di generazione dell'oggetto nello spazio.
3. **Uscire dalla modalità di modifica** per abilitare l'interazione tra elementi.

![Finestra aggiorna elemento aperta nell'app AltspaceVR](images/interactables-spawner-img-02.png)

## <a name="other-customizations"></a>Altre personalizzazioni

Dopo aver **abilitato "Genera oggetto"** quando si torna alle proprietà per tale oggetto, è possibile applicare un'impostazione aggiuntiva al comportamento dell'oggetto generato.

> [!NOTE]
> Scala dell'oggetto con interazione: imposta la scala dell'oggetto quando viene prelevato, rispetto a "Scale", ovvero la scala di come l'oggetto appare nel mondo prima di raccoglierlo per la prima volta.

Gli autori di kit potrebbero notare che le modifiche apportate al kit mentre AltspaceVR è in esecuzione non saranno effettive fino a quando non si riavvia AltspaceVR.

Di recente è stato aggiunto un pulsante nella scheda **Moderate Impostazioni** denominata **Reload Worlds Kits**. Se si fa clic su questo pulsante, (solo l'utente) inserirà nuovamente lo spazio, ricaricando di nuovo tutti i kit, scaricando solo le nuove versioni dei kit che sono state aggiornate mentre si era in AltspaceVR.

![Moderare il pannello delle impostazioni aperto nell'app AltspaceVR](images/interactables-spawner-img-03.png)