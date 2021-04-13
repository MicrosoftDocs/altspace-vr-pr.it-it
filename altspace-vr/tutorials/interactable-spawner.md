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
# <a name="using-the-interactables-spawner"></a>Uso di Interactables spawner

Il Interactables spawner consente di inserire elementi interagiscono nell'evento, nel mondo o nello spazio domestico. Questa funzionalità è attualmente parte del [programma di accesso in primo](../world-building/early-access.md) luogo e non sarà disponibile a meno che non si sia scelto di usare il menu principale.

> [!NOTE]
> Sebbene continuiamo a pilotare questa funzionalità, tenere presente che la generazione di un numero eccessivo di interactables potrebbe influire sulle prestazioni dell'ambiente o dell'evento. 

## <a name="creating-an-interactable"></a>Creazione di un'interfaccia

Per trasformare l'oggetto in un oggetto interagibile:

1. Posizionare l'oggetto nello spazio.
2. Individuare quindi la voce nell'elenco di oggetti e selezionare l'icona a forma di **ingranaggio** accanto per aprirne le impostazioni:

![Editor globale aperto con elenco oggetti evidenziato](images/interactables-spawner-img-01.png)

Nella pagina Settings (impostazioni) si troverà una nuova casella di controllo **"generatore di oggetti"**, che viene usata per renderlo un oggetto interactabile.

1. Selezionare la casella e selezionare **conferma**.
2. In modalità di modifica è possibile spostare la posizione di generazione dell'oggetto nello spazio.
3. **Uscire dalla modalità di modifica** per abilitare l'interazione dell'elemento.

![Aggiorna finestra artefatto aperta nell'app AltspaceVR](images/interactables-spawner-img-02.png)

## <a name="other-customizations"></a>Altre personalizzazioni

Dopo l'abilitazione di **"generatore oggetti"** quando si torna alle proprietà di tale oggetto, è possibile applicare un'impostazione aggiuntiva per la modalità di comportamento dell'oggetto generato.

> [!NOTE]
> Scalabilità di oggetti interagiscono: consente di impostare la scala dell'oggetto quando viene prelevato, rispetto alla "scalabilità", che rappresenta la scalabilità della modalità di visualizzazione dell'oggetto in tutto il mondo prima di selezionarlo per la prima volta.

I creatori di kit possono notare che le modifiche apportate al kit durante l'esecuzione di AltspaceVR non saranno effettive fino al riavvio di AltspaceVR.

Di recente è stato aggiunto un pulsante nella scheda **Impostazioni moderate** denominata **ricarica mondi Kit**. Se si fa clic su questo pulsante, è sufficiente immettere nuovamente lo spazio, ricaricando nuovamente tutti i kit, in modo da scaricare solo le nuove versioni dei kit aggiornati mentre si era in AltspaceVR.

![Pannello impostazioni moderato aperto nell'app AltspaceVR](images/interactables-spawner-img-03.png)