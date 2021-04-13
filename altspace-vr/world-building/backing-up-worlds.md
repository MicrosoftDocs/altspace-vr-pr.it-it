---
title: Backup dei mondi
description: Informazioni su come creare, gestire e risolvere i problemi relativi agli snapshot di backup dei AltspaceVR World.
ms.date: 03/11/2021
ms.topic: article
keywords: salvataggio
ms.openlocfilehash: fdef692c737bf2f92db315e04556831d60c2f377
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212657"
---
# <a name="backing-up-your-worlds"></a>Backup dei mondi

Un backup è uno "snapshot" o un record di tutti gli oggetti in un mondo in un momento specifico. Si supponga di dover creare una casa da sogno e un giorno in cui è stato eliminato accidentalmente il soggiorno. Se il giorno precedente è stato creato un backup del mondo, è possibile ripristinare il backup specifico, reimpostare il mondo ed evitare un attacco di panico. Oppure è possibile che si disponga di una versione di Cabin-in-the-Woods per ogni stagione e che si voglia passare da una versione all'altra, a tale scopo con i backup. Ogni backup è specifico per un singolo mondo e contiene non solo le trasformazioni (posizione, rotazione, scala) ma anche altre impostazioni sugli oggetti. Non esiste alcun limite al numero di backup che è possibile creare per un mondo.  

## <a name="whats-included-in-a-backup"></a>Cosa è incluso in un backup?

Un backup include attualmente la maggior parte degli elementi che è possibile generare con l'editor globale:
* Elementi (oggetti Kit)
* Etichette
* Teletrasporti
* Punti di spawn
* Foto
* App SDK MRE
* App native (ad esempio, ologrammi sulla realtà)

Non sono inclusi i seguenti elementi:

* Override del layout
* SKYBOX e ambiente audio
* Modelli
* Istruzioni
* Ruoli internazionali e ruoli contestuali

## <a name="managing-backups"></a>Gestione dei backup

Per creare un backup, è possibile aprire il Altspace editor globale e fare clic su "backup". Il primo pulsante sarà il pulsante "nuovo backup". Quando si crea un backup, viene richiesto di specificare un nome breve. Si tratta di un'operazione facoltativa, ma altamente consigliata, in quanto si otterrà un rapido confusione. I backup esistenti verranno elencati dopo il pulsante "Crea". Fare clic su un backup esistente per avviare un ripristino. Quando si ripristina un backup, il mondo viene reimpostato dopo alcuni istanti, ma è possibile che le modifiche non vengano riflesse. Attendere un minuto o due e reimpostare il mondo. **Attualmente non è possibile modificare o eliminare un backup in VR**. Per il momento è necessario gestire i backup nel sito Web. La gestione dei backup in VR verrà migliorata a breve. Nel frattempo, è stato portato a noi.

Per gestire i backup nel sito Web:

1. Passa a [worlds >](https://account.altvr.com/users/sign_in)My, trova il tuo mondo e premi "backups" nei controlli Administrator:

![Controlli dell'amministratore nel sito Web dei mondi con pannello backup aperto](images/world-backup-img-01.png)

2. È possibile creare, modificare ed eliminare i backup, verificare il numero di oggetti all'interno e persino caricare un'immagine di anteprima: 

![Finestra backup con i comandi create, Edit e Delete evidenziati](images/world-backup-img-02.png)

Non esiste alcun limite al numero di backup e la presenza di più backup non influirà sulle prestazioni del mondo.

## <a name="other-ways-to-back-up-your-worlds"></a>Altri modi per eseguire il backup dei mondi

* Crea un altro mondo, Mostra le opzioni avanzate e importa da tutto il mondo. Scegliere il mondo di cui si vuole eseguire il backup dal menu a discesa in quello nuovo. Nessun limite per le importazioni.
* Se si usa l'Uploader Unity, si consiglia vivamente di usare il controllo della versione. Ad esempio [GitHub per Unity](https://unity.github.com).

## <a name="troubleshooting"></a>Risoluzione dei problemi

**Guida Ho ripristinato accidentalmente un backup e il lavoro è andato perso** . Viene creato automaticamente un nuovo backup prima di ripristinare quello precedente. Cercarne uno con un nome che inizia con **auto** con il timestamp corretto e ripristinarne uno (ad esempio, **auto 2019-01-14T08:23:33-08:00**).  Se non funziona, inviare una [richiesta di supporto](https://help.altvr.com/hc/requests/new)

**È stato ripristinato un backup e alcuni oggetti risultano mancanti** In caso di foto, le foto sono state eliminate? Non è possibile ripristinare le foto eliminate per motivi di privacy. Invia un [richiesta di supporto](https://help.altvr.com/hc/requests/new) per poter esaminare

**Non vengono visualizzate modifiche** I backup vengono ripristinati in modo asincrono per indicare che possono essere necessari alcuni minuti per il ripristino a seconda del numero di oggetti. Ricordarsi di reimpostare il mondo e, se non viene visualizzato nulla dopo qualche minuto, provare a reimpostare. In futuro, è possibile fornire commenti e suggerimenti sullo stato del processo di ripristino