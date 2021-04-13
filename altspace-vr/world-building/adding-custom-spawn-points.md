---
title: Aggiunta di punti di spawn personalizzati
description: Informazioni su come creare, aggiungere e risolvere i problemi relativi ai punti di spawn personalizzati a AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: SpawnPoint, risoluzione dei problemi
ms.openlocfilehash: 0f53bdc229eb21e50edef34981c592556236fc55
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212817"
---
# <a name="adding-custom-spawn-points"></a>Aggiunta di punti di spawn personalizzati

Le persone che entrano nel mondo verranno **generate** o visualizzate nell'origine, posizione (0, 0, 0), quando entrano nel mondo. Tuttavia, è possibile aggiungere uno o più punti di spawn se si vuole, ad affermare, fare in modo che gli utenti inizino dall'ingresso al castello. Se si specificano più punti di generazione, ne verrà scelta casualmente ogni volta che un utente immette e l'origine non verrà inclusa. È possibile gestire i punti di spawn per qualsiasi mondo o evento in cui è abilitato l'editor mondiale. È possibile controllare la posizione in cui gli utenti generano (position) e la direzione in cui verranno rivolte (rotazione). I punti di generazione saranno visibili solo in modalità di modifica. 

1. Spostarsi in prossimità della posizione in cui si desidera che le persone generino. Aprire l' **Editor del mondo > nozioni di base** e assicurarsi che la rotazione del **blocco** sia selezionata. Selezionare il **punto di spawn** per crearne uno. Spostarlo nella posizione esatta desiderata:

![Finestra di base dell'editor del mondo aperta](images/spawn-points-img-01.png)

2. Selezionare sull'icona delle impostazioni per il punto di spawn e verificare che la **rotazione > X** e la **rotazione > Z** siano entrambe **0**. Si tratta di un numero ridotto, ad esempio **8.537777745 e-07**. Questo è un aspetto peculiare del modo in cui vengono gestiti i numeri a virgola mobile:

![Aggiornare i punti di spawn nelle impostazioni dell'editor del mondo](images/spawn-points-img-02.png)

3. Reimmettere il mondo tramite **Menu > impostazioni > generale > immettere nuovamente spazio > immettere nuovamente**
4. È necessario generare un nuovo punto di spawn.
5. Se si vuole che gli utenti facciano una direzione diversa, selezionare le impostazioni per il punto di spawn e impostare la **rotazione > solo Y** . Provare a impostare Y su 180 e sia X che Z su 0 (avviso: la X e la Z sono avanzate possono rendere le persone malate). Quindi selezionare **conferma** e reimmettere il mondo. Il che dovrebbe generare la direzione opposta. 

## <a name="troubleshooting"></a>Risoluzione dei problemi

**Gli utenti continuano a generare l'origine?**
    * Assicurarsi che i punti di generazione siano leggermente sopra il terreno o la superficie. Se il punto di spawn si sovrappone ad altri oggetti, gli utenti generano il percorso predefinito, ovvero l'origine. Questo problema può verificarsi se il punto di spawn all'interno di un oggetto e l'altezza della persona variano. 
    * Provare a reimpostare il mondo tramite **Menu > impostazioni > modera > Reimposta spazio**

**Si hanno più punti di spawn ma si sta ancora generando la stessa posizione?**
Potrebbe essere sfortunato, perché è casuale dopo tutto. Provare a rientrare almeno cinque volte prima di presumere che si verifichi un errore. 

**Le persone sono scomode o la loro testa è inclinata** È possibile che si sia dimenticato di controllare la **rotazione dei blocchi** o di impostare il valore X e Z per la rotazione. Che in genere devono essere impostate su 0, a meno che non si stia creando un mondo esotico. 

**Persone in calo quando vengono generate?**
Non impostare la posizione del punto di spawn troppo alta sopra un oggetto. Se sono troppo lontani, verranno rigenerati all'origine.