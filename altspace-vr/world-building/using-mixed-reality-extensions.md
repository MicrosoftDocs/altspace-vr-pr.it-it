---
title: Uso di un'estensione di realtà mista
description: Informazioni su come usare e risolvere i problemi delle estensioni di realtà mista per estendere e adattare i mondi AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: realtà mista, estensioni, risoluzione dei problemi
ms.openlocfilehash: 1439ca76eaf4e0235c6552d037e55b6151e08407871bf470b3011b6cf8cbccd5
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125358"
---
# <a name="using-a-mixed-reality-extension"></a>Uso di un'estensione di realtà mista

[Mixed Reality Extensions](https://developer.altvr.com/) (MRE) sono app che è possibile usare in Worlds, dai [caschi](https://account.altvr.com/mres/1173667287173955931) a uno [Stargate funzionante.](https://account.altvr.com/mres/1152987031857529562) Questo è il modo in cui i membri della community con esperienza di programmazione possono estendere Altspace e i World Builder unidireli possono rendere i loro mondi più interattivi. Anche se i mre possono essere usati da chiunque in un mondo, solo gli utenti del World Building Program possono esplorare e generare mre nei loro mondi. 

1. Esplorare la sezione MRE del sito [Web](https://account.altvr.com/mres). Per impostazione predefinita, verranno visualizzati i propri MRE, quindi selezionare **Altspace** per visualizzare mre ufficiali e **in** primo piano per visualizzare i mre della community. Acquisire familiarità con qualsiasi MRE prima di usarlo nel proprio mondo. 
2. Passare a [Caschi](https://account.altvr.com/mres/1173667287173955931) MRE e selezionare **Copia negli Appunti.** 
3. Immettere world e aprire World Editor to **Basics**> SDK App . Incollare l'URL di Caschi nel campo URI di destinazione e selezionare **Conferma**. L'oggetto MRE dovrebbe essere visualizzato e tentare di connettersi all'MRE in esecuzione nel cloud. A questo punto dovrebbero essere visualizzati alcuni caschi su cui è possibile fare clic.
4. Spostare/ruotare/ridimensionare l'oggetto MRE esattamente come qualsiasi altro world object.

Congratulazioni! A questo punto si usano IAS. È così interessante.

## <a name="troubleshooting"></a>Risoluzione dei problemi

**MRE mostra un emoji accigliato** 
    * Verificare che l'URL sia corretto
    * **Attivare/disattivare l'opzione** In riproduzione nell'oggetto e scegliere **conferma**
    * Provare a rientrare

**MRE è in ritardo** A seconda della posizione in cui è ospitato un MRE, è possibile che si verifichi una latenza di rete

**Perché è necessario incollare gli URL?**
In futuro, è possibile gestire e generare mres come si fa Artifacts da Kits. Fino ad allora, si continuerà a usare gli URL