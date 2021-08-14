---
title: Aggiunta di punti di generazione personalizzati
description: Informazioni su come creare, aggiungere e risolvere i problemi dei punti di generazione personalizzati in AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: spawnpoint, risoluzione dei problemi
ms.openlocfilehash: 53ff2e60d929aed9be5650b132da6d1dab8e6f1c5a78425dc5f17c10f2c4dfdb
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127263"
---
# <a name="adding-custom-spawn-points"></a>Aggiunta di punti di generazione personalizzati

Le persone che  entrano nel mondo generano o compaiono all'origine, alla posizione (0,0,0), quando entrano nel mondo. Tuttavia, è possibile aggiungere uno o più punti di generazione se si vuole, ad esempio, fare in modo che le persone inizino all'ingresso del tuo castello. Se si specificano più punti di generazione, ne verrà scelto uno in modo casuale ogni volta che un utente entra e l'origine non verrà inclusa. È possibile gestire Spawn Points in qualsiasi mondo o evento in cui è abilitato World Editor. È possibile controllare dove le persone generano (posizione) e in quale direzione verranno rivolte (rotazione). I punti di generazione saranno visibili solo in modalità di modifica. 

1. Andare vicino al punto in cui si vuole che le persone denotino la generazione. Aprire **World Editor > Basics (Nozioni di** base) e assicurarsi che **l'opzione Lock Rotation (Blocca rotazione)** sia selezionata. Selezionare **Spawn Point (Genera** punto) per crearne uno. Spostarlo nella posizione esatta desiderata:

![Finestra Nozioni di base dell'editor del mondo aperta](images/spawn-points-img-01.png)

2. Selezionare l'icona delle impostazioni per Punto di generazione e assicurarsi che **l'opzione Rotazione** > X e Rotazione > **Z** siano **entrambe 0.** Se sono numeri piccoli come **8,537777745E-07,** va bene anche questo. Si tratta di un'incoerdità di come vengono gestiti i numeri a virgola mobile:

![Aggiornare i punti di generazione nelle impostazioni dell'editor del mondo](images/spawn-points-img-02.png)

3. Reenter your World via **Menu > Impostazioni > General > Reenter Space > re-Enter**
4. È consigliabile generare il nuovo punto di generazione.
5. Se si vuole che le persone si facciano fronte a una direzione diversa, selezionare le impostazioni per Punto di generazione e impostare **Rotazione > solo Y.** Provare a impostare Y su 180 e sia X che Z su 0 (Avviso: X e Z sono avanzati possono far ammalare le persone). Selezionare quindi **Conferma** e immettere di nuovo il mondo. Verrà generato l'oggetto rivolto verso la direzione opposta. 

## <a name="troubleshooting"></a>Risoluzione dei problemi

**Le persone continuano a generare all'origine?**
    * Assicurarsi che i punti di generazione siano leggermente al di sopra del suolo o della superficie. Se il punto di generazione si sovrappone ad altri oggetti, gli utenti vengono generati nella posizione predefinita, l'origine. Ciò può verificarsi se il punto di generazione all'interno di un oggetto e l'altezza della persona varia. 
    * Provare a reimpostare il mondo tramite **menu > Impostazioni > moderare > reimpostazione dello spazio**

**Sono presenti più punti di generazione, ma la generazione è ancora nello stesso punto?**
Si potrebbe essere sforcati, è casuale, dopo tutto. Provare a rientrare almeno cinque volte prima di presumere che si sia verificato un errore. 

**Le persone sono scomode o la testa è inclinata** È possibile che si sia dimenticato di selezionare **Blocca rotazione o** di impostare il valore X e Z per Rotazione. Questi valori devono in genere essere impostati su 0, a meno che non si sta creando un mondo invaso. 

**Persone che cadono quando generano?**
Non impostare la posizione del punto di generazione troppo in alto sopra un oggetto. Se cadono troppo lontano, verranno ripresi all'origine.