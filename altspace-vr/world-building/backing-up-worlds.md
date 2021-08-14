---
title: Backup dei mondi
description: Informazioni su come creare, gestire e risolvere i problemi relativi agli snapshot di backup dei mondi AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: salvataggio
ms.openlocfilehash: 2f4f232fd843b612563b2d7425de2b5d17720c539cc02a1493bc4b118de4f117
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125473"
---
# <a name="backing-up-your-worlds"></a>Backup dei mondi

Un backup è uno "snapshot" o un record di tutti gli oggetti in un mondo in un momento specifico. Si supponga di creare la casa dei dream e che un giorno sia stato accidentalmente eliminato il living. Se il giorno prima è stato creato un backup del mondo, è possibile ripristinare il backup specifico, reimpostare il mondo ed evitare un attacco di panico. Oppure si dispone di una versione della propria cabin-in-the-boscaglia per ogni stagione e si desidera passare da una all'altra. È possibile farlo con i backup. Ogni backup è specifico di un singolo mondo e contiene non solo le trasformazioni (posizione, rotazione, scala), ma anche altre impostazioni sugli oggetti. Non esiste alcun limite al numero di backup che è possibile creare per un mondo.  

## <a name="whats-included-in-a-backup"></a>Che cosa è incluso in un backup?

Un backup include attualmente la maggior parte degli elementi che è possibile generare con World Editor:
* Artifacts (oggetti Kit)
* Etichette
* Teletrasporti
* Generare punti
* Foto
* App dell'SDK MRE
* App native (ad esempio, Ologrammi Against Reality)

Non è incluso quanto segue:

* Sostituzioni del layout
* Skybox e audio ambientale
* Modelli
* Istruzioni
* Ruoli del mondo e ruoli contestuali

## <a name="managing-backups"></a>Gestione dei backup

È possibile creare un backup aprendo World Editor/Altspace e facendo clic su "Backup". Il primo pulsante sarà il pulsante "Nuovo backup". Quando si crea un backup, verrà richiesto di specificare un nome breve. Questo è facoltativo ma altamente consigliato perché si otterrà rapidamente confusione. I backup esistenti verranno elencati dopo il pulsante "Crea". Facendo clic su un backup esistente verrà avviato un ripristino. Quando si ripristina un backup, world verrà reimpostato dopo alcuni istanti, ma le modifiche potrebbero non essere visualizzate. Attendere uno o due minuti e reimpostare di nuovo Il mondo. **Attualmente non è possibile modificare o eliminare** un backup in VR. Per il momento è necessario gestire i backup nel sito Web. La gestione dei backup nella realtà virtuale verrà migliorata a breve. Nel frattempo, portare con noi).

Per gestire i backup nel sito Web:

1. Passare a [Worlds > Mine](https://account.altvr.com/users/sign_in), trovare il proprio mondo e premere "Backup" in Administrator Controls (Controlli amministratore):

![Controlli dell'amministratore nel sito Web worlds con il pannello backup aperto](images/world-backup-img-01.png)

2. È possibile creare, modificare ed eliminare i backup, controllare il numero di oggetti all'interno e persino caricare un'immagine di anteprima: 

![Finestra Backup con i comandi di creazione, modifica ed eliminazione evidenziati](images/world-backup-img-02.png)

Non esiste alcun limite al numero di backup e la presenza di più backup non influisce sulle prestazioni del mondo.

## <a name="other-ways-to-back-up-your-worlds"></a>Altri modi per eseguire il backup dei mondi

* Creare un altro mondo, Mostra opzioni avanzate e Importa dal mondo. Scegliere il mondo di cui si vuole eseguire il backup dal menu a discesa in quello nuovo. Non sono presenti limiti per le importazioni.
* Se si usa Unity Uploader, è consigliabile usare il controllo della versione. Ad esempio, [Github per Unity.](https://unity.github.com)

## <a name="troubleshooting"></a>Risoluzione dei problemi

**Guida. È stato ripristinato accidentalmente un backup e il lavoro non** è più disponibile. Si crea automaticamente un nuovo backup prima di ripristinarne uno precedente. Cercarne uno con un nome che inizia con **Auto** con il timestamp giusto e ripristinarne uno (ad esempio, **Auto 2019-01-14T08:23:33-08:00**).  Se non funziona, inviare un [Richiesta di supporto](https://help.altvr.com/hc/requests/new)

**È stato ripristinato un backup e alcuni oggetti sono mancanti** Se sono presenti foto, queste foto sono state eliminate? Non è possibile ripristinare le foto eliminate per motivi di privacy. Inviare un [Richiesta di supporto](https://help.altvr.com/hc/requests/new) in modo che sia possibile analizzare

**Non sono presenti modifiche** I backup vengono ripristinati in modo asincrono, ovvero possono richiedere alcuni minuti a seconda del numero di oggetti. Ricordarsi di reimpostare Il mondo e se non viene visualizzato nulla dopo pochi minuti, provare a reimpostare di nuovo. In futuro, è possibile fornire altri commenti e suggerimenti sullo stato del processo di ripristino