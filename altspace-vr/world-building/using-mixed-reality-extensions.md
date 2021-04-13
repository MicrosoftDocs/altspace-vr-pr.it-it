---
title: Uso di un'estensione di realtà mista
description: Informazioni su come usare e risolvere i problemi delle estensioni per la realtà mista per estendere e adattare i AltspaceVR World.
ms.date: 03/11/2021
ms.topic: article
keywords: realtà mista, estensioni, risoluzione dei problemi
ms.openlocfilehash: 498e71c48f7c67abc40ce4f4667c9eeac4c4e73b
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212641"
---
# <a name="using-a-mixed-reality-extension"></a>Uso di un'estensione di realtà mista

Le estensioni per la [realtà mista](https://developer.altvr.com/) (MRES) sono app che puoi usare nei tuoi mondi dai [caschi](https://account.altvr.com/mres/1173667287173955931) a uno [Stargate](https://account.altvr.com/mres/1152987031857529562)funzionante. Questo è il modo in cui i membri della community con esperienza di programmazione possono estendere Altspace e i creatori di un mondo unidirezionale possono rendere i propri mondi più interattivi. Sebbene MREs possa essere usato da chiunque in un mondo, solo le persone nel programma di compilazione mondiale possono esplorare e generare MREs nei loro mondi. 

1. Esplorare la sezione MRE del [sito Web](https://account.altvr.com/mres). Per impostazione predefinita, verrà visualizzato il proprio MREs, quindi selezionare in **Altspace** per vedere MRES ufficiale e in **primo piano** per visualizzare MRES dalla community. Acquisire familiarità con qualsiasi MRE prima di utilizzarlo nel mondo. 
2. Passare al MRE dei [caschi](https://account.altvr.com/mres/1173667287173955931) e selezionare **copia negli Appunti**. 
3. Entra nel mondo e Apri l'editor globale per le **nozioni di base > App SDK**. Incollare l'URL per i caschi nel campo URI di destinazione e selezionare **conferma**. L'oggetto MRE verrà visualizzato e tenterà di connettersi al MRE in esecuzione nel cloud. A questo punto si vedranno alcuni caschi che è possibile fare clic su.
4. Spostare/ruotare/ridimensionare il MRE esattamente come qualsiasi altro oggetto globale.

Congratulazioni! Si sta usando MREs adesso, è molto interessante.

## <a name="troubleshooting"></a>Risoluzione dei problemi

**MRE Mostra un Emoji imbronciato** 
    * Verificare che l'URL sia corretto
    * Attiva/Nascondi è l'opzione di **riproduzione** nell'oggetto e scegli **conferma**
    * Prova a eseguire nuovamente l'accesso

**MRE è in ritardo** A seconda della posizione in cui è ospitato un MRE, è possibile che si verifichi una latenza di rete

**Perché è necessario incollare gli URL?**
In futuro, è possibile gestire e generare MREs come gli artefatti dei kit. Fino a quel momento, continueremo a usare gli URL